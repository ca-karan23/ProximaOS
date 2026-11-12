# ProximaOS
HyperOS based MOD ROM for xiaomi devices now for beryl
[readme.md](https://github.com/user-attachments/files/34739582/readme.md)
# 🌌 Project ProximaOS™ — Xiaomi 15 Ultra Edition (HyperOS 3)

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

---

## 🛠️ How to Upload Your 3.9 GB ROM to GitHub Releases

> **⚠️ Important GitHub Size Limit**:
> - **Git Repository (`git push`)**: Maximum **100 MB** per file (NEVER put the 3.9 GB `.zip` inside normal repo commits).
> - **GitHub Releases (Release Assets)**: Maximum **2.0 GB (2048 MB)** per individual uploaded file.
> - Because your ROM is **3.9 GB**, you have **2 easy options** to host it on GitHub:

### Option A: Upload Directly to GitHub Releases as a 2-Part Split Archive (100% Free & Fast Servers)
GitHub Releases allows unlimited files up to **2 GB each**. Splitting your 3.9 GB ROM into two `1.95 GB` parts lets you host it directly on GitHub's ultra-fast CDN:

**Using Termux / Linux / PC (7-Zip or `split`):**
```bash
# Method 1: Create a multi-volume 7z archive (1900 MB per part)
7z a -v1900m ProximaOS_beryl_OS3.0.306.0_By_Karan.7z ProximaOS_ROM.zip

# Method 2: Or split the flashable ZIP directly into 2 parts
split -b 1950M -d ProximaOS_ROM.zip ProximaOS_beryl_OS3.0.306.0.zip.part
```

**Or Using GitHub CLI (`gh`) to Create the Release & Upload Both Parts:**
```bash
gh release create v3.0.306.0 \
  ProximaOS_beryl_OS3.0.306.0.zip.part00 \
  ProximaOS_beryl_OS3.0.306.0.zip.part01 \
  --title "ProximaOS™ v3.0.306.0 | Xiaomi 15 Ultra Edition | Redmi Note 14 5G (beryl)" \
  --notes-file RELEASE_NOTES.md
```

### Option B: Single-File 3.9 GB Direct Download Mirror + GitHub Release Page
If you want users to download a **single unsplit 3.9 GB `.zip`**, upload the `.zip` to **SourceForge**, **PixelDrain**, or **GoFile**, and paste the direct download button inside your GitHub Release notes!

---

## ⚡ Installation Instructions (Fastboot / Recovery)

1. Ensure your **Redmi Note 14 5G (`beryl` / `citrine`)** bootloader is unlocked.
2. Download the ProximaOS™ ROM archive from the \[suspicious link removed\] page (if split into `.7z.001` & `.7z.002`, extract `.7z.001` using ZArchiver / MT Manager / 7-Zip to get the full ROM).
3. Reboot device into Fastboot / Recovery mode.
4. Flash the ROM script (`fastboot_first_install_with_data_format.bat` / `.sh`) or flash via custom recovery.
5. **Format Data (`Wipe Data`)** is mandatory on first install so all `persist.*` Computility 4 and Ultra Blur properties initialize cleanly.
6. Reboot and enjoy **Project ProximaOS™**!

---

## ❤️ Credits & Maintainer
- **Lead Developer & Maintainer**: **Karan** (`Project ProximaOS™`)
- **Tools Used**: MT Manager, DNA Tool, KernelSU-Next
- **Special Thanks**: Xiaomi HyperOS Team, KernelSU-Next Developers, and all testers who supported this project!
