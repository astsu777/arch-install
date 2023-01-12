# Arch Install

This repository hosts a *BASH* script that can be used to automate the installation of Arch Linux. The script has the following abilities:

* Automate disk partitioning
* Configure LVM automatcally
* Enable SWAP partition the same size as the RAM
* Full Disk Encryption (FDE) using LUKS (optional)
* Install a minimal base system
* Support for UEFI/BIOS systems

⚠️ **This script should not be used to setup a server!** Please use a proper automation framework such as [Ansible](https://www.ansible.com/) to do so.
However, I use it to install any workstation or personal computer (desktop or laptop) where I intend to use Arch Linux.

# Requirements
It is necessary to download the live Arch Linux environment. The ISO file can be downloaded from [Arch's Website](https://archlinux.org/download/).

Once the ISO image is downloaded, you need to prepare a boot drive (USB key or CD/DVD) and boot your computer from it. All instructions can be found on the [Arch Wiki](https://wiki.archlinux.org/title/Installation_guide#Prepare_an_installation_medium).

# Compatibility
This script has been fully validated with the following systems:

| OS | Compatibility | Comment |
|:-:|:-:|:-|
| Lenovo X1 Carbon Gen9 | ✅ | Fully compatible |
| MacBook Air 2012 | ✅ | Fully compatible |
| Virtual Machines (KVM/VirtualBox/VMware) | ✅| Fully compatible |
| Dell Optiplex 3000 Micro | ✅ | Fully compatible |

From a general perspective, the script should work on pretty much any standard laptop/desktop computer.

# Usage
It is recommended to download the script and execute it locally. In order to so, type the following commands:

```
curl -LO https://raw.githubusercontent.com/astsu777/arch-install/master/arch-install)
./arch-install
```

# Log
The output to the console will sho everything that is happening. A log file is always created in the */root* folder and is unique for each run. This way, it is possible to review all performed operations and check for errors.

# CHROOT
The script will not enter the CHROOT environment automatically. However, it will prompt you to do so and provide instruction to execute another script to continue the installation.

# Contact
You can always reach out to me:

* [Twitter](https://twitter.com/astsu777)
* [Email](mailto:gaetan@ictpourtous.com)

# TODO

* Better on-screen log
* Manage multiple locale
* Manage manual partitioning completey (buggy for now)
* More partition layout?
* Provide ability to detect hardware and propose certain drivers
* Show a menu to choose the timezone
