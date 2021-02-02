# HP Probook 440 G4 Hackintosh (OpenCore)

OpenCore bootloader config files for my kaby lake laptop.

## System Information

| Name     |                    Model |
| :------- | -----------------------: |
| CPU      | Intel i7 7500U (Skylake) |
| GPU      |             Intel HD 620 |
| SSD      |               SATA 256GB |
| WiFi     |     Intel Dual Band (xx) |
| Ethernet |              Realtek Gbe |

- OpenCore: v0.6.5
- MacOS: v11.1 BigSur
- OpenCanopy theme: <https://github.com/tekteq/opencanopy-minimal-theme>

## Guide

<https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html>
<https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/kaby-lake.html>

### SMBIOS

Selected: `MacBookPro14,1`

Don't forget to change device uuid, board serials and network mac address
Go to <https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/kaby-lake.html#platforminfo> For information on setting up SMBIOS platform info

## Kexts Used

| Package                | Version |
| :--------------------- | ------: |
| AppleALC               |      xx |
| Lilu                   |      xx |
| WhateverGreen          |      xx |
| VirtualSMC             |      xx |
| SMCProcessor           |      xx |
| SMCSuperIO             |      xx |
| SMCBatteryManager      |      xx |
| SMCBatteryManager      |      xx |
| CPUFriendDataProvider  |     xxx |
| RealtekRTL8111         |     xxx |
| USBInjectAll           |     xxx |
| VoodooPS2Controller    |     xxx |
| VoodooRMI              |     xxx |
| VoodooSMBUS            |     xxx |
| IntelBluetoothFirmware |     xxx |
| AirportItlwm           |     xxx |

What works: WiFi, BT, Ethernet, Fn keys, Brightness, KB Backlight, Sound, Touchpad Gestures etc

## What's not working

- Battery readouts (gonna fix this soon)

## Pre Install

- Change SMBIOS Platform info (UUID, Board Serial etc)

## Post Install

- Change OpenCore to release version
- Upgrade OpenCore versions
- Check power management
  