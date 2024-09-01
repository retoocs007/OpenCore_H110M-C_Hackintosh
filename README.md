# OpenCore H110M-C Hackintosh
ASUS H110M-C with Intel Core i3-6000 Hackintosh (OpenCore 0.9.1)


[![OpenCore](https://img.shields.io/badge/OpenCore-0.9.1-blue.svg)](https://github.com/acidanthera/OpenCorePkg)
[![macOSver](https://img.shields.io/badge/macOS-Monterey-brightgreen.svg)]()
[![macOSver](https://img.shields.io/badge/macOS-Ventura-brightgreen.svg)]()
[![macOSver](https://img.shields.io/badge/macOS-Sonoma-brightgreen.svg)]()


### 🖥️ Hardware
| Component    | Info                                                      |
|--------------|-----------------------------------------------------------|
| **CPU**      | `Intel Core i3-6100`                                      |
| **RAM**      | `Micron 16GB 2133MHz DDR4`                                |
| **Storage**  | `Kingston 256GB SSD`                                      |
| **iGPU**     | `Intel HD Graphics 530 spoofed as Intel UHD Graphics 630` |
| **dGPU**     | `None`                                                    |
| **Audio**    | `ALC887 - alcid=1`                                        |
| **Ethernet** | `Realtek Gigabit Ethernet RTL8111GR`                      |

### ⚠️ Disclaimer:
- Use this EFI configurations as a **starting point** if you have similar hardware, remember to always make your EFI by following [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- This EFI configurations aren't constantly updated, especially if there is not updated Dortania's guide for new OpenCore version
- Before you use these EFI configurations please generate SMBIOS using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) and update configurations accordingly 
- This readme is not complete like EFI configurations themselves 
##


![ScreenShot](/Screenshots/Screenshot-Sonoma.png?raw=true "ScreenShot")


### ✅️ What works (tested so far)
- iGPU acceleration Intel UHD 530 1536 MB spoofed as Intel UHD 630
- Audio
- DVI output with hardware acceleration
- USB ports
- Ethernet
- iMessage

### ❌️ What doesn't work
- Will update this list as I find out

### ⚙️ Setup
- When generating SMBIOS data using GenSMBIOS for Monterey and Ventura choose iMac18,1 and for Sonoma choose iMac19,1 
- Difference between Monterey and Ventura is that Monterey doesn't have any configuration for the **PciRoot(0x0)/Pci(0x2,0x0)**
- For Big Sur you can use Monterey configuration with default Dortania configuration for iGPU in the **PciRoot(0x0)/Pci(0x2,0x0)** and SMBIOS for iMac17,1