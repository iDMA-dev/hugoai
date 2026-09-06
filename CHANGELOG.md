================================================================================
 HUGO AI SUITE - CHANGELOG & UPDATE HISTORY
 Version: 6.3.24
 DEV by Hugo (telegram: @Hugo997911)
================================================================================

## [v6.3.24] - 2026-09-06

### 1. Ẩn/Hiện Động Dòng Hướng Dẫn Tùy Chỉnh Lực (Custom Recoil Hint Visibility)
- **Yêu cầu & Triệu chứng:**
  - Dòng chữ vàng `💡 Ingame: Mũi tên ↑ / ↓ để chỉnh lực (khi bật Custom)` trên thẻ `CLOUD PROFILE` trước đây luôn hiển thị mặc định, ngay cả khi người dùng đang dùng Master Cloud Profile và chưa từng chỉnh lực súng.
  - Người dùng yêu cầu dòng chữ này chỉ được phép hiển thị khi người dùng đang bật Custom Recoil hoặc đã có tùy chỉnh lực trong file `weapons_custom.json`.
- **Giải pháp:**
  - Trong `RecoilMenuControl.xaml`: Đặt định danh `x:Name="lblCustomRecoilHint"` và mặc định ẩn `Visibility="Collapsed"`.
  - Trong `RecoilMenuControl.xaml.cs`: Trong hàm `UpdateStateUI()`, kiểm tra điều kiện kích hoạt:
    - Nếu `RecoilEngineManager.IsCustomRecoilEnabled == true` hoặc `ConfigMode` chứa `"CUSTOM"`, hoặc phát hiện file `weapons_custom.json` có chứa dữ liệu lực (`HasCustomRecoilAdjustments()`) -> hiển thị (`Visibility.Visible`).
    - Ngược lại (mặc định) -> ẩn hoàn toàn (`Visibility.Collapsed`).

### 2. Khôi Phục Cơ Chế Gửi Báo Cáo Khi Thoát/Tắt App (Discord Webhook Exit Report)
- **Yêu cầu & Triệu chứng:**
  - Khôi phục tính năng gửi báo cáo khi người dùng tắt/thoát ứng dụng (như cơ chế trong Hugo Aiding cũ).
  - Bổ sung các thông tin chi tiết vào tin nhắn báo cáo:
    - `UUID`: UUID người dùng.
    - `License Hugo Recoil`: Hạn đến ngày bao nhiêu (còn bao nhiêu ngày nữa cần gia hạn).
    - `License Hugo AI Assist`: Hạn đến ngày bao nhiêu (còn bao nhiêu ngày nữa cần gia hạn).
- **Giải pháp:**
  - Tạo lớp `ExitReportManager.cs` trong C# WPF để thu thập toàn bộ thông tin phiên chơi:
    - UUID / HWID từ `HardwareAuthManager.CurrentHardwareUUID` (fallback qua Windows `MachineGuid`).
    - Thời gian phiên chơi online (`Online: HH:MM:SS`).
    - Tính toán chính xác thời hạn bản quyền và số ngày còn lại cần gia hạn của cả Hugo Recoil và Hugo AI Assist.
    - Phân tích log lỗi cuối cùng (`log.txt` / `hugo_ai_debug.log`).
    - Tự động đính kèm file `custom_{hwid}.json` qua multipart request nếu phát hiện file `weapons_custom.json` có tùy chỉnh.
    - Gửi ngầm tới Discord Webhook (`https://discord.com/api/webhooks/1481532663801057421/...`) của Hugo Support Bot.
  - Tích hợp vào `PerformFastExit()` trong `MainWindow.xaml.cs` và `OnExit()` trong `App.xaml.cs`. Giao diện ẩn ngay lập tức (`Hide()`) để người dùng không bị trễ, tiến trình gửi ngầm với timeout 2.5s an toàn tuyệt đối.
  - Toàn bộ chuỗi dữ liệu tuân thủ chuẩn 100% Pure 7-bit ASCII không dấu.

================================================================================
 DEV by Hugo (telegram: @Hugo997911)
================================================================================
