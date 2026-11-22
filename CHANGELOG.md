# Hugo AI Suite - Nhật Ký Cập Nhật (Changelog)
> **Phiên bản hiện tại:** `v6.3.89`  
> **Tác giả / Hỗ trợ:** DEV by Hugo (telegram: [@Hugo997911](https://t.me/Hugo997911))

---

## [v6.3.89] - 2026-11-22
### 1. Nâng Cấp Hệ Thống Tăng Tốc GPU Kép: NVIDIA CUDA / Tensor Core Boost & Smart DirectML Discrete Lock
- Bổ sung chế độ tăng tốc phần cứng **NVIDIA CUDA / Tensor Core Boost** (hỗ trợ đầy đủ GTX 16xx, RTX 20xx, RTX 30xx, RTX 40xx và RTX 50xx Blackwell) song song với **DirectML**: Cài đặt ngầm chỉ 1 lần duy nhất ngay trên giao diện, tự động giữ nguyên qua tất cả các bản cập nhật `HugoAI` về sau mà không làm tăng dung lượng tải App (~98 MB).
- Ứng dụng công nghệ **Hardware CUDA Graph** và bộ nhớ **Zero-Allocation Pinned IoBinding**: Gom toàn bộ 239 lớp mạng AI thành 1 lệnh GPU duy nhất, giảm tối đa độ trễ suy luận (nhanh hơn tới 46% ở khung 640px) đồng thời chống tranh chấp hàng đợi 3D khi PUBG chiếm 99% GPU trên màn hình 2K.
- Tối ưu hóa **DirectML Native** cho Card **AMD Radeon / Intel Arc & Laptop Gaming**: Tự động quét và khóa cứng vào Card đồ họa rời có VRAM lớn nhất (loại bỏ 100% lỗi chạy nhầm trên card tích hợp onboard iGPU) kèm cơ chế nạp nóng nhân GPU chống khựng khung hình đầu tiên.
- Tích hợp cơ chế **Auto Hardware Guard (3 mức bảo vệ 4GB / 6GB / 8GB+)** bảo vệ các dòng card đời cũ không bao giờ bị quá tải hoặc tràn VRAM, kèm thanh chuyển đổi nhanh **1-Click GPU Engine** ngay đầu thẻ `Aim Assist`.
- Bổ sung huy hiệu trạng thái **`AI AIM: ON / OFF`** hiển thị cố định, siêu gọn ngay bên phải thanh **In-Game HUD Overlay** (**Xanh lá** khi `ON`, **Đỏ** khi `OFF`, đồng bộ tức thì với phím tắt & công tắc giao diện) và khắc phục lỗi hiện đúp thông báo khi thu nhỏ cửa sổ cùng độ bền lưu cấu hình `Aim Assist` 100%.
---
## [v6.3.88] - 2026-11-21
### 1. Cập Nhật Nhanh Tại Chỗ (1-Click In-Place Update) & Nâng Cấp Key Combo Linh Hoạt
- Bổ sung tính năng **1-Click Update** ngay trên thanh Topbar và mục `About`: Tự động tải bản mới và cập nhật trực tiếp ngay tại thư mục đang sử dụng, giữ nguyên 100% cấu hình cá nhân, quyền loại trừ Windows Security và NVIDIA Profile, tự động dọn sạch file tạm sau khi khởi động lại.
- Tối giản và nâng cấp thẻ **License Center** (cùng nút lối tắt `+ KEY / COMBO` trên màn hình chính): Hợp nhất về 1 ô nhập Key thông minh duy nhất cho phép kích hoạt mới, nâng cấp lên gói **Combo VIP (`HGCB-...`)** hoặc cộng dồn ngày dùng bất cứ lúc nào ngay cả khi bản quyền hiện tại chưa hết hạn.
- Tự động đồng bộ ngầm bản quyền Cloud tức thì khi mở tab hoặc khi được gia hạn/nâng cấp từ xa mà không cần bấm nút thủ công hay khởi động lại ứng dụng.
## [v6.3.86] - 2026-11-13
### 1. Tối Ưu Hiệu Năng GPU Khi Giữ Ngắm & Lưu Cấu Hình Tự Động Tức Thì
- Tối ưu hóa hiệu năng xử lý GPU DirectML khi kích hoạt AI Aim + Auto Recoil (tự động tối ưu kích thước khung quét ngầm theo vùng FOV mà vẫn giữ 100% thanh trượt FOV Size tự do từng pixel, giảm đáng kể mức tải GPU và nhiệt độ).
- Lưu và khôi phục chính xác 100% trạng thái các tùy chọn (`Aim Assist`, `FOV`, `FOV Style`, `UI TopMost`, `StreamGuard`, `EMA Smoothening`, `Hotkeys`, `Sliders`) ngay khi thay đổi và sau khi khởi động lại ứng dụng.
- Bổ sung nút **RESET CUSTOM** trên thẻ Recoil và cơ chế nhận diện xóa `weapons_custom.json` thông minh để trả ngay về thông số Cloud chuẩn mặc định mà không bị tải lại bản cũ.

---

### Hướng Dẫn Cập Nhật Nhanh
1. Bấm nút **CẬP NHẬT** ngay trên thanh Topbar của ứng dụng (hoặc tải gói **`HugoAI_v6.3.89.zip`** bên dưới và giải nén ra thư mục trên máy tính).
2. Cắm thiết bị **Hugo Device** vào cổng USB, mở **`HugoAI.exe`** để sử dụng ngay.
- **Hỗ trợ trực tuyến 24/7:** DEV by Hugo (telegram: `@Hugo997911`)
