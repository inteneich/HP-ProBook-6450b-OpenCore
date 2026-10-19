# HP-ProBook-6450b-OpenCore
 
### Before you give this EFI a try, make sure you read [this](#generating-your-own-serial-and-editing-rom)!

This repo includes an OpenCore EFI for the HP ProBook 6450b laptop, made specifically for OS X 10.8.

Testing on:

Model | HP ProBook 6450b
------------- | ---------------
CPU | Intel Core i5 M 520
GPU | Intel HD Graphics (Ironlake)
RAM | 4 GB DDR3-1066 (spare Samsung sticks)
Ethernet | Intel 82574L
Wi-Fi | Intel Centrino Wireless N-1000

## What works?

- Boot
- USB
- Ethernet
- Wi-Fi
- GPU acceleration
- Sleep
- Audio (requires VoodooHDA)

## What doesn't work?

- display over DP

## BIOS settings

[Dortania BIOS Guide](http://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/arrandale.html#intel-bios-settings)

## Creating the installer

You should have a working install of macOS, then [follow this](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install-pkg.html).


After you have created a bootable Installer, copy the EFI folder to the EFI partition of the installer drive and install as usual (GUID Partiton Map; Mac OS Extended (Journaled)). After the installation, mount the EFI partition of the installed OS and copy the EFI folder to its partition.

## Generating your own serial and Editing ROM

Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate a serial for MacbookPro5,2

use [ProperTree](https://github.com/corpnewt/propertree) to manually enter the details in the following sections of the config (as shown in the video): (SystemSerialNumber, MLB, UUID and ROM)

https://user-images.githubusercontent.com/59102649/116117179-3ea51200-a6bc-11eb-8a18-a03f7bb5bf1d.mp4

## Credits

* [inteneich](https://github.com/inteneich) (for creating the EFI)
* [TECHNIKVERBOT](https://github.com/TECHNIKVERBOT) (for README.md)
* [acidanthera](https://github.com/acidanthera) (for OpenCore and the kexts)
* [dortania](https://dortania.github.io/OpenCore-Install-Guide/) for their awesome guide
