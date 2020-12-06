# Arch-Linux-Installation-Guide
## Setting up
First do arch linux install guide: https://wiki.archlinux.org/index.php/Installation_guide
I will tell you how to do post installation of Arch linux once you install the base system. 
You have to chroot into the your arch linux root directory to install these packages. 

## Choose the grub bootloader
I recommend installing grub as a beginner to this installation. 
This link will help install and configure grub for uefi or legacy systems: https://wiki.archlinux.org/index.php/GRUB
Note: Remeber to configure grub after installing grub properly. 

## Install xorg
```
# pacman -S xorg
```

## Install display manager
List of display manangers: https://wiki.archlinux.org/index.php/Display_manager

I will use lightdm as my display manager. 
```
# pacman -S lightdm
```

## Make sure to install lightdm greeter
```
# pacman -S lightdm-gtk-greeter
```

## Enable lightdm service 
```
#systemctl enable lightdm
```

## Install desktop environment 
List of desktop environments: https://wiki.archlinux.org/index.php/Desktop_environment
```
# pacman -S xfce4
```

## You are arch linux installation is ready
Shutdown your system
```
# shutdown now
```

## Power on your system
Your arch linux installation is finished

