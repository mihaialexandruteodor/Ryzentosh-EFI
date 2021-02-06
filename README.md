## OS: Big Sur 11.2

Tutorial followed : https://www.youtube.com/watch?v=DqrshDmNFu4&t=2101s

## Parts

My tower config

|Part                         |Model                         |
|-------------------------------|-----------------------------|
|CPU            |`Ryzen 5 1400`          |
|GPU            |`RX 560 2GB`          |
|MOBO            |`B450M-DS3H`           |
|RAM| `16GB DDR4 2400 Mhz - dual channel`|
|SSD| `2xKingston 256GB`|
|PSU| `Inter-Tech 650W`|
||`Tested with 2 Monitors, Apple Magic Keyboard 2, blutooth mice, various peripherals, all working`|

## Not Working:
AMD virtualization not supported by Apple, so no VM. Also no FaceTime.

## BIOS settings
# Disable
* Fast Boot
* Secure Boot
* Serial/COM Port
* Parallel Port
* Compatibility Support Module (CSM)(Must be off, GPU errors like gIO are common when this option in enabled)
Special note for 3990X users: macOS currently does not support more than 64 threads in the kernel, and so will kernel panic if it sees more. The 3990X CPU has 128 threads total and so requires half of that disabled. We recommend disabling hyper threading in the BIOS for these situations.

# Enable
* Above 4G decoding(This must be on, if you can't find the option then add npci=0x2000 to boot-args. Do not have both this option and npci enabled at the same time.)
* If you are on a Gigabyte/Aorus or an AsRock motherboard, enabling this option may break certain drivers(ie. Ethernet) and/or boot failures on other OSes, if it does happen then disable this option and opt for npci instead
2020+ BIOS Notes: When enabling Above4G, Resizable BAR Support may become an available on some X570 and newer motherboards. Please ensure this is Disabled instead of set to Auto.
* EHCI/XHCI Hand-off
* OS type: Windows 8.1/10 UEFI Mode
* SATA Mode: AHCI


##Various
If the Apple logo is too big on boot, Reset NVRAM when booting from the OpenCore boot menu
