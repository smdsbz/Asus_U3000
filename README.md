# Asus_U3000
macØS H!gh Sierra on Asus U3000


## Hardware Specs.

  Model     |   Asus U3000
------------|----------------------
  CPU       |   i7-6500U
  Memory    |   2*4G DDR3
  Storage   |   Micron M600 512G SSD
  Graphics  |   Intel HD520 (integrated)
  Display   |   13.3" 1080p IPS
  Ethernet  |   Intel 7265NGW (with Bluetooth 4.0)


## Currently Not Working

- Intel Ethernet (somehow Bluetooth is working by itself)
- Backlight
    - `ACPIBacklight.kext` is of no use
    - `IntelBacklight.kext` causes k.p.

## Look-Outs

- **Never** plug in secondary display when booting!
- `_BIX` related errors and warnings

- - - - - - - - - - - - - - - - - - - - -

## Implementation

### Prerequisites

- **Pure** macOS High Sierra image
- **Pure** Clover
- Necessary `.kext`s (see `./CLOVER/kext/`)

### Procedure

 1. Copy Clover to your `EFI` Volume / Partition
 2. BIOS settings:
      - VT-d: disable
      - DVMT: 64 / 128 M
      - Safe / Fast Boot: disable
      - SATA mode: ACHI
