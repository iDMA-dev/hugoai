# Hugo AI Suite - Nhật Ký Cập Nhật (Changelog)
> **Phiên bản hiện tại:** `v6.3.91`  
> **Tác giả / Hỗ trợ:** DEV by Hugo (telegram: [@Hugo997911](https://t.me/Hugo997911))

---

## [v6.3.91] - 2026-11-23
### 1. Giao Diện Luxury Gold Mới, Cập Nhật An Toàn & Trạng Thái AI Thực Tế
- Ra mắt diện mạo **Luxury Gold** sang trọng, độ tương phản cao và dịu mắt khi sử dụng lâu dài trên toàn bộ cửa sổ chính, bảng điều khiển **Auto Recoil**, **AI Aim Assist**, **License Center**, **In-Game HUD Overlay** và vòng tâm **FOV**.
- Nâng cấp trình **1-Click Update** tích hợp kiểm định toàn vẹn gói cài đặt `SHA-256` trước khi giải nén và cổng thông báo cập nhật phiên bản bắt buộc thông minh, đảm bảo mọi thiết bị luôn đồng bộ cấu hình chuẩn xác nhất mà không làm gián đoạn cài đặt cá nhân.
- Hoàn thiện hiển thị trạng thái sẵn sàng thực tế của mô hình AI/GPU ngay trên thanh **Sidebar** (phân biệt rõ đang khởi tạo, sẵn sàng hoạt động hoặc cảnh báo lỗi nạp nhân GPU khi chạy gói **Combo VIP**).
- Nâng cấp đồng bộ **Cloud Profile** đa máy tính (Máy A <-> Máy B): Luôn ưu tiên nạp cấu hình mới nhất trên Cloud không phụ thuộc độ lệch giờ đồng hồ Windows, loại bỏ hoàn toàn lỗi cấu hình cũ ghi đè ngược lên Cloud và tự động đồng bộ ngầm ngay khi tinh chỉnh lực kéo súng trong game.
## [v6.3.90] - 2026-11-22
### 1. Tối Ưu Hóa Đồng Bộ Đám Mây, In-Game HUD Overlay & Độ Ổn Định Kết Nối
- Nâng cấp độ ổn định kết nối với cụm máy chủ Cloud chính & dự phòng, tối ưu tốc độ xác thực bản quyền và tự động đồng bộ thông số ghim tâm mới nhất tức thì khi khởi động.
- Hoàn thiện huy hiệu trạng thái **`AI AIM: ON / OFF`** trực quan trên thanh **In-Game HUD Overlay** (**Xanh lá** / **Đỏ**) cùng cơ chế lưu trữ bền vững 100% thiết lập cá nhân (`Aim Assist`, `Custom Recoil`, `Hotkeys`, `GPU Engine`) qua mọi lần cập nhật.
- Cải thiện cơ chế gửi báo cáo chẩn đoán thông minh khi đóng ứng dụng, giúp đội ngũ kỹ thuật hỗ trợ xử lý sự cố nhanh chóng hơn mà không gây gián đoạn trải nghiệm chơi game.
## [v6.3.89] - 2026-11-22
### 1. Nâng Cấp Hệ Thống Tăng Tốc GPU Kép: NVIDIA CUDA / Tensor Core Boost & Smart DirectML Discrete Lock
- Bổ sung chế độ tăng tốc phần cứng **NVIDIA CUDA / Tensor Core Boost** (hỗ trợ đầy đủ GTX 16xx, RTX 20xx, RTX 30xx, RTX 40xx và RTX 50xx Blackwell) song song với **DirectML**: Cài đặt ngầm chỉ 1 lần duy nhất ngay trên giao diện, tự động giữ nguyên qua tất cả các bản cập nhật `HugoAI` về sau mà không làm tăng dung lượng tải App (~98 MB).
- Ứng dụng công nghệ **Hardware CUDA Graph** và bộ nhớ **Zero-Allocation Pinned IoBinding**: Gom toàn bộ 239 lớp mạng AI thành 1 lệnh GPU duy nhất, giảm tối đa độ trễ suy luận (nhanh hơn tới 46% ở khung 640px) đồng thời chống tranh chấp hàng đợi 3D khi PUBG chiếm 99% GPU trên màn hình 2K.
- Tối ưu hóa **DirectML Native** cho Card **AMD Radeon / Intel Arc & Laptop Gaming**: Tự động quét và khóa cứng vào Card đồ họa rời có VRAM lớn nhất (loại bỏ 100% lỗi chạy nhầm trên card tích hợp onboard iGPU) kèm cơ chế nạp nóng nhân GPU chống khựng khung hình đầu tiên.
- Tích hợp cơ chế **Auto Hardware Guard (3 mức bảo vệ 4GB / 6GB / 8GB+)** bảo vệ các dòng card đời cũ không bao giờ bị quá tải hoặc tràn VRAM, kèm thanh chuyển đổi nhanh **1-Click GPU Engine** ngay đầu thẻ `Aim Assist`.
- Bổ sung huy hiệu trạng thái **`AI AIM: ON / OFF`** hiển thị cố định, siêu gọn ngay bên phải thanh **In-Game HUD Overlay** (**Xanh lá** khi `ON`, **Đỏ** khi `OFF`, đồng bộ tức thì với phím tắt & công tắc giao diện) và khắc phục lỗi hiện đúp thông báo khi thu nhỏ cửa sổ cùng độ bền lưu cấu hình `Aim Assist` 100%.
---

---

### Hướng Dẫn Cập Nhật Nhanh
1. Bấm nút **CẬP NHẬT** ngay trên thanh Topbar của ứng dụng (hoặc tải gói **`HugoAI_v6.3.91.zip`** bên dưới và giải nén ra thư mục trên máy tính).
2. Cắm thiết bị **Hugo Device** vào cổng USB, mở **`HugoAI.exe`** để sử dụng ngay.
- **Hỗ trợ trực tuyến 24/7:** DEV by Hugo (telegram: `@Hugo997911`)
