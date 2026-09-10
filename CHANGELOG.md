# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

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
## [v6.3.23] - 2026-09-06
### 1. Chuẩn Hóa 100% Tiếng Anh / Pure ASCII Không Dấu (Triệt Tiêu Hoàn Toàn Lỗi Định Dạng UTF-8 & Charmap Encode Crash)
  - Người dùng yêu cầu: *"Nếu hay bị 'Lỗi định dạng UTF-8' thì hãy chuyển thành ENG hoặc tiếng việt không dấu toàn bộ, sau này sẽ không bị lỗi nữa"*.
  - Trước đây khi chạy trên hệ điều hành Windows với bảng mã mặc định `cp1252`/`cp437`/`ANSI`, việc Python ghi log, in thông báo console, giải mã Named Pipe IPC hoặc lưu file cấu hình có chứa các ký tự Unicode tiếng Việt có dấu (như `Đã cập nhật`, `Lỗi định dạng`, `Bật`, `Tắt`, `❌`, `⚠️`) thường xuyên kích hoạt ngoại lệ `UnicodeEncodeError: 'charmap' codec can't encode character ...: character maps to <undefined>`.
  - Ngoại lệ này làm crash tiến trình nền Worker hoặc khiến lệnh `json.load()` thất bại rồi âm thầm fallback về giá trị mặc định.
---