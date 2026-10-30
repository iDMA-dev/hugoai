# Hugo AI Suite v6.3.76 - Huong Dan Cai Dat & Su Dung Tung Buoc (Step-by-Step Guide)
> **Ban quyen / Author:** DEV by Hugo (telegram: @Hugo997911)  
> **Chuyen muc:** AI AIM, Auto Recoil & Ho tro PUBG Chuyen Nghiep

---

## BUOC 1: Tai Ve, Giai Nen & Ket Noi Thiet Bi USB Hugo Device
1. **Yeu cau he thong (System Requirements):**
   - **He dieu hanh:** Windows 10 / Windows 11 (64-bit), may tinh co ket noi Internet on dinh.
   - **Zero Dependency:** Ung dung da dong goi san toan bo thu vien .NET 8 va AI, khong can cai them moi truong phu.
2. **Giai nen phan mem:**
   - Tai goi **`HugoAI_v6.3.76.zip`** va giai nen ra mot thu muc rieng (vi du: `Desktop\HugoAI`). Khong chay truc tiep ben trong file nen `.zip`.
3. **Cam thiet bi phan cung Hugo Device (BAT BUOC):**
   - Cam thiet bi **Hugo Device** vao cong USB may tinh **truoc khi mo ung dung**.
   - He thong se tu dong quet va nhan dien cong USB COM tuong thich (Auto COM Detection), dieu khien chuot 100% qua phan cung cach ly, 0% can thiep bo nho game.
   - **Lien he mua thiet bi Hugo Device:** Chi phi tu 499k - 2.999k (da bao gom ban quyen su dung) qua Telegram: [@Hugo997911](https://t.me/Hugo997911).

---

## BUOC 2: Chay Cap Quyen Windows Defender
> **Luu y:** Sau moi lan cap nhat phien ban moi, giai nen xong ban can lam lai buoc nay 1 lan, nhung cac lan mo sau khong can thiet.

De tranh Windows Defender bao nham hoac chan file chay:
1. Mo thu muc vua giai nen, click chuot phai vao file **`Cho_Phep_Chay_HugoAI.bat`** va chon **Run as Administrator**.
2. Script se tu dong them thu muc `HugoAI` vao danh sach loai tru (Exclusion) cua Windows Defender.
   - *Luu y tren Windows 11:* Neu dang bat Tamper Protection, script se tu dong copy duong dan thu muc vao Clipboard va mo cua so Windows Security de ban bam `Add an exclusion -> Folder -> Paste (Ctrl + V)` chi trong 1 click.

---

## BUOC 3: Khoi Chay Ung Dung (`HugoAI.exe`) & Kich Hoat Ban Quyen (License)
1. Click chuot phai vao file **`HugoAI.exe`** -> chon **Run as Administrator**.
2. Kich hoat ban quyen truc tuyen (Online Key):
   - Tai man hinh cho hoac chuyen den the **License** trong ung dung.
   - Dan ma **Online Key** nhan tu Admin (`@Hugo997911`) vao o nhap ma va bam **Kich hoat Online**.
   - He thong se tu dong kich hoat, cap nhat thoi han (hoac cong don ngay su dung) va mo nut **Vao Ung Dung**.

---

## BUOC 4: Mo Game PUBG & Cai Dat Chuan Trong Game (BAT BUOC)
De AI Vision nhan dien 100% vu khi/phu kien va quy dao ghim tam chuan xac tuyet doi, ban **bat buoc** thiet lap trong game PUBG nhu sau:

### 4.1. Ngon Ngu Game & Che Do Man Hinh
- **Ngon ngu trong game (Language):** Chuyen sang **TIENG ANH (ENGLISH)** (`Settings -> Gameplay -> Language -> Language Selection -> English`).
- **Che do hien thi (Display Mode):** Chon **Borderless** (Khong vien) hoac **Windowed** (Cua so). **Tuyet doi khong dung Fullscreen.**

### 4.2. Bang Thong So Chuot Chuan Trong Game (`Settings -> Controls -> Main`)

| Thiet Lap In-Game (Setting) | Gia Tri Chuan (Value) | Y Nghia / Ghi Chu (Description) |
| :--- | :--- | :--- |
| **Invert Mouse** | **Disable** | Tat dao nguoc chuot |
| **General Sensitivity** | **30** | Do nhay chuot tong the trong game |
| **Vertical Sensitivity Multiplier** | **1** (hoac 1.0) | Ty le nhay doc / ngang chuan |
| **Aim Sensitivity** | **30** | Do nhay ngam qua vai (Aim) |
| **ADS Sensitivity** | **30** | **Cuc ky quan trong**: Do nhay ngam ban dau ruoi / scope |
| **Universal Sensitivity for All Scopes** | **Enable** | Bat ap dung chung cho tat ca cac loai Scope |
| **Scoping Sensitivity** | **30** | Do nhay ong ngam |

---

## BUOC 5: Bang Phim Tat Dieu Khien Trong Tran (In-Game Hotkeys)
Khi vao tran, ban chi can mo balo (**Phim Tab**) de AI tu dong nhan dien sung/phu kien va su dung cac phim tat sau:

| Phim Tat (Hotkey) | Chuc Nang (Function) |
| :--- | :--- |
| **ALT + F12** | Bat / Tat Auto Recoil (Ghim tam tu dong) |
| **Tab** | Tu dong quet nhan dien sung va phu kien khi mo balo |
| **F1** | Chuyen Che Do Recoil (AUTO / MANUAL / S-ONLY / LOCKED) |
| **F2** | Chuyen doi Scope thu cong |
| **F3** | Chuyen doi Tay cam (Grip) thu cong |
| **F4** | Chuyen doi Dau nong (Muzzle) thu cong |
| **F5** | Quet balo thu cong (Force Full Scan) |
| **Caps Lock** | Bat / Tat Smart Auto Loot (Nhat do tu dong qua Vision AI) |
| **V** | Prone Macro (Tu dong nam ban - Drop Shot khi say, mac dinh: OFF) |
| **Mui ten Len (Up)** | Tang luc giat doc (Recoil Vertical +) khi bat Custom Recoil |
| **Mui ten Xuong (Down)** | Giam luc giat doc (Recoil Vertical -) khi bat Custom Recoil |
| **Mui ten Trai / Phai** | Bu tru do giat ngang (Horizontal Recoil Bias Left/Right) |
| **ALT + F9** | Ket noi lai thiet bi phan cung Hugo Device |
| **ALT + F10** | Nap lai file cau hinh Hotkeys va Cloud Profile |
| **F11** | Bat / Tat giao dien In-Game HUD Overlay |
| **Shift + Esc** | Thoat nhanh khan cap va dong toan bo tien trinh ngam (Panic Exit) |

---

## BUOC 6: Huong Dan Tinh Chinh Thong So Nang Cao & Danh Sach Vu Khi Ho Tro

### 6.1. Cac Thong So Trong Hugo Recoil (Ghim Tam Tu Dong)
1. **Toggle Recoil (ALT + F12):** Bat/Tat ghim tam. Khi tat, HUD bao `RECOIL: PAUSED`.
2. **Recoil Multiplier (He so luc ghim - Mac dinh `1.00`):**
   - **So lon hon (> 1.0, vi du 1.05 - 1.20):** Ghim **MANH HON** (chinh tang khi dan bay len tren dau muc tieu).
   - **So nho hon (< 1.0, vi du 0.85 - 0.95):** Ghim **NHE LAI** (chinh giam khi tam sung bi keo chui xuong dat).
3. **Custom Recoil:** Khi **ON** cho phep luu luc ghim rieng cho tung sung tren may ca nhan; khi **OFF** dung 100% thong so chuan tu Cloud.
4. **Human Jitter:** Mo phong dao dong vi mo cua tay nguoi that.
5. **Smart Auto Loot (Caps Lock) & Prone Macro (Phim V):** Ho tro nhat do sieu toc va nam ban Drop Shot (Mac dinh: OFF).

### 6.2. Cac Thong So Trong Hugo AI (AI Aim Assist & Target Tracking)
1. **Sticky Aim & Sticky Aim Threshold (0 - 100 px, Khuyen dung `40 - 60 px`):**
   - Khoa chat muc tieu dang ban, chong nhay tam khi co nhieu dich dung gan nhau.
2. **Prediction Method - Hugo Zero-Lag Tracking (Khuyen dung):**
   - **Base Lookahead (Mac dinh `2.90`):** He so ban don dau theo thoi gian dan bay (`< 2.0` cho tam gan, `> 3.5` cho tam xa/xe chay).
   - **Tracking Feedforward (Mac dinh `1.00`):** Bu tre van toc khung hinh giup tam bam sat muc tieu di chuyen ngang.
   - **Distance Adaptive Lead (Khuyen dung `ON`):** Tu dong tang/giam don dau theo khoang cach xa/gan cua dich.
3. **FOV Size (10 - 640 px):** Ban kinh vung quet quanh tam (`100 - 200 px` ban kin dao legit; `300 - 500 px` quet rong).
4. **Mouse Sensitivity (0.01 - 1.00):** Toc do keo chuot cua AI (`0.15 - 0.40` muot tu nhien; `0.70 - 0.90` bam nhanh).
5. **Y Offset (-150 den +150 px):** Keo sang **TRAI (so am)** uu tien ban len **DAU**; keo sang **PHAI (so duong)** ban vao **NGUC/THAN**.
6. **X Offset (-150 den +150 px):** Chinh lech tam ngang Trai (so am) / Phai (so duong).
7. **EMA Smoothening, Max AI FPS (60 - 165 FPS) & AI Minimum Confidence (Khuyen dung 45% - 60%).**

### 6.3. Danh Sach Cac Loai Sung & Phu Kien Ho Tro
| Nhom Sung (Category) | Cac Loai Sung Ho Tro (Supported Weapons) |
| :--- | :--- |
| **AR Dan 5.56mm** | M416, AUG, SCAR-L, QBZ, G36C, K2 |
| **AR Dan 7.62mm** | Beryl M762, AKM, ACE32, GROZA |
| **SMG / CQC** | UZI, MP5K, VECTOR, P90, JS9, MP9, PP-19 Bizon, Tommy Gun, UMP45 |
| **DMR / LMG** | M249, DP-28, MG3, FAMAS, M16A4, Mk47 Mutant, RPD |
| **Ong Ngam (Scopes)** | Red Dot, Holo, 2x, 3x, 4x, 6x, 8x, 15x (Tu dong bu tru luc giat rieng cho tung Scope) |
| **Phu Kien (Attachments)** | Tu dong nhan dien Tay cam (Vert, Angled, Half, Thumb, Light) & Dau nong (Comp, Flash, Brake, Supp) |

---

## BUOC 7: Toi Uu Hieu Nang Do Hoa & Lien He Ho Tro (Support)
- **Toi uu NVIDIA & PUBG:**
  - **Low Latency Mode:** Chon **Ultra** trong NVIDIA Control Panel.
  - **Power Management Mode:** Chon **Prefer maximum performance**.
  - **DirectX:** Chon **DirectX 11** hoac **DirectX 11 Enhanced**; **V-Sync:** **Disable**.
- **Thong tin lien he & Ho tro chinh thuc:**
  - **Developer:** Hugo
  - **Telegram Support:** [@Hugo997911](https://t.me/Hugo997911)
  - **Copyright:** DEV by Hugo (telegram: @Hugo997911)
