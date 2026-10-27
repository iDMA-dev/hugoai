# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

## [v6.3.64] - 2026-10-27
### 1. Executable Standardization & NVIDIA Profile Persistence
- Standardized client executable to fixed name `HugoAI.exe` across dev and client distribution packages.
- Eliminates graphics setting resets in NVIDIA Control Panel (Power management, Ultra Low Latency, Max FPS persist across updates).
- Fixed desktop test directory to permanent path `Desktop\HugoAI\`.
### 2. Code Signing & Authenticode Timestamping
- Generated Hugo Development Team root code signing certificate (10-year validity: 2026-2036).
- Integrated DigiCert RFC 3161 TSA server (`http://timestamp.digicert.com`) for valid timestamp verification.
- Automatically signs `HugoAI.exe`, `hugo_recoil_worker.exe`, and `Hugo_Admin_Tool.exe`.
### 3. Stealth Security Setup & Tamper Protection Compatibility
- Relocated public root certificate to GitHub Cloud raw storage (`iDMA-dev/hugoai/main/HugoRootCA.cer`).
- Overhauled `Cho_Phep_Chay_HugoAI.bat` to download cert into %TEMP% on the fly and clean up immediately (zero `.cer` files left in folder).
- Built-in Windows 11 Tamper Protection fallback: auto-copies folder path to clipboard and launches Windows Security page in 1 click.
---
## [v6.3.63] - 2026-10-27
### 1. UI Reorganization & Streamlining (AIM & Settings Tabs)
- Reorganized AIM Assist menu into 6 clean, intuitive cards: Aim Assist, Aim Speed & Tracking, FOV Config, Target Selection, Recoil Compensation, and Advanced Expert Settings.
- Elevated Sticky Aim and Sticky Aim Threshold to Card 2 (Aim Speed & Tracking) for quick access during multi-target combat.
- Relocated Constant AI Tracking to Advanced Expert Settings to declutter primary controls.
- Removed redundant Third Person Support and Dynamic FOV options.
- Hid dev-only and debugging options in Settings (Data Collection, Auto Labeling, Debug Mode, Model Switch Keybind, Target Class, Mouse Background Effect).
### 2. Stability & Crash Prevention
- Fixed KeyNotFoundException crash on startup by adding defensive key lookup fallback in ATitle component.
- Standardized section titles across UI controls and minimized state configs.
### 3. Build & Packaging Hardening
- Permanently eliminated weapons_custom.json from client distribution packages.
- Ensured 100% clean client packages with zero pre-shipped licenses or local models.
---
## [v6.3.54] - 2026-10-25
### 1. Thong Bao Chi Tiet Cong Don Ngay Khi Gia Han Ban Quyen (Stacking Days)
- **Cai tien:**
  - Client C# (`HardwareAuthManager.cs`) tiep nhan va hien thi truc tiep thong bao chi tiet tu Cloudflare Auth Worker khi kich hoat / gia han Voucher Key.
  - Hien thi ro rang so ngay duoc cong them vao goi hien tai va han dung moi (vi du: `Gia han thanh cong! Da cong them 30 ngay vao goi RECOIL. Han dung moi: YYYY-MM-DD`).
- **Bao mat & Cloud-First:**
  - Hoan thien kien truc Pure Cloud-First: Khong luu file `.lic` tren dia, chi ghi nho ma key de tu dong dien khi mo lai trinh kich hoat.
---