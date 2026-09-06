# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

## [v6.3.28] - 2026-09-06
### 1. Kich Hoat Ban Quyen Online Qua Cloudflare Worker & Chu Ky So RSA-2048
  - Nang cap he thong xac thuc ban quyen: loai bo hoan toan khoa MASTER_KEY tinh khoi Client de tang cuong bao mat.
  - Xac thuc va ky so session token qua may chu serverless Cloudflare Workers su dung RSA-2048.
  - Client xac thuc chu ky so RSA doc lap khong can goi them thu vien ngoai (Zero Dependency).
### 2. Bat Buoc Co Ket Noi Internet Khi Kich Hoat Key (Cam Kich Hoat Khi Mat Mang)
  - Nguoi dung yeu cau: Khong cho phep kich hoat ban quyen khi mat mang / offline.
  - Khi nhap ma kich hoat moi (`HGMC-...` hoac `HGAI-...`), bat buoc Client phai co ket noi Internet de may chu Cloudflare Worker kiem tra va ky so.
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
## [v6.3.22] - 2026-09-06
### 1. Fix: Toggle Bật/Tắt Tự Động Bật Lại & Gán Phím Không Lưu (Triệt Tiêu Lỗi UTF-8 BOM & Race Condition)
  - Bấm tắt toggle Auto Loot, Prone Macro hoặc Custom Recoil trên App thì nút tự động nhảy ngược lại thành BẬT.
  - Gán phím tắt mới (như F6, L, các phím số...) không lưu được, bị nhảy ngược về phím mặc định (Caps Lock, V).
---
## [v6.3.21] - 2026-09-06
### 1. Fix: Nút Bật/Tắt Tính Năng Auto Loot, Prone Macro Trong App Bấm Tắt Bị Tự Động Bật Lại
### 2. Fix: Sau Khi Auto Loot Xong Vẫn Tự Click Chuột Bắn Súng
---
## [v6.3.18] - 2026-09-05
### 1. Fix: Bấm Phím Tab Không Kích Hoạt Quét (Chỉ Quét Được Khi Bấm Nút Quét Thử F5 Trên UI)
### 2. Fix: Nhận Diện Được Súng Nhưng Toàn Bộ Phụ Kiện (Tay Cầm, Đầu Nòng, Scope) Bị Mất Dấu
### 3. Cải Tiến: Mở Rộng Thẻ Hero Card Trên Giao Diện RecoilMenuControl Thành 5 Cột
---
## [v6.3.13] - 2026-09-05
### 1. Fix: Ứng Dụng Vẫn Chạy & Icon Vẫn Nằm Trên Thanh Taskbar Khi Tắt App
### 2. Fix: Chỉnh Sửa File `hugo_hotkeys.json` Nhưng Phím Bấm Không Thay Đổi Khi Vào Lại
---
## [v6.3.12] - 2026-09-05
### 1. Fix: Tâm Bắn Vọt Lên Trời Khi Bấm Bắn (Spray / Recoil)
### 2. Fix: Tâm Lắc Qua Lại Khá Mạnh Và Nhanh Quanh Người Địch
### 3. Fix: Tiến Trình `hugo_recoil_worker` Vẫn Chạy Ngầm Trong Task Manager Khi Thoát App
---
## [v6.3.6] - 2026-09-05
- Fix: Đồng bộ tư thế bắn STAND / CROUCH / PRONE lên HUD C# khi ngắm bắn.
- Tối ưu: Loại bỏ file debug symbol `.pdb` khỏi bản phân phối.