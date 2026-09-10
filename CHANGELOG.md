# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

## [v6.3.33] - 2026-09-10
### 1. Luu Toa Do Recoil HUD Khi Di Chuyen Va Dong/Mo Ung Dung
  - Nguoi dung di chuyen HUD Recoil toi vi tri mong muon tren man hinh, bam nut Khoa HUD roi thoat ung dung.
  - Khi mo lai ung dung, vi tri HUD Recoil bi reset ve giua man hinh (770, 940).
### 3. Dong Bo Cloud Profile Khi Nang Cap Version Moi
  - Khi nang cap len version moi, ung dung hien thi thong so factory default thay vi phuc hoi profile da luu tren GitHub cloud.
---
## [v6.3.30] - 2026-09-08
### 1. Bao Mat Chong Crack Va Xac Thuc Phan Cung Arduino (Hardware Handshake Guard)
  - Tang cuong bao mat chong crack: ngan chan cac tool/script ben ngoai tu y ket noi vao cong COM de dieu khien chuot Arduino.
  - Loai bo cac nguy co crash/bypass khi xay ra ngoai le khoi dong ung dung C#.
### 2. An Toan Bo Link Tai Nguyen Qua Cloudflare Worker Proxy (Zero Source Link Leak)
  - Khong de lo link raw GitHub / Gist / Webhook ben trong ma nguon va file thuc thi client.
  - Ho tro chuyen repository thanh Private ma khong lam gian doan qua trinh tai Model AI, Config hay Templates.
---
## [v6.3.28] - 2026-09-06
### 1. Kich Hoat Ban Quyen Online Qua Hugo AI Worker & Chu Ky So RSA-2048
  - Nang cap he thong xac thuc ban quyen: loai bo hoan toan khoa MASTER_KEY tinh khoi Client de tang cuong bao mat.
  - Xac thuc va ky so session token qua may chu serverless Hugo AI Worker su dung RSA-2048.
  - Client xac thuc chu ky so RSA doc lap khong can goi them thu vien ngoai (Zero Dependency).
### 2. Bat Buoc Co Ket Noi Internet Khi Kich Hoat Key (Cam Kich Hoat Khi Mat Mang)
  - Nguoi dung yeu cau: Khong cho phep kich hoat ban quyen khi mat mang / offline.
  - Khi nhap ma kich hoat moi (`HGMC-...` hoac `HGAI-...`), bat buoc Client phai co ket noi Internet de may chu Hugo AI Worker kiem tra va ky so.
---
### 1. Ẩn/Hiện Động Dòng Hướng Dẫn Tùy Chỉnh Lực (Custom Recoil Hint Visibility)
  - Dòng chữ vàng `💡 Ingame: Mũi tên ↑ / ↓ để chỉnh lực (khi bật Custom)` trên thẻ `CLOUD PROFILE` trước đây luôn hiển thị mặc định, ngay cả khi người dùng đang dùng Master Cloud Profile và chưa từng chỉnh lực súng.
  - Người dùng yêu cầu dòng chữ này chỉ được phép hiển thị khi người dùng đang bật Custom Recoil hoặc đã có tùy chỉnh lực trong file `weapons_custom.json`.