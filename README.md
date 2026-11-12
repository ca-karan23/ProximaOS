# 🌌 Project ProximaOS™ — Xiaomi 15 Ultra Edition (HyperOS 3)

![Device](https://img.shields.io/badge/Device-Redmi%20Note%2014%205G%20(beryl%20%2F%20citrine)-FF3D12?style=for-the-badge&logo=xiaomi)
![OS](https://img.shields.io/badge/HyperOS-v3.0.306.0%20%7C%20Android%2016%20(SDK%2036)-0066FF?style=for-the-badge&logo=android)
![Root](https://img.shields.io/badge/Root-KernelSU--Next%20Pre--Integrated-00C853?style=for-the-badge)
![Maintainer](https://img.shields.io/badge/Maintainer-Karan-8A2BE2?style=for-the-badge)
![License](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-orange?style=for-the-badge)

> **Project ProximaOS™** is a flagship-grade modded **Xiaomi HyperOS 3 (`OS3.0.306.0.WOQCNXM` | Android 16)** ROM engineered specifically for the **Redmi Note 14 5G (`beryl` / `citrine`)**. Built with **DNA Tool & MT Manager** and powered by **KernelSU-Next**, it unlocks the full **Xiaomi 15 Ultra** visual pipeline, real-time Gaussian glass blurs, iOS-inspired animations, and unrestricted system performance—with zero bootloops.

---

## ✨ Key Highlights & Official Changelog

### 🎨 Visuals, iOS Aesthetics & UI Overhaul
- **Custom Boot Animation & Setup Wizard**: Features a custom ProximaOS™ boot animation and a redesigned Setup Wizard (`Provision.apk`) sporting the **Project ProximaOS** vector branding with a vibrant Red-Orange `OS` accent.
- **ColorOS-Inspired About Phone Page**:Redesigned About Phone screen featuring the bold **PROXIMAOS** metallic vector banner (`SettingsResourceOverlay.apk`), detailed hardware specification cards, and custom build banner (`OS3.0.306.0 | ProximaOS™ | Karan`).
- **Fully Customizable iOS-Style Control Center & Volume Bar**: Smooth frosted glass real-time blur with custom blue tint accents and an iOS-style vertical volume slider.
- **iOS-Style App Opening Animations & Parallel Sweep**: Non-linear HyperOS V3 transitions (`persist.sys.hyper_transition_v=3`) with parallel rendering (`enable_parallel_sweep=true`) and gesture bar follow animations.
- **iOS Emoji Support & Dynamic Font Animations**: Pre-installed iOS emojis and variable system font weight animations (`ro.miui.ui.font.animation=enable`).
- **Stackable Widgets & Expanded Icon Styling**: Full support for HyperOS stackable desktop widgets, App Vault enhancements, and expanded icon customization.
- **AI Dynamic & Depth Wallpapers**: Unlocked flagship lockscreen depth effects and AI wakeup transitions.
- **New Power Menu & Screenshot Frames**: Modernized power menu slider and device screenshot frame overlays.
- **Added My Love 🥰**: Crafted with passion, attention to detail, and extra love in every UI corner.

### 🚀 Performance, Computility 4 & Hardware Unlocks
- **Upgraded CPU & GPU Computility to Level 4 (`V2 Level 3`)**: Overridden stock budget tier (`computility=2`) to `persist.sys.computility.cpulevel=4` & `gpulevel=4`, unlocking flagship shader pipelines without breaking PowerVR (`IMG BXM-8-256`) tile borders.
- **Global 120Hz Refresh Rate**: Unlocked 120Hz default refresh rate across all applications (`defaultFps=120` & `smart_fps_value=120`) with `windowsmgr.max_events_per_sec=120`.
- **Xiaomi 15 Ultra Feature Spoofing & Device Features (`beryl.xml` / `citrine.xml`)**:
  - **Always-On Display (AOD) "Always" Mode**: Removed the stock 10-second AOD restriction (`is_only_support_keycode_goto=false`, `support_aod_always=true`) safely without FSAOD SystemUI crashes.
  - **Display Expert Mode & TrueColor**: Enabled P3/sRGB/RGB/HSV calibration controls, TrueTone, MEMC Smart Frame Rate, and SDR-to-HDR Video Toolbox enhancements.
  - **Dolby Atmos & Hi-Fi Audio**: Unlocked `support_dolby=true`, `support_hifi=true`, Game Turbo Voice Changer, 300% Volume Boost, and Bluetooth A2DP internal audio screen recording.
- **Camera Lag Fixed & Xiaomi Ultra AI Suite**:
  - Resolved stock viewfinder lag, enabled **Live Photos** (`ro.product.camera.livephoto.support=3`), Shutter Sound toggle (`ro.camera.sound.forced=0`), Focus Peaking, Object Tracking, and Audio Zoom.
  - Unlocked Gallery **AI Eraser 2.0, AI Image Expansion, Magic Sky, Ultra HDR Display**, and **AI Subtitles / Real-Time Voice Translation**.
- **System & Security Mods**:
  - **New UI Package Installer**: Redesigned package installer with patched private app permissions—eliminating the annoying **10-second MIUI Danger Warning Pop-up**.
  - **Dex2oat Speed Compilation & Log Disabler**: Compiled with `dalvik.vm.dex2oat-filter=speed` and stripped background modem/scout/dump logging for maximum battery life and instant touch response.

---

## 📂 Included Mod Kit Files in This Repository

| File / Path in Repository | Target Path in ROM | Description |
| :--- | :--- | :--- |
| `product/etc/build.prop` | `/product/etc/build.prop` | Master ProximaOS™ Xiaomi 15 Ultra Edition properties (`Computility=4`, Real Blur Everywhere, `OS3.0.306.0 \| ProximaOS™ \| Karan`). |
| `product/etc/device_features/beryl.xml` | `/product/etc/device_features/beryl.xml` | Unlocked Xiaomi Ultra features for `beryl` (AOD Always, Dolby Atmos, 120Hz Default, Display Expert Mode, AI Gallery). |
| `product/etc/device_features/citrine.xml` | `/product/etc/device_features/citrine.xml` | Unlocked Xiaomi Ultra features for `citrine` regional variant. |
| `product/overlay/SettingsResourceOverlay.apk` | `/product/overlay/SettingsResourceOverlay.apk` | Bold **PROXIMAOS** metallic vector logo overlay for the About Phone banner. |
| `system_ext/priv-app/Provision/Provision.apk` | `/system_ext/priv-app/Provision/Provision.apk` | Custom Setup Wizard with **Project ProximaOS** vector branding (Red-Orange `OS`). |
| `assets/ProximaOS_Bold_Logo.png` | Repository Banner / Asset | High-resolution transparent Bold PROXIMAOS wordmark. |
.

## ⚡ Installation Instructions (Fastboot)

1. Ensure your **Redmi Note 14 5G OR Poco M7 Pro 5G (`beryl` / `citrine`)** bootloader is unlocked.
2. Download the ProximaOS™ ROM archive from the [Releases](../../releases) page
3. Reboot device into Fastboot mode.
4. Flash the ROM (`fastboot flash super super.img`).
5. - fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img --slot all

- fastboot reboot recovery

                  →Wipe Data →

Back to Fastboot(most important)

- Fastboot -w

- fastboot erase frp
7. Reboot and enjoy **Project ProximaOS™**!

---

## ❤️ Credits & Maintainer
- **Lead Developer & Maintainer**: **Karan** (`Project ProximaOS™`)
- **Tools Used**: MT Manager, DNA Tool, KernelSU-Next
- **Special Thanks**: Xiaomi HyperOS Team, KernelSU-Next Developers, and all testers who supported this project!
