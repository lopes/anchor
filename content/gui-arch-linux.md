+++
title = "GUI in Arch Linux"
description = "How to install the graphical user interface in Arch, focusing in Xorg and I3 window manager."
date = 2020-07-15
draft = true
slug = "gui-arch-linux"

[taxonomies]
categories = ["technology"]
tags = ["oss", "linux", "arch"]

[extra]
comments = true
lang = "en"
image = "https://lopes.id/installing-arch-linux/archlinux-vert-dark.png"
+++

```sh
sudo pacman -Syu
```


## Drivers
### VirtualBox
unnecessary on bare metal installations.

sudo pacman -S virtualbox-guest-utils xf86-video-vmware
sudo systemctl enable vboxservice.service

> GRUB EFI: `videoinfo` GRUB: `vbeinfo`

vim /etc/defaut/grub
GRUB_GFXMODE=1440x900x32

grub-mkconfig -o /boot/grub/grub.cfg

vim /boot/grub/grub.cfg
...-menuentry "Arch Linux"... --unrestricted...

reboot


### KVM
# Figure out the driver needed:
# lspci | grep -e VGA -e 3D
# 
# Search and install the driver:
# EXAMPLE --this driver/package was intalled with # VirtualBox guest utils:
# pacman -Ss vmware
# pacman -S xf86-video-vmware
# 
### Audio
```sh
sudo pacman -S alsa-utils
```

## Graphical Environment and Applications

```sh
sudo pacman -S xorg-server xorg-xinit ttf-dejavu \
    picom i3-gaps rofi i3lock i3status \
    arc-gtk-theme papirus-icon-theme \
    termite code ranger pcmanfm \
    firefox transmission-gtk \
    gnome-calculator                    zathura calibre \
    nitrogen maim xclip xdotool \
    imagemagick gimp inkscape feh       vlc mpv \
    nmap wireshark-cli tcpdump httping \
```

mkdir ~/{Documents,Pictures,Music,Movies,Downloads}
mkdir ~/Pictures/{wallpapers,screenshots}

git clone https://github.com/lopes/dotfiles
cp -r dotfiles/.{bashrc,config,gitconfig,gtkrc-2.0,inputrc,local,screenrc,vimrc,xinitrc,zshrc} ~

### Fonts






mkdir .local/bin
cd .local/bin
curl https://getmic.ro | bash

> **Note**: to troubleshoot Picom, run the same command in i3 configuration file and pay attention to the error message.  Maybe you will have to disable some feature for instance `vsync`.

reboot
startx


### Keyboard
setxkbmap -layout us -model abnt -variant intl
localectl --no-convert set-x11-keymap us abnt intl
localectl status

Download wallpapers and put in ~/Pictures/wallpapers.
nitrogen


## Theming
>>> Firefox theme is set with GTK, but there is an Arc-Dark theme for it.
>>> VLC theme: vlc -I skins2 --skins2-last ~/.local/share/vlc/skins2/Arc-Dark.vlt

```sh
sudo pacman -S powertop
```


## System Performance
Until now we installed the system using secure features and hardened the whole thing.  Now we implemented a lot of graphical software and it worths measuring how the boot process was affected.  The commands below show that and can be used to troubleshoot whether there is some problem in the boot process.

```sh
systemd-analyze
systemd-analyze blame
systemd-analyze critical-chain
systemd-analyze plot > /tmp/boot.png
```







## TODO-List
- Create .local/share/application .desktop files
- finish setting up i3status
- configure Rofi
- configure i3lock and its bindings
- test nerdfonts
- add blur in Picom
- implement sound tools and i3 controls
- multimedia keys with xmodmap










## References
- [Arch Linux's VirtualBox](https://wiki.archlinux.org/index.php/VirtualBox/Install_Arch_Linux_as_a_guest)
- [Arch Linux's Kernel Parameters](https://wiki.archlinux.org/index.php/Kernel_parameters)
- [Arch Linux's Xorg](https://wiki.archlinux.org/index.php/Xorg)
- [Arch Linux's Picom](https://wiki.archlinux.org/index.php/Picom)
- [Arch Linux's i3](https://wiki.archlinux.org/index.php/i3)
- [Arch Linux's Fonts](https://wiki.archlinux.org/index.php/fonts)
- [Arch Linux's Keyboard Configuration](https://wiki.archlinux.org/index.php/Xorg/Keyboard_configuration)
