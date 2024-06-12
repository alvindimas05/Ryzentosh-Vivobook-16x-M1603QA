# EFI Hackintosh Laptop ASUS Vivobook 16x M1603QA

![Preview](README.png)

## 💻 Specs :

- <b>Processor</b>: AMD Ryzen 5 5600H  
- <b>iGPU</b>: AMD Radeon RX Vega 7  
- <b>Storage</b>: SSD INTEL 512GB 670P M.2 SSDPEKNU512GZX1 PCIe 3.0 x4 NVMe 
- <b>Ram</b>: 8GB DDR4 on board + 8GB DDR4 SO-DIMM
- <b>Wireless & Bluetooth</b>: ~~Mediatek MT7921~~ Intel AX200 (Replaced)
- <b>Audio Codec</b>: ALC256
- <b>MacOs Version</b>: Sonoma 14.3.1
- <b>Installer</b>: Olarilla

## 🔧 Important Tips
- When USB Mapping using USBToolbox, enable <b>Use Native Classes</b> in the <b>Settings</b> to avoid USB issues. Mainly stall at startup and possibly sleep.
- Set the VRAM to at least 1 GB for Apps to be able to run without any lags.
- Some Apps like Adobe Photoshop need [AMDFriend](https://github.com/NyaomiDEV/AMDFriend) to be able to run. See the details [here](https://chefkissinc.github.io/guide/compatibility#compatibility-issues-with-some-apps).
- For iServices to work, use stable version of [itlwm](https://github.com/OpenIntelWireless/itlwm/releases). For now, this EFI using stable version of [itlwm](https://github.com/OpenIntelWireless/itlwm/releases/tag/v2.2.0) and [Heliport](https://github.com/OpenIntelWireless/HeliPort/releases/tag/v1.4.1). Since [Airportitlwm](https://github.com/OpenIntelWireless/itlwm/releases/tag/v2.2.0) stable version doesn't support MacOs Sonoma.
- Read other guides from [ChefKissInc](https://chefkissinc.github.io/guide/guide-differences).
- To get _slighty better_ audio quality, use [SpeakerAmp](https://apps.apple.com/us/app/speakeramp-booster-equalizer/id1496955576).

## ⚙️ BIOS
### Default
- <b>SATA Mode</b>: AHCI
### [Smokeless UMAF](https://github.com/DavidS95/Smokeless_UMAF)
- <b>AMD CBS > NBIO Common Options > GFX Configuration > iGPU Configuration</b>: UMA_SPECIFIED (So that the VRAM can be changed)
- <b>AMD CBS > NBIO Common Options > GFX Configuration > UMA Frame buffer Size</b>: 2G (2G Recommended, 1G minimum for apps with no lags)
- <b>AMD CBS > CPU Common Options > Core Performance Boost</b>: <b>Disable</b> (Reduce Heat and Power Usage) or <b>Enable</b> (Gaming Performance)
- <b>AMD PBS > s3/Modern Standby Support</b>: s3 Enable (For sleep to work)

## 📈 Working
- [x] USB Ports
- [x] HDMI port & audio
- [x] Internal Audio, Internal Mic, & Headphone Jack
- [x] Trackpad
- [x] Keyboard (Backlight, Volumes & Brightness Control)
- [x] Wifi & Bluetooth (Intel)
- [x] Sleep & Wake (Clamshell, Menu, & Idle)
- [x] Hibernation (Yes, works with <b>hibernatemode 25</b>. Probably unstable)
- [x] Some Apps (Firefox, VSCode, Discord, etc)
- [x] Some VMs/Emulators (Nox, iPhone Simulator, Docker (Minikube))
- [x] Some Games (Roblox, etc)
- [x] iServices (iMessage & Facetime)
- [x] HID Key PWRB & SLPB

## 📉 Not Working / Unstable
- [ ] Advanced OpenGL Apps (Chrome, Brave, etc)
- [ ] Hardware DRM Apps (FL Studio, etc)
- [ ] Fingerprint (MacOs/Windows)
- [ ] Audio Quality (Not Recommended for Audiophile)