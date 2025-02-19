# nwg-iso

This repository is a part of the nwg-shell project. Please check the [project website](https://nwg-piotr.github.io/nwg-shell).

[![Download nwg-iso](https://a.fsdn.com/con/app/sf-download-button)](https://sourceforge.net/projects/nwg-iso)

The nwg-iso project provides two ISO images built with [archiso](https://wiki.archlinux.org/title/Archiso), with additions to ensure a simple way to install [Arch Linux](https://archlinux.org), [sway](https://swaywm.org/) & [Hyprland](https://hyprland.org/) Wayland compositors, and the [nwg-shell](https://nwg-piotr.github.io/nwg-shell) toolbox.

## nwg-mini

The live environment (CLI) comes with the `installer` command, which is a simplified version of the interactive installation with the [archinstall](https://github.com/archlinux/archinstall) script. Some must have stuff has already been pre-selected. The iso also provides a script to install the shell itself - from the user account (see [Multiple user accounts](#multiple-user-accounts) below). During installation you can choose the text editor and the web browser. Some packages (installer, AUR helper, customized sddm theme, python-dasbus and wlr-randr) have been enclosed in a local repository. Besides, we only use [Arch](https://archlinux.org/packages) and [AUR](https://aur.archlinux.org/) repositories. Installation time (since you press 'Install' until you see the login screen): 12 minutes.

## nwg-live

This ISO comes with live Hyprland/sway environment, so that you can test compositors and the shell before installation. The text editor and the web browser are predefined: mousepad and Firefox. Of course you can replace them later with what you like most. All the AUR stuff comes packaged in the local repository. The entire installation, for all user accounts, is performed in one pass by the `installer` script. Please find the "Installer" item in the top panel menu. Installation time: 6 minutes.

## Installation

### nwg-mini

1. Download the nwg-mini ISO from [SourceForge](https://sourceforge.net/projects/nwg-iso/).
2. Create USB flash installation medium, as decribed in [Arch Wiki](https://wiki.archlinux.org/title/USB_flash_installation_medium). Or just use SUSE Studio [ImageWriter](https://github.com/openSUSE/imagewriter), as I do.
3. Boot from the flash drive, type the `installer` command. Go through the interactive Arch Linux installation.
4. Reboot and login as a user with sudo privilleges. Wait for the script to finish installation and reboot.

![image](https://github.com/nwg-piotr/nwg-iso/assets/20579136/14587d6e-f794-4cc7-8830-5a955aaa9776)

### nwg-live

1. Download the nwg-live ISO.
2. Create USB flash installation medium, as described above.
3. Boot from the flash drive, enjoy the live sway and Hyprland environment. **User**: `nwg` **Password**: `nwg`
5. If you decide to install, use the "Installer" item in the top panel menu. The script will run in the terminal emulator.

## Post-installation

Find the 'Shell settings' item in the top panel menu. Review your settings here.

![2023-09-16-001157_hypr_screenshot](https://github.com/nwg-piotr/nwg-iso/assets/20579136/a11a9786-558e-4567-a7f4-8b2a5226032c)

Click the (i) icon in the top panel to see key bindings help. Open the Controls menu in the top panel to see more configuration tools.

## Multiple user accounts

If you installed from the nwg-mini ISO, to set up nwg-shell config files on another user's account you need to:

1. Log in as another user in console;
2. execute the `nwg-shell-installer -w -hypr` command.

## Testing on a virtual machine

Running sway and Hyprland on a VM is possible, but frustrating. If you use VirtualBox, the installer will add VirtualBox 
guest utils automatically. The necessary `export WLR_NO_HARDWARE_CURSORS=1` line will be added to `/etc/profile` as well.
The mouse pointer, however, well be sluggish and slow-reacting. I highly recommend testing on real hardware. 
If you still want to test on a VM, remember to enable 3D acceleration and EFI.

## Preinstalled stuff

- [foot](https://wiki.archlinux.org/title/Foot) - Fast, lightweight and minimalistic Wayland terminal emulator (Super+T);
- [baph](https://bitbucket.org/natemaia/baph) - Basic AUR Package Helper;
- [fastfetch](https://github.com/fastfetch-cli/fastfetch) - Like neofetch, but much faster because written in C;
- [pacseek](https://github.com/moson-mo/pacseek) - TUI for searching and installing Arch Linux packages;
- [swayimg](https://github.com/artemsen/swayimg) - Image viewer for Sway/Wayland;
- [Thunar](https://docs.xfce.org/xfce/thunar/start) - Simple text editor for Xfce;
- (nwg-live ISO) [Mousepad](https://docs.xfce.org/apps/mousepad/start) - Simple text editor for Xfce;
- (nwg-live ISO) [Firefox](https://www.mozilla.org/firefox) - Standalone web browser from mozilla.org.

**Aliases:**

- `cls` for `clear`

## Contact

See my [GitHub profile](https://github.com/nwg-piotr) for contact info.
