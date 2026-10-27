# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

## [v6.3.70] - 2026-10-27
### 1. Khac Phuc Triet De Loi Phim Tat Toggle Recoil (ALT + F12)
- Loai bo hook trung lap trong `setup_keyboard_hooks()`, giu duy nhat co che debounced polling ben trong luong `input_listener_worker`.
- Bấm 1 lần bat/tat on dinh 100% giua ON va PAUSED, khong con bi tinh trang nhay 2 lan lien tiep gay ra hien tuong "bam cai toan ON".
### 2. Toi Uu Sieu Toc Do Quet Balo (Tab) Nhan Dien Sung & Phu Kien
- Khoi phuc thuat toan OpenCV matchTemplate toan cuc de tim diem so cao nhat tren tung danh muc, triet tieu 100% tinh trang nhan nham sung hay phu kien.
- Ha thoi gian delay mo balo Tab xuong 160ms (vua khop thoi diem ket thuc hoat anh mo balo trong PUBG).
- Co che Smart Burst Cap: Khi da tim thay sung va nhan dien xong cac phu kien dang co, chi duy tri toi da 100ms de xac nhan cac o phu kien trong (thay vi bat nguoi dung cho het timeout 500ms nhu ban cu).
- Tong thoi gian quet balo giam tu ~720ms xuong con ~180ms - 260ms (nhanh gap gan 3 lan).
### 3. Dieu Chinh Mac Dinh Prone Macro ve OFF
- Toan bo he thong (C# Host, Python Daemon, file cau hinh mac dinh `hugo_hotkeys.json`) duoc dong bo de tinh nang Prone Macro (Drop Shot) mac dinh la OFF, nguoi dung chu dong bat khi can.
### 4. Cap Nhat Huong Dan Su Dung & Thiet Lap In-Game PUBG Chuan Xac
- Bo sung huong dan chi tiet cach tinh toan cac thong so thanh truot (Y Offset, X Offset, FOV, Kalman Lead Time, Recoil Multiplier) giup nguoi dung de dang can chinh.
- Tich hop bang thong so cai dat chuot Ingame PUBG chuan xac (Sens 30, ADS 30, Vert Mult 1.0, Universal Scopes Enable).
- Bo sung khuyen nghi bat buoc cai dat ngon ngu game PUBG sang TIENG ANH (ENGLISH) de AI Vision dat do chinh xac 100%.
---
## [v6.3.66] - 2026-10-27
### 1. Canh Bao Ngat Ket Noi Thiet Bi Hugo Device & Tu Dong Phuc Hoi (Issue 1 Fixed)
- Phat trien co che giam sat phan cung thoi gian thuc (Real-time Hardware Watchdog) hoat dong song song o ca 2 lop: C# Client (<2s) va Python Recoil Worker Daemon (<1s).
- Khi nguoi dung rut thiet bi Hugo Device khoi cong USB trong luc ung dung dang chay:
  - Tuyen trinh ban va di chuyen chuot lap tuc dung an toan de tranh xung dot hoac lag lenh.
  - Tu dong xoa tep phien lam viec cu `hugo_device_session.json` de khong bi treo trang thai gia lap.
  - Phat canh bao noi bat ngay lap tuc tren HUD in-game de nguoi dung nhan biet: `[ CANH BAO: MAT KET NOI HUGO DEVICE! VUI LONG CAM LAI USB ]`.
  - Hien thi thong bao Warning NoticeBar tren man hinh Desktop: `CANH BAO: Thiet bi Hugo Device da bi ngat ket noi khoi cong USB!`.
- Co che Tu dong nhan dien va ket noi lai (Zero-Click Auto Reconnect):
  - Khi nguoi dung cam lai Hugo Device vao bat ky cong USB nao, he thong tu dong do tim, xac thuc chu ky phan cung va ket noi lai ngay lap tuc.
  - Tu dong phuc hoi tinh nang Recoil va AI Aim ma nguoi dung KHONG can khoi dong lai ung dung hoac an to hop phim Alt+F9.
  - Hien thi thong bao thanh cong tren ca HUD va NoticeBar: `[ DA KET NOI LAI HUGO DEVICE THANH CONG! ]`.
### 2. Nang Cap Giao Dien Canh Bao Khi Chua Cam Thiet Bi Luc Khoi Chay (Issue 2 Fixed)
- Dai tu toan dien giao dien `LicenseWindow`:
  - Loai bo hoan toan tinh trang roi mat do hien thi qua nhieu o nhap ma key, huy hieu trang thai "Chua kich hoat" gay hoang mang cho nguoi dung khi chua cam thiet bi.
  - Khi chua cam Hugo Device: Tu dong an toan bo cac o nhap lieu phuc tap, thay the bang Khung Thong Bao Canh Bao Chuyen Biet (Dedicated Hardware Missing Alert Panel) voi vien do noi bat.
  - Tieu de canh bao ro rang: `[!] CHUA KET NOI THIET BI HUGO DEVICE`.
  - Huong dan ket noi 3 buoc ro rang, de hieu (cam truc tiep cong USB tren mainboard, he thong tu dong nhan dien khong can mo lai ung dung).
  - Trinh trang thai quey dang cho: `[ DANG CHO KET NOI CONG USB COM... ]` va badge `[ CHUA KET NOI USB ]`.
  - Nut vao ung dung chuyen trang thai `CHO KET NOI USB...` de nguoi dung hieu ro ly do chua the vao app.
- Tu dong chuyen doi giao dien tuc thi:
  - Ngay khi nguoi dung cam Hugo Device vao may, giao dien tu dong mo cac o ban quyen hoac mo nut `VAO UNG DUNG` neu may da co ban quyen hop le.
---
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