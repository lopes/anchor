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

First update the system:
sudo pacman -Syu


## Drivers
### VirtualBox
unnecessary on bare metal installations.

sudo pacman -S virtualbox-guest-utils xf86-video-vmware

Enable the modules at boot time:
sudo systemctl enable vboxservice.service

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

sudo pacman -S alsa-utils


## Graphical Environment
### Installation
sudo pacman -S xorg-server xorg-xinit ttf-dejavu \
    picom i3-gaps i3lock i3status rofi \
    arc-gtk-theme papirus-icon-theme \
    termite code ranger pcmanfm \
    firefox chromium \
    gnome-calculator \
    nitrogen maim xclip xdotool \
    imagemagick gimp inkscape feh vlc mpv \
    
    nmap wireshark-cli tcpdump httping\

### Keyboard
setxkbmap -layout us -model abnt -variant intl
localectl --no-convert set-x11-keymap us abnt intl
localectl status


### Tunning
mkdir ~/{Documents,Pictures,Music,Movies,Downloads}
mkdir ~/Pictures/wallpapers


git clone https://github.com/lopes/dotfiles
cp -r dotfiles/.{bashrc,zshrc,config,local,inputrc,screenrc,vimrc,gitconfig,xinitrc,gtkrc-2.0} ~
fc-cache -f -v

mkdir .local/bin
cd .local/bin
curl https://getmic.ro | bash



startx


## Theming
>>> Firefox theme is set with GTK, but there is a Arc-Dark theme for it.
>>> VLC theme: vlc -I skins2 --skins2-last ~/.local/share/vlc/skins2/Arc-Dark.vlt


### Optional: Fonts
Install more fonts.  Clone my repository, move .local/share/fonts to your HOME and install them:

fc-cache -f -v

listing available fonts:
fc-match -a
<file>: "<name>" "<style>"




## References
- [Arch Linux's VirtualBox](https://wiki.archlinux.org/index.php/VirtualBox/Install_Arch_Linux_as_a_guest)
- [Arch Linux's Kernel Parameters](https://wiki.archlinux.org/index.php/Kernel_parameters)
- [Arch Linux's Xorg](https://wiki.archlinux.org/index.php/Xorg)
- [Arch Linux's Picom](https://wiki.archlinux.org/index.php/Picom)
- [Arch Linux's i3](https://wiki.archlinux.org/index.php/i3)
- [Arch Linux's Fonts](https://wiki.archlinux.org/index.php/fonts)
- [Arch Linux's Keyboard Configuration](https://wiki.archlinux.org/index.php/Xorg/Keyboard_configuration)
