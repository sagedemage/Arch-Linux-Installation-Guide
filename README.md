# Arch-Linux-Installation-Guide

## About getting into Arch Linux
I will assume you are knowledgable of linux. I would recommend you have some experience with Ubuntu or Manjaro linux distributions. Arch linux is an advance linux distribution because of its minimal nature of it. The good news is that Arch Linux installs faster than Debian from my experience. The bad news is that programs will break and you will have to figure out how to fix them in Arch Linux. I reccomend you look at the lastest news section of Arch Linux website (https://archlinux.org/). 

## Reccomendations
1. Have some experience with 
--> Ubuntu 
or 
--> Manjaro

2. Learn to use the terminal in linux. This will likely take some time to master it if you are not used to with it. When I started Arch Linux I had rusty terminal skills. 

3. Install it on virtual machine with a program called virtualbox. This would give you practice to install Arch Linux on hardware. 

## Setting up
First do arch linux install guide: [Installation Guide] (https://wiki.archlinux.org/index.php/Installation_guide)
I will tell you how to do post installation of Arch linux once you install the base system. 

Note: You have to chroot into the your arch linux root directory to install these packages. 

## If you need help getting internet connection for wifi
Check this page for help with that: [iwd](https://wiki.archlinux.org/index.php/Iwd)

## Adding user 
This command automatically adds the user in the wheel group. This is important for giving your user escalated priviledges. 
```
useradd -mg wheel username 
```
## Editing the sudoers file
The file path to the sudoers file: /etc/sudoers. Lets edit the sudoers file.
```
nano /etc/sudoers
```
Look for this line and uncomment the pound sign (#) before %wheel ALL=(ALL) ALL.

Before
```
## Uncomment to allow members of group wheel to execute any command
#%wheel ALL=(ALL) ALL
```
After
```
## Uncomment to allow members of group wheel to execute any command
%wheel ALL=(ALL) ALL
```
Now the username can execute commands with sudo. 

## Choose the grub bootloader
I recommend installing grub as a beginner to this installation. 
This link will help install and configure grub for uefi or legacy systems: [Grub](https://wiki.archlinux.org/index.php/GRUB)
Note: Remember to configure grub after installing grub properly. 

## Install xorg
The program needed to run graphical programs. 
```
# pacman -S xorg
```

## Install display manager
List of display manangers: [Display Manager](https://wiki.archlinux.org/index.php/Display_manager)

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

## Install network manager applet 
Install this to get network manager icon tray for connecting to wifi.
```
# pacman -S network-manager-applet
```

## Install desktop environment 
List of desktop environments: [Desktop Environment](https://wiki.archlinux.org/index.php/Desktop_environment)
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

