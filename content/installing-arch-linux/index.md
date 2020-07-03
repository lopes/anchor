+++
title = "Installing Arch Linux"
description = "My installation tutorial for Arch Linux, including LVM, FDE, and a couple of things."
date = 2020-07-03
draft = false
slug = "installing-arch-linux"

[taxonomies]
categories = ["technology"]
tags = ["oss", "linux", "arch"]

[extra]
comments = true
lang = "en"
image = "https://lopes.id/installing-arch-linux/archlinux-vert-dark.png"
+++

I have decided to install Arch Linux on my next laptop but first had to test it to be sure of my choice.  Since I was looking for a hardened installation, which was not covered by the official installation guide, I decided to create this guide for my personal use and I hope it will be useful to someone else.

This text will consider the installation in a VirtualBox VM.


## Installer Setup
Assuming you already have the official ISO, create a new VM in VirtualBox with the following characteristics --or very similar:

- CPU: 2
- RAM: 4096 MB
- Disk: 16 GB (dynamically allocated)
- A single network card with default settings
- ISO inserted in a virtual drive

Turning the VM on should load the ISO and present the shell, which is the installation's start point.  The first thing to do is to prepare this installation environment, assuring that the keyboard and connectivity are properly configured.

### Keyboard
In my case, I use a US keyboard, but it is essential for me to use Latin characters, such as àêíöú --if this set of characters isn't necessary, this step is needless.  The commands below helped me to find candidates to layout and apply the correct one:

```sh
localectl list-keymaps | egrep '(us|uk)'  # to find layouts
loadkeys us-acentos                       # load the selected layout
```

### Networking
The network should be accessible just as the system's up, but here I list some commands that can help to troubleshoot it.

```sh
ip link
ip address
dhcpcd enp0s3  # enable dhcp for enp0s3 interface
```

Having connectivity working, enable NTP to make sure the clock is synchronized with reliable sources.

```sh
timedatectl set-ntp true
timedatectl status
```


## Disk Preparation
These steps will show how to perform full device encryption using LVM, enabling the disk to receive the new system.  

### Partitioning
The main goal here is to create only a minimum bootable unencrypted partition and an encrypted partition on the rest of the disk.  Table 1 resumes this scenario.

| Mount point | Partition | Size   | File system |
|-------------|-----------|--------|-------------|
| `/efi`\*    | primary   | 550 MB | FAT32       |
| `/boot`     | primary   | 450 MB | EXT4        |
| LVM         | primary   | Rest   | LVM         |

