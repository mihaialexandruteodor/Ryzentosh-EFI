## OS: Big Sur 11.2

Tutorial followed : https://www.youtube.com/watch?v=DqrshDmNFu4&t=2101s

## Parts

My tower config

|Part                         |Model                         |
|-------------------------------|-----------------------------|
|CPU            |`Ryzen 5 1400`          |
|GPU            |`RX 560 2GB`          |
|MOBO            |`B450M-DS3H`           |
|RAM| `16GB DDR4 2666 Mhz - dual channel`|
|SSD| `2xKingston 256GB`|
|PSU| `Inter-Tech 650W`|
||`Tested with 2 Monitors, Apple Magic Keyboard 2, blutooth mice, various peripherals, all working`|

## Not Working:
AMD virtualization not supported by Apple, so no VM. Also no FaceTime.

## BIOS settings
*disable CSM
*disable Secure Boot
*set SATA as AHCI
*disable VT-D
*enable XHCI Hand-off
*disable Legacy USB Support
*disable CFG Lock

##Various
If the Apple logo is too big on boot, Reset NVRAM when booting from the OpenCore boot menu
