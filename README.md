# Arch-Linux-Installation-Guide
## Setting up
First do arch linux install guide: [Arch Linux Installation Guide](https://wiki.archlinux.org/index.php/Installation_guide)
I will tell you how to do post installation of Arch linux once you install the base system. 

Note: You have to chroot into the your arch linux root directory to install these packages. 

## Choose the grub bootloader
I recommend installing grub as a beginner to this installation. 
This link will help install and configure grub for uefi or legacy systems: [Grub](https://wiki.archlinux.org/index.php/GRUB)
Note: Remeber to configure grub after installing grub properly. 

## Install xorg
There is also wayland which is another graphical program other than xorg but I recommend xorg. Wayland is an experiemntal graphical program so avoid it especially if you are new to arch linux. 
```
# pacman -S xorg
```

## Install display manager
List of display manangers: [Display Managers](https://wiki.archlinux.org/index.php/Display_manager)

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
# systemctl enable lightdm
```

## Install desktop environment 
List of desktop environments: [Desktop Environments](https://wiki.archlinux.org/index.php/Desktop_environment)
```
# pacman -S xfce4
```

## Your arch linux installation is ready (Poweroff)
Shutdown your system
```
# shutdown now
```

## Power on your system
Your arch linux installation is finished