> **Note:** on the physical system using [UEFI](https://en.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface), it is necessary to create another partition to mount the `/efi` directory and this partition must be formatted using FAT32 --personally, I recommend to allocate 550 MB for it.

You can use `cfdisk` for partitioning, but this tutorial will present the `fdisk` commands.  


```sh
fdisk -l         # list the available disks
fdisk /dev/sda   # start partitioning /dev/sda

# inside fdisk...
n > p > default > default > +450M    # [n]ew [p]rimary partition with 450 MB
n > p > default > default > default  # [n]ew [p]rimary partition with the left space
w                                    # [w]rite changes and exit
```

### Encrypting
[LUKS](https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup) will be used to encrypt the system's partition and this is done in the next command list.  Note that after running the first command you will be asked to insert a password and must be aware to insert a strong one.  This password will always be asked on the system boot.

The second command will open this newly encrypted partition as a new device in `/dev/mapper/luks`.

```sh
cryptsetup -v --type luks --cipher aes-xts-plain64 --key-size 256 --hash sha256 --iter-time 2000 --use-urandom --verify-passphrase luksFormat /dev/sda2

cryptsetup luksOpen /dev/sda2 luks
```

### LVM
The encrypted partition will host the [LVM](https://opensource.com/business/16/9/linux-users-guide-lvm) system with the partitions shown in Table 2 --these are the partitions I like to use in my systems and the spaces are dimensioned to this 16 GB disk.

| Mount point | Partition type | Size   | File system |
|-------------|----------------|--------|-------------|
| swap        | primary        | 512 MB | swap        |
| `/`         | primary        | 6 GB   | EXT4        |
| `/home`     | primary        | 6 GB   | EXT4        |
| `/var`      | primary        | REST   | EXT4        |

The next command listing shows all commands needed to create LVM volumes for each partition.  The last command is optional but is good to check if everything's fine.

```sh
pvcreate /dev/mapper/luks
vgcreate vg0 /dev/mapper/luks

lvcreate --size 512M vg0 --name swap
lvcreate --size 6G vg0 --name root
lvcreate --size 6G vg0 --name home
lvcreate -l +100%FREE vg0 --name var

lvdisplay
```

### Formatting
With all partitions in place, they should be formatted as previously planned.  The next listing shows all commands to accomplish this task --the last one just presents a resume of everything.

```sh
mkswap /dev/mapper/vg0-swap
mkfs.ext4 /dev/sda1
mkfs.ext4 /dev/mapper/vg0-root
mkfs.ext4 /dev/mapper/vg0-home
mkfs.ext4 /dev/mapper/vg0-var

lsblk  # just to see the big picture
```

### Mounting
Finally, all partitions must be mounted, including those inside the root partition and the swap.

```sh
swapon /dev/mapper/vg0-swap

mount /dev/mapper/vg0-root /mnt

mkdir /mnt/{boot,home,var}

mount /dev/sda1 /mnt/boot
mount /dev/mapper/vg0-home /mnt/home
mount /dev/mapper/vg0-var /mnt/var
```


## Installation
At this point, the disk should be ready to receive the system's files.  To do it, `pacman` will be used, but since it comes with a lot of repositories and many of them could perform really bad for some users, it is recommended to allow only the nearest from the user.  I use two simple commands to discard all repositories but the ones in the countries I selected:


```sh
cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.bkp

sed -n '/\(Brazil\|United States\)/,+1p' /etc/pacman.d/mirrorlist.bkp > /etc/pacman.d/mirrorlist
```

Now the system can be installed with the next command --notice that I'm installing additional packages I use, but most users will only want the first three --`base`, `linux`, and `linux-firmware`.

```sh
pacstrap /mnt base linux linux-firmware ufw openntpd sudo zsh tmux python atop networkmanager dhcpcd dnsutils wget curl git vim
```

At this point, you should have a virtual environment running in memory --which you are using to install the system-- and a Linux system installed on the disk mounted in `/mnt`.  To finish the installation, the objective is to chroot `/mnt`, but first the `/etc/fstab` file must be generated and I like to set up `/tmp` as a virtual partition for security reasons.  The next command shows how this can be achieved.

```sh
genfstab -U /mnt >> /mnt/etc/fstab

echo "tmpfs   /var/tmp tmpfs  size=1G,mode=1777,rw,nodev,nosuid,noexec    0    0" >> /mnt/etc/fstab

echo "tmpfs   /tmp     tmpfs  size=1G,mode=1777,rw,nodev,nosuid,noexec    0    0" >> /mnt/etc/fstab

echo "tmpfs   /dev/shm tmpfs  size=1G,rw,nodev,nosuid,noexec    0    0" >> /mnt/etc/fstab

arch-chroot /mnt
```


## Localization
Inside the installed system, the localization settings should be created to appropriately define timezone, idioms, and the keyboard.  Starting with the timezone, the next listing shows the commands --substitute the time zone accordingly.

```sh
ln -sf /usr/share/zoneinfo/America/Sao_Paulo /etc/localtime
hwclock --systohc
```

I do mix `en_US` and `pt_BR` as locales, but always in UTF-8.  To create a similar setup --even if only one locale will be used--, uncomment the language lines in the `/etc/locale.gen` file and generate the locales.  Then, create the configuration file for your system use them --see the next listing.

```sh
vim /etc/locale.gen
# uncomment desired locales

locale-gen

vim /etc/locale.conf
# LANG=en_US.UTF-8
# LANGUAGE=en_US
# LC_ADDRESS=en_US.UTF-8
# LC_COLLATE=en_US.UTF-8
# LC_CTYPE=en_US.UTF-8
# LC_IDENTIFICATION=en_US.UTF-8
# LC_MESSAGES=en_US.UTF-8
# LC_NAME=en_US.UTF-8
# LC_TELEPHONE=en_US.UTF-8
# LC_MEASUREMENT=pt_BR.UTF-8
# LC_MONETARY=pt_BR.UTF-8
# LC_NUMERIC=pt_BR.UTF-8
# LC_PAPER=pt_BR.UTF-8
# LC_TIME=pt_BR.UTF-8
```

To configure the keyboard, just create the `/etc/vconsole.conf` file and set the same keyboard layout you are using for the installation --considering you changed the default at the beginning.

```sh
echo "KEYMAP=us-acentos" > /etc/vconsole.conf
```


## Networking
Networking setup includes creating the hostname files and enabling DHCP service --this last step is not necessary if you pretend to use a static IP approach, but it is up to you.

```sh
echo "orion" > /etc/hostname

vim /etc/hosts
# 127.0.0.1   localhost
# ::1         localhost
# 127.0.1.1   orion.lopes.id  orion

systemctl enable dhcpcd
```


## Users
This is not a necessary step at all, but the root user should be avoided for security reasons in any operating system.  So, I will create a user (`lopes`) and allow him to use `sudo` --note that my default shell is `zsh`.   Strong passwords must be defined for both users.

```sh
passwd  # set root password

useradd -m -G wheel,audio,video,optical,storage -s /bin/zsh lopes
passwd lopes

visudo
# uncomment this line: "%wheel ALL=(ALL) ALL"
```


## Boot Loader
The last step is to install and configure the boot loader, ensuring that the LVM and encrypted partition will be recognized.  For doing this, [GRUB](https://en.wikipedia.org/wiki/GNU_GRUB) and [mkinitcpio](https://wiki.archlinux.org/index.php/Mkinitcpio) must be adjusted as shown in the following listing.

### GRUB
After installing the package, it must be installed in the boot device and configuration must be created.  Then, the default configuration file must be changed because the variable `GRUB_CMDLINE_LINUX` should contain the command line to load the encrypted device and the variable `GRUB_ENABLE_CRYPTODISK` must be set to "yes".

### mkinitcpio
This Arch script must be properly configured to support the file systems, so module `ext4` should be loaded and hooks `encrypt` and `lvm2` must be loaded before `filesystems`.


```sh
pacman -S grub lvm2

vim /etc/mkinitcpio.conf
# MODULES=(ext4)
# HOOKS=(...encrypt lvm2 filesystems...)

vim /etc/default/grub
# GRUB_CMDLINE_LINUX="cryptdevice=/dev/sda2:luks:allow-discards"
# GRUB_ENABLE_CRYPTODISK=y   # uncomment this

mkinitcpio -p linux

grub-install --target i386-pc --recheck /dev/sda
grub-mkconfig -o /boot/grub/grub.cfg
```


## Reboot
The system must be fully functional at this point, so it is time to turn the media install off and boot the installed system.  Run the following commands to get out from the chroot environment, guarantee that the disk is properly unmounted, and reboot the system --remember to remove the media installation before the new boot.

```sh
exit
umount -R /mnt
swapoff -a
reboot
```

After rebooting you will be asked to enter the password to decrypt the disk and after that, the system will be loaded, presenting you the login prompt.  At this point, you are able to go ahead and customize the system as you wish and install further packages.

Let's rock and roll in Arch!


## References

* [Arch Linux's Official Installation Guide](https://wiki.archlinux.org/index.php/installation_guide)
* [Arch Linux's Device Encryption](https://wiki.archlinux.org/index.php/Dm-crypt/Device_encryption)
* [Arch Linux's Encrypting an Entire Device](https://wiki.archlinux.org/index.php/Dm-crypt/Encrypting_an_entire_system)
