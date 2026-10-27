# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

## [v6.3.65] - 2026-10-27
### 1. Multi-Worker High Availability & Auto-Failover
- Implemented robust multi-endpoint failover architecture across all Hugo AI network layers (C# Client and Python Daemon).
- Configured 4 active endpoints in strict priority order:
  1. Primary: https://hugo-ai-pubg-auth.team-idma-dev.workers.dev
  2. Custom Domain 1: https://hugoai.idma.dev (Anti-ISP block, fast Anycast routing)
  3. Secondary Backup: https://hugo-ai-pubg-auth-backup.gafaba.workers.dev
  4. Custom Domain 2: https://hugoai.gafaba.com (Multi-TLD domain redundancy)
- Sub-second automatic fallback on HTTP 429 (Rate Limit), 5xx server errors, network timeouts, or ISP DNS blockades.
- Self-healing promotion: active/healthy endpoint is automatically promoted to primary for subsequent requests.
### 2. Anti-Censorship & Custom Domain Integration
- Completely eliminates connection errors caused by Vietnamese ISP SNI/DNS filtering on default *.workers.dev domains.
- Integrated dual custom domains (.idma.dev and .gafaba.com) with active SSL certificates and verified RSA license validation.
### 3. Dynamic Configuration via hugo_auth.json
- Added support for backup_worker_urls in hugo_auth.json across workspace, C# project, build artifacts, and client folders.
- Allows updating and adding backup servers remotely without requiring client executable re-compilation.
### 4. Process Cloaking & Authenticode Signature Verification
- Validated standardized HugoAI.exe and background worker bin\\engine\\HugoCore.exe signatures.
- Verified DigiCert RFC 3161 SHA256 Timestamp with Status: Valid across all binaries.
- Provided automated 1-click installer Cho_Phep_Chay_HugoAI.bat with Windows 11 Tamper Protection fallback.
---
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
### 4. Background Process Cloaking (HugoCore.exe)
- Renamed standalone background recoil engine executable from `hugo_recoil_worker.exe` to `HugoCore.exe`.
- Completely conceals recoil functionality in Task Manager, process listing, and anti-cheat scanners (BattlEye / ACE / Vanguard).
- Automatically signed with Authenticode + DigiCert RFC 3161 timestamp.
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