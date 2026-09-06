# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

## [v6.3.24] - 2026-09-06
### 1. Ẩn/Hiện Động Dòng Hướng Dẫn Tùy Chỉnh Lực (Custom Recoil Hint Visibility)
  - Dòng chữ vàng `💡 Ingame: Mũi tên ↑ / ↓ để chỉnh lực (khi bật Custom)` trên thẻ `CLOUD PROFILE` trước đây luôn hiển thị mặc định, ngay cả khi người dùng đang dùng Master Cloud Profile và chưa từng chỉnh lực súng.
  - Người dùng yêu cầu dòng chữ này chỉ được phép hiển thị khi người dùng đang bật Custom Recoil hoặc đã có tùy chỉnh lực trong file `weapons_custom.json`.
### 2. Khôi Phục Cơ Chế Gửi Báo Cáo Khi Thoát/Tắt App (Discord Webhook Exit Report)
  - Khôi phục tính năng gửi báo cáo khi người dùng tắt/thoát ứng dụng (như cơ chế trong Hugo Aiding cũ).
  - Bổ sung các thông tin chi tiết vào tin nhắn báo cáo:
    - `UUID`: UUID người dùng.
    - `License Hugo Recoil`: Hạn đến ngày bao nhiêu (còn bao nhiêu ngày nữa cần gia hạn).
    - `License Hugo AI Assist`: Hạn đến ngày bao nhiêu (còn bao nhiêu ngày nữa cần gia hạn).
---
## [v6.3.23] - 2026-09-06
### 1. Chuẩn Hóa 100% Tiếng Anh / Pure ASCII Không Dấu (Triệt Tiêu Hoàn Toàn Lỗi Định Dạng UTF-8 & Charmap Encode Crash)
  - Người dùng yêu cầu: *"Nếu hay bị 'Lỗi định dạng UTF-8' thì hãy chuyển thành ENG hoặc tiếng việt không dấu toàn bộ, sau này sẽ không bị lỗi nữa"*.
  - Trước đây khi chạy trên hệ điều hành Windows với bảng mã mặc định `cp1252`/`cp437`/`ANSI`, việc Python ghi log, in thông báo console, giải mã Named Pipe IPC hoặc lưu file cấu hình có chứa các ký tự Unicode tiếng Việt có dấu (như `Đã cập nhật`, `Lỗi định dạng`, `Bật`, `Tắt`, `❌`, `⚠️`) thường xuyên kích hoạt ngoại lệ `UnicodeEncodeError: 'charmap' codec can't encode character ...: character maps to <undefined>`.
  - Ngoại lệ này làm crash tiến trình nền Worker hoặc khiến lệnh `json.load()` thất bại rồi âm thầm fallback về giá trị mặc định.
---
## [v6.3.22] - 2026-09-06
### 1. Fix: Toggle Bật/Tắt Tự Động Bật Lại & Gán Phím Không Lưu (Triệt Tiêu Lỗi UTF-8 BOM & Race Condition)
- **Triệu chứng:**
  - Bấm tắt toggle Auto Loot, Prone Macro hoặc Custom Recoil trên App thì nút tự động nhảy ngược lại thành BẬT.
  - Gán phím tắt mới (như F6, L, các phím số...) không lưu được, bị nhảy ngược về phím mặc định (Caps Lock, V).
- **Nguyên nhân cốt lõi (Root Cause):**
  1. **Lỗi UTF-8 BOM từ C#:**
     - Khi C# gọi `SaveHotkeysToDisk()`, hàm `File.WriteAllText(mainPath, json, Encoding.UTF8)` mặc định ghi kèm tiền tố Byte Order Mark (BOM: `\xEF\xBB\xBF`).
     - Khi Python Worker (`core/utils.py` và `recoil_worker_daemon.py`) mở file hotkeys bằng `open(..., 'r', encoding='utf-8')`, `json.load()` gặp lỗi nghiêm trọng: `JSONDecodeError: Unexpected UTF-8 BOM (decode using utf-8-sig): line 1 column 1`.
     - Khối `except Exception:` trong Python đã bắt ngoại lệ này và **âm thầm khôi phục toàn bộ về `DEFAULT_HOTKEYS`** (`auto_loot_enabled: True`, `prone_macro_enabled: True`, `auto_loot: "caps lock"`).
     - Ngay sau đó, Python gửi gói tin `status` chứa các giá trị mặc định này ngược sang C#, khiến C# lập tức ghi đè toggle thành "BẬT" và phím thành "CAPS LOCK".
  2. **Xung đột gói tin trễ (Race Condition Echo):**
     - Khi người dùng bấm toggle hoặc gán phím, nếu luồng socket IPC nhận được một gói tin `status` hoặc `weapon_changed` đang xếp hàng từ trước, C# nhận gói tin cũ và ghi đè trạng thái UI trước khi lệnh mới kịp phản hồi.
  3. **Thiếu cập nhật `mtime` trong lệnh `set_hotkey`:**
     - Sau khi lưu phím qua IPC `set_hotkey`, worker không cập nhật `active_hotkeys_mtime`, khiến luồng polling nền phát hiện sai là file bị sửa đổi từ bên ngoài.
  4. **Ánh xạ phím số (Number keys & Numpad):**
     - Các phím số `Key.D0`..`Key.D9` và `Key.NumPad0`..`Key.NumPad9` trong WPF trả về `"d1"`, `"numpad1"`, thiếu ánh xạ sang mã VK tương ứng trong bảng hook của Python.
---