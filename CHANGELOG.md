================================================================================
 HUGO AI SUITE - CHANGELOG & UPDATE HISTORY
 Version: 6.3.70
 DEV by Hugo (telegram: @Hugo997911)
================================================================================

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

================================================================================
 DEV by Hugo (telegram: @Hugo997911)
================================================================================
