# HP Probook 440 G4 Hackintosh (OpenCore)

OpenCore bootloader configuration EFI for my kaby lake laptop.

## System Information

| Name     |                    Model |
| :------- | -----------------------: |
| CPU      | Intel i7 7500U (Skylake) |
| GPU      |             Intel HD 620 |
| SSD      |               SATA 256GB |
| WiFi     |     Intel Dual Band (xx) |
| Ethernet |              Realtek Gbe |

- OpenCore: v0.6.5
- MacOS: v11.2 BigSur
- OpenCanopy theme: <https://github.com/tekteq/opencanopy-minimal-theme>

## Guide

<https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html>
<https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/kaby-lake.html>

### SMBIOS

Selected: `MacBookPro14,1`

Don't forget to change device uuid, board serials and network mac address
Go to <https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/kaby-lake.html#platforminfo> For information on setting up SMBIOS platform info

## Kexts Used

| Package                |   Version |
| :--------------------- | --------: |
| AppleALC               |     1.5.6 |
| Lilu                   |     1.5.0 |
| WhateverGreen          |     1.4.6 |
| VirtualSMC             |     1.1.9 |
| SMCProcessor           |     1.1.9 |
| SMCSuperIO             |     1.1.9 |
| SMCBatteryManager      |     1.1.9 |
| CPUFriendDataProvider  |         _ |
| RealtekRTL8111         |     2.3.0 |
| USBInjectAll           | 2018-1108 |
| VoodooPS2Controller    |     2.2.0 |
| VoodooRMI              |       2.2 |
| VoodooSMBUS            |       2.2 |
| IntelBluetoothFirmware |     1.1.2 |
| AirportItlwm           |     1.2.0 |

What works: WiFi, BT, Ethernet, Fn keys, Brightness, KB Backlight, Sound, Touchpad Gestures etc

## What's not working

- Battery readout (gonna fix this soon)

## Pre Install

- Change SMBIOS Platform info (UUID, Board Serial etc)

## Post Install

- Change OpenCore to release version
- Upgrade OpenCore versions
- Check power management

If tap to click is not working on touchpad run the following commands and reboot

```bash
defaults write com.apple.AppleMultitouchTrackpad Clicking -bool true
sudo defaults write com.apple.driver.AppleBluetoothMultitouch.trackpad Clicking -bool true
sudo defaults -currentHost write NSGlobalDomain com.apple.mouse.tapBehavior -int 1
sudo defaults write NSGlobalDomain com.apple.mouse.tapBehavior -int 1
```
  