# Dell Latitude 3410 EFI OpenCore

OpenCore EFI configuration for Dell Latitude 3410, tailored for macOS Sonoma 14.4 and Intel 10th Generation processors.

![Dell Latitude 3410](https://static.toiimg.com/thumb/resizemode-4,msid-78414846,imgsize-300,width-300,imgv-3/78414846.jpg)

## System Specifications

| Component   | Model Details         |
| :---------- | :-------------------- |
| **CPU**     | Intel Core i7-10510U  |
| **iGPU**    | Intel UHD620          |
| **Storage** | KBG40ZNS512G NVMe KIOXIA |
| **Audio**   | Realtek ALC236        |
| **WLAN**    | Intel AX201           |
| **LAN**     | Realtek RTL8111       |

## macOS Version

This EFI configuration is designed specifically for **macOS Sonoma 14.4** but should also work with earlier versions. To use this EFI with versions other than Sonoma, replace the `AirportItlwm.kext` in `EFI/OC/Kexts` with the appropriate version.

[Download AirportItlwm.kext here](https://github.com/OpenIntelWireless/itlwm/releases)

---

## Features

- Full support for Intel UHD620 integrated graphics.
- NVMe KIOXIA drive support included.
- Realtek ALC236 audio support (limited to external output; microphone not supported natively).
- Intel AX201 wireless support via AirportItlwm.kext.

---

## Known Issues

- **dGPU Support**: No NVIDIA dGPU support available.  
- **Microphone**: No Intel microphone array support. Use a USB-C DAC instead for audio input.

---

## Setup Instructions

1. **Download** the latest release from this repository and extract it to a USB drive.
2. Modify the **SMBIOS** information in `EFI/OC/config.plist` under `PlatformInfo/Generic` before booting the system.

For more detailed instructions on configuring the SMBIOS, refer to the [OpenCore Laptop Guide](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/coffee-lake-plus.html#platforminfo).

![OpenCore Config](https://dortania.github.io/OpenCore-Install-Guide/homepage.png) 

---

## Not Working

- **dGPU (NVIDIA)**: This laptop has no NVIDIA GPU support.
- **Microphone**: Built-in Intel microphone array doesn't work. Use an external **USB-C DAC** for microphone support.

---

## Credits

- [OpenIntelWireless](https://github.com/OpenIntelWireless) for wireless drivers.
- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/) for the detailed installation process.
---

