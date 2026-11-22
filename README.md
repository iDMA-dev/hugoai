# Hugo AI Suite v6.3.89 - Hướng Dẫn Cài Đặt & Sử Dụng Từng Bước (Step-by-Step Guide)
> **Bản quyền / Tác giả:** DEV by Hugo (telegram: @Hugo997911)  
> **Chuyên mục:** AI AIM, Auto Recoil & Hỗ Trợ PUBG Chuyên Nghiệp

---

## BƯỚC 1: Tải Về, Giải Nén & Kết Nối Thiết Bị USB Hugo Device
1. **Yêu cầu hệ thống (System Requirements):**
   - **Hệ điều hành:** Windows 10 / Windows 11 (64-bit), máy tính có kết nối Internet ổn định.
   - **Zero Dependency:** Ứng dụng đã đóng gói sẵn toàn bộ thư viện `.NET 8` và lõi AI, mở lên chạy ngay không cần cài thêm phần mềm phụ.
2. **Giải nén phần mềm:**
   - Tải gói **`HugoAI_v6.3.89.zip`** và giải nén ra một thư mục riêng (ví dụ: `Desktop\HugoAI`). **Không chạy trực tiếp bên trong file nén `.zip`.**
3. **Cắm thiết bị phần cứng Hugo Device (BẮT BUỘC):**
   - Cắm thiết bị **Hugo Device** vào cổng USB máy tính **trước khi mở ứng dụng**.
   - Hệ thống tự động quét và nhận diện cổng USB COM tương thích (Auto COM Detection), điều khiển chuột 100% qua phần cứng cách ly độc lập, **0% can thiep bộ nhớ game**.
   - **Liên hệ mua thiết bị Hugo Device:** Chi phí từ **499k - 2.999k** (đã bao gồm bản quyền sử dụng) qua Telegram: [@Hugo997911](https://t.me/Hugo997911).

---

## BƯỚC 2: Chạy Cấp Quyền Windows Defender
> **Lưu ý:** Sau mỗi lần giải nén phiên bản mới ra thư mục mới bạn làm bước này 1 lần đầu tiên; các lần mở sau hoặc khi bấm nút **CẬP NHẬT** trực tiếp trên App thì không cần làm lại.

Để tránh Windows Defender nhận diện nhầm hoặc chặn file chạy:
1. Mở thư mục vừa giải nén, click chuột phải vào file **`Cho_Phep_Chay_HugoAI.bat`** và chọn **Run as administrator**.
2. Script sẽ tự động thêm thư mục `HugoAI` vào danh sách loại trừ (Exclusion) của Windows Defender.
   - *Lưu ý trên Windows 11:* Nếu đang bật *Tamper Protection*, script sẽ tự động copy sẵn đường dẫn thư mục vào Clipboard và mở cửa sổ Windows Security để bạn bấm `Add an exclusion -> Folder -> Paste (Ctrl + V)` chỉ trong 1 thao tác.

---

## BƯỚC 3: Khởi Chạy Ứng Dụng (`HugoAI.exe`) & Kích Hoạt Bản Quyền (License)
1. Mở file **`HugoAI.exe`** (ứng dụng tự động yêu cầu quyền **Administrator**).
2. Kích hoạt bản quyền trực tuyến (**Online Key**):
   - Tại màn hình chờ hoặc chuyển đến thẻ **License** trong ứng dụng.
   - Dán mã **Online Key** (Gói lẻ Recoil `HGMC-...`, AI Aim `HGAI-...` hoặc Gói **Combo VIP `HGCB-...`**) nhận từ Admin (`@Hugo997911`) vào ô nhập mã và bấm **Kích hoạt**.
   - Hệ thống tự động kích hoạt, cập nhật thời hạn (hoặc cộng dồn ngày sử dụng) ngay tức thì.

---

## BƯỚC 4: Mở Game PUBG & Cài Đặt Chuẩn Trong Game (BẮT BUỘC)
Để AI Vision nhận diện chuẩn xác 100% vũ khí/phụ kiện và quỹ đạo ghim tâm khớp tuyệt đối, bạn **bắt buộc** thiết lập trong game PUBG như sau:

### 4.1. Ngôn Ngữ Game & Chế Độ Màn Hình
- **Ngôn ngữ trong game (Language):** Chuyển sang **TIẾNG ANH (ENGLISH)** (`Settings -> Gameplay -> Language -> Language Selection -> English`).
- **Chế độ hiển thị (Display Mode):** Chọn **Borderless** (Không viền) hoặc **Windowed** (Cửa sổ). **Tuyệt đối không dùng Fullscreen.**

### 4.2. Bảng Thông Số Chuột Chuẩn Trong Game (`Settings -> Controls -> Main`)

| Thiết Lập In-Game (Setting) | Giá Trị Chuẩn (Value) | Ý Nghĩa / Ghi Chú (Description) |
| :--- | :--- | :--- |
| **Invert Mouse** | **Disable** | Tắt đảo ngược chuột |
| **General Sensitivity** | **30** | Độ nhạy chuột tổng thể trong game |
| **Vertical Sensitivity Multiplier** | **1** (hoặc 1.0) | Tỷ lệ nhạy dọc / ngang chuẩn |
| **Aim Sensitivity** | **30** | Độ nhạy ngắm qua vai (Aim) |
| **ADS Sensitivity** | **30** | **Cực kỳ quan trọng:** Độ nhạy ngắm bắn đầu ruồi / scope |
| **Universal Sensitivity for All Scopes** | **Enable** | Bật áp dụng chung cho tất cả các loại Scope |
| **Scoping Sensitivity** | **30** | Độ nhạy ống ngắm |

---

## BƯỚC 5: Bảng Phím Tắt Điều Khiển Trong Trận (In-Game Hotkeys)
Khi vào trận, bạn chỉ cần mở balo (**Phím Tab**) để AI tự động nhận diện súng/phụ kiện và sử dụng các phím tắt sau:

| Phím Tắt (Hotkey) | Chức Năng (Function) |
| :--- | :--- |
| **ALT + F12** | Bật / Tắt **Auto Recoil** (Ghim tâm tự động) |
| **Chuột Hông Trước (`XButton2` / Mouse 5)** | Bật / Tắt nhanh **AI AIM** trong trận (báo trạng thái Xanh lá / Đỏ trên HUD) |
| **HOME** | Ẩn / Hiện nhanh cửa sổ giao diện **HugoAI** xuống khay hệ thống (System Tray) |
| **Tab** | Tự động quét nhận diện súng và phụ kiện siêu tốc khi mở balo |
| **F5** | Quét balo thủ công (Force Full Scan) |
| **Caps Lock** | Bật / Tắt **Smart Auto Loot** (Nhặt đồ tự động qua Vision AI) |
| **V** | **Prone Macro** (Tự động nằm bắn - Drop Shot khi sấy, mặc định: OFF) |
| **Mũi tên Lên (Up)** | Tăng lực ghim dọc (Recoil Vertical +) khi bật Custom Recoil |
| **Mũi tên Xuống (Down)** | Giảm lực ghim dọc (Recoil Vertical -) khi bật Custom Recoil |
| **Mũi tên Trái / Phải** | Bù trừ độ giật ngang (Horizontal Recoil Bias Left/Right) |
| **ALT + F9** | Kết nối lại thiết bị phần cứng Hugo Device |
| **ALT + F10** | Nạp lại file cấu hình Hotkeys và Cloud Profile |
| **F11** | Bật / Tắt thanh giao diện **In-Game HUD Overlay** |
| **Shift + Esc** | Thoát nhanh khẩn cấp và đóng toàn bộ tiến trình ngầm (Panic Exit) |

---

## BƯỚC 6: Hướng Dẫn Tinh Chỉnh Thông Số Nâng Cao & Danh Sách Vũ Khí Hỗ Trợ

### 6.1. Các Thông Số Trong Hugo Recoil (Ghim Tâm Tự Động)
1. **Toggle Recoil (ALT + F12):** Bật/Tắt ghim tâm. Trên thanh HUD hiển thị đầy đủ tên súng, scope, phụ kiện, tư thế đứng/ngồi/nằm và huy hiệu **`AI AIM: ON`** (Xanh lá) / **`AI AIM: OFF`** (Đỏ) cố định rất dễ quan sát.
2. **Recoil Multiplier (Hệ số lực ghim - Mặc định `1.00`):**
   - **Số lớn hơn (`> 1.0`, ví dụ `1.05 - 1.20`):** Ghim **MẠNH HƠN** (chỉnh tăng khi đạn bay lên trên đầu mục tiêu).
   - **Số nhỏ hơn (`< 1.0`, ví dụ `0.85 - 0.95`):** Ghim **NHẸ LẠI** (chỉnh giảm khi tâm súng bị kéo chúi xuống đất).
3. **Custom Recoil:** Khi **ON** cho phép lưu lực ghim riêng cho từng súng trên máy cá nhân; bấm **RESET CUSTOM** nếu muốn trả ngay về thông số chuẩn mặc định từ Cloud.
4. **Human Jitter:** Mô phỏng dao động vi mô tự nhiên của tay người thật.
5. **Smart Auto Loot (Caps Lock) & Prone Macro (Phím V):** Hỗ trợ nhặt đồ siêu tốc và nằm bắn Drop Shot (Mặc định: OFF).

### 6.2. Các Thông Số Trong Hugo AI (AI Aim Assist & Target Tracking)
1. **Sticky Aim & Sticky Aim Threshold (`0 - 100 px`, Khuyên dùng `40 - 60 px`):**
   - Khóa chặt mục tiêu đang bắn, chống nhảy tâm khi có nhiều địch đứng gần nhau.
2. **Prediction Method - Hugo Zero-Lag Tracking (Khuyên dùng):**
   - **Base Lookahead (Mặc định `2.90`):** Hệ số bắn đón đầu theo thời gian đạn bay (`< 2.0` cho tầm gần, `> 3.5` cho tầm xa / sấy xe chạy ngang).
   - **Tracking Feedforward (Mặc định `1.00`):** Bù trễ vận tốc khung hình giúp tâm bám sát mục tiêu di chuyển ngang.
   - **Distance Adaptive Lead (Khuyên dùng `ON`):** Tự động tăng/giảm đón đầu theo khoảng cách xa/gần của địch.
3. **FOV Size (`10 - 640 px`):** Bán kính vùng quét quanh tâm (`100 - 200 px` bắn kín đáo legit; `300 - 500 px` quét rộng).
4. **Mouse Sensitivity (`0.01 - 1.00`):** Tốc độ kéo tâm của AI (`0.15 - 0.40` mượt tự nhiên; `0.70 - 0.90` bám nhanh).
5. **Y Offset (`-150` đến `+150 px`):** Kéo sang **TRÁI (số âm)** ưu tiên bắn lên **ĐẦU**; kéo sang **PHẢI (số dương)** bắn vào **NGỰC / THÂN**.
6. **X Offset (`-150` đến `+150 px`):** Chỉnh lệch tâm ngang Trái (số âm) / Phải (số dương).
7. **EMA Smoothening, Max AI FPS (`60 - 165 FPS`) & AI Minimum Confidence (Khuyên dùng `45% - 60%`).**

### 6.3. Danh Sách Các Loại Súng & Phụ Kiện Hỗ Trợ
| Nhóm Súng (Category) | Các Loại Súng Hỗ Trợ (Supported Weapons) |
| :--- | :--- |
| **AR Đạn 5.56mm** | M416, AUG, SCAR-L, QBZ, G36C, K2 |
| **AR Đạn 7.62mm** | Beryl M762, AKM, ACE32, GROZA |
| **SMG / CQC** | UZI, MP5K, VECTOR, P90, JS9, MP9, PP-19 Bizon, Tommy Gun, UMP45 |
| **DMR / LMG** | M249, DP-28, MG3, FAMAS, M16A4, Mk47 Mutant, RPD |
| **Ống Ngắm (Scopes)** | Red Dot, Holo, 2x, 3x, 4x, 6x, 8x, 15x (Tự động bù trừ lực giật riêng cho từng Scope) |
| **Phụ Kiện (Attachments)** | Tự động nhận diện Tay cầm (Vert, Angled, Half, Thumb, Light) & Đầu nòng (Comp, Flash, Brake, Supp) |

---

## BƯỚC 7: Chọn Công Nghệ GPU (DirectML vs NVIDIA CUDA) & Bảng Thông Số "Điểm Ngọt" (Sweet Spot)

### 7.1. Hướng Dẫn Chọn Chế Độ Tăng Tốc GPU (`Aim Assist` -> Thanh GPU Engine trên cùng)
- **DirectML (Mặc định - Chạy ngay 0MB tải thêm):** Tương thích 100% mọi dòng card **AMD Radeon**, **Intel Arc** và **NVIDIA**. Hệ thống tự động quét và khóa cứng vào Card đồ họa rời (không bao giờ chạy nhầm trên card onboard iGPU).
- **NVIDIA CUDA / Tensor Core Boost (Tùy chọn cài 1 lần duy nhất):** Dành riêng cho card **NVIDIA từ GTX 1650 / RTX 20-30-40-50 series trở lên**. Bấm nút **`CAI DAT CUDA BOOST`** ngay trên đầu thẻ `Aim Assist` để App tự tải ngầm bộ thư viện chính hãng Microsoft & NVIDIA (chỉ cài 1 lần duy nhất, giữ nguyên vĩnh viễn qua mọi bản cập nhật `HugoAI` về sau).
- **Cơ chế Auto-Guard bảo vệ Card đời cũ tự động:** Hệ thống tự nhận diện dung lượng VRAM (`4GB / 6GB / 8GB+`) để giới hạn bộ nhớ đệm và trần FPS an toàn, đảm bảo không bao giờ tràn VRAM hay gây giật lag PUBG.
- **Không xung đột DirectX trong game:** Việc để PUBG ở **`DirectX 11` hoặc `DirectX 11 Enhanced` + `Borderless`** là thiết lập mượt nhất và hoạt động độc lập 100%, không hề xung đột với `DirectML (DX12)` hay `NVIDIA CUDA` của HugoAI.

### 7.2. Bảng Thông Số "Điểm Ngọt" (Sweet Spot) Tối Ưu Theo Hãng Card & Cấu Hình
> **Nguyên tắc vàng:** `Max AI FPS` (trong *Aim Assist -> Advanced Expert Settings*) nên đặt bằng khoảng **70% - 85% FPS trung bình của PUBG** trong giao tranh (không cần đặt cao hơn FPS thực tế của game).

| Hãng Card & Cấu Hình GPU | Nên Chọn Engine Nào? | Mức `Max AI FPS` Tối Ưu | Ghi Chú & Lý Do Thực Chiến |
| :--- | :---: | :---: | :--- |
| **AMD Radeon (4GB VRAM)**<br>*(RX 570, RX 580 4GB, RX 6500 XT)* | **DirectML** *(Chuẩn số 1 cho AMD)* | **`60 FPS`** *(Mặc định)* | Nhẹ card, giữ ổn định khung hình PUBG, không lo tràn VRAM. |
| **AMD Radeon (8GB - 16GB+ VRAM)**<br>*(RX 580 8G, RX 6600/6700 XT, RX 7600/7800 XT)* | **DirectML** *(Chuẩn số 1 cho AMD)* | **`85 - 105 FPS`** | Kiến trúc RDNA của AMD tối ưu cực mạnh cho DirectML trên Windows, bám tâm rất mượt. |
| **Intel Arc GPU**<br>*(Arc A380, A580, A750, A770, B580)* | **DirectML** | **`60 - 85 FPS`** | Tương thích native tốt nhất cho dòng card Intel Arc. |
| **NVIDIA Đời Cũ GTX 10-Series**<br>*(GTX 1050 Ti, GTX 1060, GTX 1070, GTX 1080)* | **DirectML** *(Auto Eco Guard)* | **`60 FPS`** | Dòng 10-series không có nhân Tensor Core; dùng DirectML nhẹ máy và ổn định nhất. |
| **NVIDIA 4GB VRAM (Turing / RTX Laptop)**<br>*(GTX 1650 4GB, RTX 2050 / RTX 3050 4GB)* | **DirectML** hoặc **NVIDIA CUDA** *(Eco 4GB)* | **`60 FPS`** | Auto-Guard tự bóp trần VRAM 320MB & <= 65 FPS để nhường VRAM cho PUBG. |
| **NVIDIA 6GB VRAM Tầm Trung**<br>*(GTX 1660 Super/Ti, RTX 2060 6GB, RTX 3060 Laptop 6GB)* | **NVIDIA CUDA Boost** *(Khuyên dùng)* | **`80 - 90 FPS`** | Giảm độ trễ bám mục tiêu ~35% so với DirectML mà vẫn giữ an toàn VRAM 6GB. |
| **NVIDIA RTX 8GB - 24GB+ Đời Mới**<br>*(RTX 3060 12G, RTX 3070, RTX 4060/4070, **RTX 5060 Ti / 5070 / 5080**)* | **NVIDIA CUDA Boost** *(Tối ưu nhất)* | **`105 - 120 FPS`** | **Điểm ngọt đỉnh cao!** Phát huy 100% nhân Tensor Core + CUDA Graph (~1.4 - 2.2ms/frame), sấy xe và mục tiêu di chuyển ngang cực dính trên màn 144Hz - 240Hz. |

### 7.3. Tối Ưu NVIDIA Control Panel & Liên Hệ Hỗ Trợ (Support)
- **Tối ưu NVIDIA & PUBG:**
  - **Low Latency Mode:** Chọn **Ultra** trong NVIDIA Control Panel.
  - **Power Management Mode:** Chọn **Prefer maximum performance**.
  - **DirectX trong PUBG:** Chọn **DirectX 11** hoặc **DirectX 11 Enhanced**; **Display Mode:** **Borderless**; **V-Sync:** **Disable**.
- **Thông tin liên hệ & Hỗ trợ chính thức:**
  - **Developer:** Hugo
  - **Telegram Support:** [@Hugo997911](https://t.me/Hugo997911)
  - **Copyright:** DEV by Hugo (telegram: @Hugo997911)
