# Hackintosh Intel NUC8 BEH (i3)
EFI boot folder based on OpenCore for Intel NUC 8 BEH Core i3
Last update: December 2nd 2025.  

## Description

EFI files based on OpenCore  
OpenCore version: 1.0.6   
Compatible macOS version: __Ventura 13.7.2__

## How to use

1/ Download a release corresponding to your macOS version  
2/ Extract it on USB stick (GPT disk with FAT32 primary partition) or EFI partition  
3/ Generate a new "SystemSerialNumber" and "SystemUUID" using OCAuxiliaryTools for example  
4/ Save and reboot  

### Important note: macOS Ventura

At the moment, macOS Ventura is the latest macOS version running fine.  
macOS Sonoma and Sequoia are compatible with Mac Mini 2018 but OpenCore won't boot.  

### Important note: Intel Wireless Card with Sequoia (work in progress)  

Airportitlwm actually doesn't support Sequoia. That's the trick:  
- use OCAuxiliaryTools and edit config.plist to uncomment DP/PCIExpress entry (remove #)  
- reboot computer and patch with OpenCore Legacy Patcher
- reboot computer again and comment DP/PCIExpress entry (set #)  
- reboot another time your laptop  

It uses *Ventura*-airportitlwm.kext to work under Sequoia.  
Actually, there is no Bluetooth support.  

## Hardware

__Laptop Toshiba Tecra Z50-A__  
![Intel NUC8 Picture](/Assets/Intel-NUC8-BEH.jpg "Intel NUC8 BEH")  
[Datasheet Intel NUC8](/Assets/Intel-NUC8-BEH-Datasheet.pdf)  

| Type	| Name                   |
|:------|:-----------------------|
| CPU	| Intel i3 8109U	 |
| RAM	| 1xDDR4 2133MHz - 8Gb  |
| GPU	| Intel Iris Plus Graphics 655 |
| Drive	| SATA SSD 500 Gb	 |
| Sound	card	| Integrated	 |
| LAN   | Intel I219V		|
| WLAN	| Intel Dual Band Wireless-AC 9560 	 |
| Bluetooth | Intel Wireless-AC 95600 #Port008 ||
| Display | Port HDMI |

## SMBIOS Info

System Product Name : Mac Mini 2018 8.1   
System Serial : C07CG0UPJYVX  

## Working and Not-Working

### Working
WIFI : ok  
GPU : ok   
Shutdown/Restart : ok  
USB Port : ok  
Sound : ok (speakers and microphone)  
Brightness : ok  
Webcam : ok  
Keyboard : ok  
Card Reader : ok  
Bluetooth : ok  
Auto-unlock : with BLEUnlock  
Boot shime : ok
HDMI display output : ok

### Working with issue

Sleep/Wake : partially (randomly not enter in sleep mode)    
Touchpad : partially (need improvements / broken gestures)    
  
### Not-Working
  
## Screenshots
  
### macOS Ventura 13.6.4  
To be captured.  
  
## Work to do

## About Boot Shime

## Credit

EFI Base folder : https://github.com/Lorys89/Intel-NUC8-Hackintosh  
