# Hugo AI Suite v6.3.70 - Huong Dan Su Dung & Cai Dat Toan Dien
> **Ban quyen / Author:** DEV by Hugo (telegram: @Hugo997911)  
> **Chuyen muc:** AI AIM, Auto Recoil & Ho tro PUBG Chuyen Nghiep

---

## 1. Yeu Cau He Thong & Luu Y Quan Trong (System Requirements & Important Note)
- **He dieu hanh:** Windows 10 / Windows 11 (64-bit).
- **Yeu cau cai dat:** Zero Dependency (Ung dung da dong goi san .NET 8 runtime va cac thu vien AI, khong can cai them moi truong).
- **PHAN CUNG BAT BUOC (MANDATORY REQUIREMENT):** Bat buoc phai co thiet bi phan cung **Hugo Device** (ket noi qua cong USB may tinh) de dieu khien chuot phan cung 100% cach ly, 0% can thiep bo nho game, khong lo bi phat hien.
- **LUU Y QUAN TRONG VE NGON NGU IN-GAME:**
  > **Hugo AI Suite hoat dong tot nhat va chinh xac nhat o ngon ngu TIENG ANH (ENGLISH) trong cai dat game PUBG.**
  > Vui long vao `Settings -> Gameplay -> Language -> Language Selection -> English` de AI Vision nhan dien 100% ten sung, phu kien va thong so vat pham.

---

## 2. Cai Dat In-Game PUBG Chuan Xac (PUBG In-Game Mouse Settings - BAT BUOC)
De he thong Recoil va AI Aim hoat dong voi quy dao ghim tam chuan xac tuyet doi, ban can thiet lap cac thong so chuot trong game PUBG chinh xac nhu sau:

| Thiet Lap In-Game (Setting) | Gia Tri Chuan (Value) | Y Nghia / Ghi Chu (Description) |
| :--- | :--- | :--- |
| **Invert Mouse** | **Disable** | Tat dao nguoc chuot |
| **General Sensitivity** | **30** | Do nhay chuot tong the trong game |
| **Vertical Sensitivity Multiplier** | **1** (hoac 1.0) | Ty le nhay doc / ngang chuan |
| **Aim Sensitivity** | **30** | Do nhay ngam qua vai (Aim) |
| **ADS Sensitivity** | **30** | **Cuc ky quan trong**: Do nhay ngam ban dau ruoi / scope |
| **Universal Sensitivity for All Scopes** | **Enable** | Bat ap dung chung cho tat ca cac loai Scope |
| **Scoping Sensitivity** | **30** | Do nhay ong ngam |
| **Display Mode (Che do man hinh)** | **Borderless** / **Windowed** | **Khong dung Fullscreen doc quyen** |

---

## 3. Huong Dan Chi Tiet Cac Thong So Cai Dat (Settings Detailed Guide)

### A. Cac Thong So Trong Hugo Recoil (Ghim Tam Tu Dong)
1. **Toggle Recoil (ALT + F12):**
   - Bat hoac tat toan bo he thong ghim tam Recoil. Khi tat, HUD se bao `RECOIL: PAUSED` va khong can thiep chuot.
2. **Recoil Multiplier (Do nhay / Luc ghim tam):**
   - He so nhan luc ghim tong the (Mac dinh: `1.00`).
   - Co the dieu chinh truc tiep trong tran bang 2 phim **Mui ten Len (Up)** va **Mui ten Xuong (Down)** (khi bat Custom Recoil).
   - **So lon hon (> 1.0, vi du 1.05 - 1.20):** Luc ghim **MANH HON**, chuot bi keo xuong sau hon. *Chinh tang khi thay dan bi giat bay len tren dau muc tieu*.
   - **So nho hon (< 1.0, vi du 0.85 - 0.95):** Luc ghim **NHE LAI**, chuot keo it hon. *Chinh giam khi thay tam sung bi ghim chui xuong dat*.
3. **Custom Recoil:**
   - Khi **ON**: Cho phep nguoi choi tuy chinh va luu luc ghim rieng biet cho tung khau sung vao may ca nhan.
   - Khi **OFF**: Su dung 100% thong so chuan dong bo tu Master Cloud Profile.
4. **Human Jitter (Mo phong rung tay nguoi):**
   - Tu dong them cac dao dong vi mo ngau nhien vao quy dao ghim tam de chong cac he thong Anti-Cheat AI phat hien duong keo chuot hoan hao dang robot.
5. **Smart Auto Loot (Phim Caps Lock):**
   - Tu dong quet va nhat trang bi, dan duoc, phu kien sieu toc qua Vision AI.
6. **Prone Macro - Drop Shot (Phim V):**
   - Macro tu dong nam ban khi say (Mac dinh: **OFF** de nguoi dung chu dong bat khi can).

---

### B. Cac Thong So Trong Hugo AI (AI Aim Assist & Target Tracking)
1. **Sticky Aim & Sticky Aim Threshold (0 - 100 pixel):**
   - **Sticky Aim (Bat / Tat):** Khoa chat mot muc tieu duy nhat dang ban cho toi khi bi ha guc, chong hien tuong tam nhay loan xa (crosshair hopping) khi co nhieu dich dung gan nhau.
   - **Sticky Aim Threshold (Ban kinh dung sai: 0 - 100 px):**
     + **So nho (0 - 20 px):** Nguong bam long, de doi muc tieu sang ke dich khac neu ke do chay sat tam chuot hon.
     + **So lon (60 - 100 px):** Luc hut dinh cuc manh vao muc tieu hien tai, ke dich khac chay ngang qua che dan cung khong bi hut tam theo.
     + **Khuyen dung:** `40 - 60 px` (can bang giua bam dinh va linh hoat doi muc tieu).
2. **Prediction Method (Thuat toan du doan don dau):**
   - **Hugo Zero-Lag Tracking (Khuyen dung - Cong nghe doc quyen Hugo):**
     Triet tieu hoan toan do tre khung hinh nho he thong Feedforward dong toc va bo loc toc do cao Alpha-Beta.
     + **Base Lookahead (0.0 - 6.0 Factor, Mac dinh: 2.90):** He so ban don dau do thoi gian dan bay trong PUBG.
       * *Keo sang Trai (< 2.0 Factor):* Don ngan, ngam sat than dich (phu hop tam gan, dich di bo cham).
       * *Keo sang Phai (> 3.5 Factor):* Don xa hon ve phia truoc huong dich chay (phu hop dich sprint o tam xa 70-150m hoac lai xe co chay ngang).
       * *Khuyen dung:* `2.90 Factor`.
     + **Tracking Feedforward (0.0 - 1.50 Gain, Mac dinh: 1.00):** Luc day bu tre van toc khung hinh. Truyen luc di chuot dong pha song song voi van toc dich ngay trong frame hien tai.
       * *Keo sang Trai (< 0.70 Gain):* Chuot di chuyen em hon, it quan tinh.
       * *Keo sang Phai (> 1.20 Gain):* Chuot bam dong toc cuc manh theo dich chay nuoc rut (khong de qua 1.30 de tranh bi vot tron khi dich phanh dot ngot).
       * *Khuyen dung:* `1.00 Gain` (Ty le dong toc hoan hao 1:1).
     + **Distance Adaptive Lead (Bat / Tat):** Tu dong tinh toan va dieu chinh he so don dau dua theo chieu cao Bounding Box cua dich tren man hinh (dich o xa nguoi nho -> tang he so len toi 2.2x; dich o gan nguoi to -> giam xuong 0.7x de tranh ban truot). Khuyen dung: **BAT (ON)**.
   - **Kalman Filter (Thuat toan truyen thong):**
     + **Kalman Lead Time (0.02 - 0.50 giay):** Thoi gian don dau co dinh theo bo loc Kalman (chi hien thi khi chuyen sang thuat toan Kalman Filter).
3. **FOV Size (10 - 640 pixel):**
   - Ban kinh vung tron tim kiem muc tieu xung quanh tam man hinh.
   - **So nho (100 - 200 px):** Vung quét hep, chi ho tro khi tam da o rat gan muc tieu. Thich hop ban kin dao (legit), khong bi lo khi stream/quay clip.
   - **So lon (300 - 500 px):** Vung quet rong, giup bat va khoa muc tieu o xa tam ngam mot cach de dang.
4. **Mouse Sensitivity (+/-) (0.01 - 1.00):**
   - Toc do va cuong do keo chuot cua AI khi bam duoi muc tieu.
   - **So nho (0.10 - 0.40):** Keo chuot nhe nhang, em ai, tao cam giac ngam ban hoan toan tu nhien.
   - **So lon (0.70 - 0.90):** Keo chuot cuc nhanh, tam dinh chat vao muc tieu ngay khi xuat hien.
3. **Sticky Aim Threshold (0 - 100 pixel):**
   - Do dinh tam (nguong giu muc tieu). Khi tam da vao sat nguoi dich trong khoang cach nay, AI se tang cuong do bam giu de tam khong bi vang ra ngoai du dich co nhay hay doi huong.
5. **Y Offset (Up/Down) (-150 den +150 pixel):**
   - Diem ngam muc tieu theo chieu doc (Dau / Co / Nguc):
   - **Keo thanh truot sang TRAI (Gia tri am, -):** Tam ngam duoc day **LEN CAO** (Uu tien Headshot / ban vao dau).
   - **Keo thanh truot sang PHAI (Gia tri duong, +):** Tam ngam duoc keo **XUONG DUOI** (Nguc / Than tren, an toan va de trung dan).
6. **X Offset (Left/Right) (-150 den +150 pixel):**
   - Diem ngam muc tieu theo chieu ngang:
   - **Keo sang TRAI (Gia tri am, -):** Tam ngam lech sang **BEN TRAI** muc tieu.
   - **Keo sang PHAI (Gia tri duong, +):** Tam ngam lech sang **BEN PHAI** muc tieu.
6. **Kalman Lead Time (0.02 - 0.50 giay):**
   - Thuat toan du doan don dau huong di chuyen cua dich (Lead Tracking):
   - **So lon (0.15 - 0.35s):** Ban don dau xa hon ve phia truoc khi muc tieu dang chay nhanh ngang man hinh hoac di chuyen bang phuong tien (xe co).
   - **So nho (0.05 - 0.10s):** Ngam sat nguoi muc tieu, phu hop dich dang di bo cham hoac giao tranh tam gan.
7. **EMA Smoothening (0.01 - 1.00):**
   - Bo loc lam muot chuyen dong chuot (Exponential Moving Average):
   - **So lon:** Chuyen dong chuot muot ma, em ai, triet tieu hien tuong rung lac tam man hinh.
8. **Max AI FPS (60 - 165 FPS):**
   - Toc do xu ly suy luan AI moi giay. Khuyen nghi cai dat phu hop voi tan so quet man hinh hoac kha nang cua GPU (Mac dinh: `60` - `120`).
9. **AI Minimum Confidence (1 - 100%):**
   - Do tin cay toi thieu de AI xac nhan do la nguoi choi dich:
   - **So lon (50% - 70%):** Chi ngam khi nhin thay ro rang nguoi dich, tranh tuyet doi viec nhan nham goc cay, tang da.
   - **So nho (35% - 45%):** Nhan dien nhay hon khi dich nup sau bui co hoac o khoang cach cuc xa.

---

## 4. Bang Phim Tat Mac Dinh Trong Game (Default In-Game Hotkeys)

| Phim Tat (Hotkey) | Chuc Nang (Function) |
| :--- | :--- |
| **ALT + F12** | Bat / Tat Auto Recoil (Ghim tam tu dong) |
| **F1** | Chuyen Che Do Recoil (AUTO / MANUAL / S-ONLY / LOCKED) |
| **F2** | Chuyen doi Scope thu cong |
| **F3** | Chuyen doi Tay cam (Grip) thu cong |
| **F4** | Chuyen doi Dau nong (Muzzle) thu cong |
| **F5** | Quet balo thu cong (Force Full Scan) |
| **Tab** | Tu dong quet nhan dien sung va phu kien khi mo balo |
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

## 5. Buoc Khoi Dau Quan Trong - Bo Qua Windows Defender
De tranh Windows Defender bao dong nham hoac chan file chay:
1. Click chuot phai vao file **`Cho_Phep_Chay_HugoAI.bat`** va chon **Run as Administrator**.
2. Script se tu dong:
   - Tu dong them thu muc HugoAI vao danh sach loai tru (Folder Exclusion) cua Windows Defender.
   - Neu Windows 11 dang bat Tamper Protection, script se tu dong copy duong dan vao Clipboard va mo trang cai dat Windows Security de ban paste them trong 1 click.

---

## 6. Thiet Bi Phan Cung (Hugo Device) - BAT BUOC
- **Lien he (Support) de mua Hugo Device:**
  - Chi phi tu 499 ca den 2.999 ca (da bao gom ban quyen su dung).
  - Telegram Support: [@Hugo997911](https://t.me/Hugo997911)
- **Huong dan ket noi thiet bi:**
  - Cam thiet bi Hugo Device vao cong USB may tinh truoc khi khoi dong ung dung.
  - He thong se tu dong quet va ket noi cong COM tuong thich (Auto COM Detection).

---

## 7. Cach Kich Hoat Ban Quyen (License Activation)
Hugo AI ho tro 2 hinh thuc kich hoat tien loi:
- **Cach 1 (Khuyen dung - Online Key):**
  - Mo ung dung `HugoAI.exe`, chuyen den the **License**.
  - Nhap ma kich hoat Online Key nhan tu Admin (@Hugo997911) va bam **Kich hoat Online**.
  - He thong se tu dong xac thuc RSA qua Cloud, cap nhat thoi han va tu dong cong don ngay su dung.
- **Cach 2 (Offline License):**
  - Chep truc tiep file ban quyen `*.lic` nhan tu Admin vao **cung thu muc** voi file `HugoAI.exe`.
  - Khi khoi chay, ung dung se tu dong nhan dien va kich hoat offline ngay lap tuc.

---

## 8. Tinh Nang Noi Bat & Danh Sach Vu Khi Ho Tro

### Bang Tinh Nang Noi Bat (Key Features)

| Tinh Nang (Feature) | Mo Ta Chi Tiet (Description) |
| :--- | :--- |
| **AI Aim Alignment** | Tu dong nhan dien va bam muc tieu thoi gian thuc bang AI (GPU/CPU) toc do cao |
| **Auto Recoil Engine** | Tu dong nhan dien sung, ong ngam, phu kien de ghim tam chuan xac tuyet doi |
| **Smart Auto Loot** | Tu dong quet va nhat nhanh trang bi, dan duoc, phu kien sieu toc qua Vision AI |
| **Prone Macro (Drop Shot)** | Ho tro macro tu dong nam ban linh hoat trong cac pha giao tranh (Mac dinh: OFF) |
| **In-Game HUD Overlay** | Hien thi truc quan thong tin sung, phu kien va trang thai ngay tren man hinh game |
| **Cloud Profile Sync** | Tu dong dong bo thong so ghim tam toi uu lien tuc tu he thong Cloud |
| **Process Stealth Cloaking** | Engine chay ngam mang ten HugoCore.exe, an danh 100% truoc Task Manager va Anti-Cheat |
| **Multi-Worker Cloud Failover** | Ha tang xac thuc 4 lop voi Cloudflare Workers va 2 Custom Domains rieng biet |
| **Hardware Isolation (100% Safe)** | Hoan toan qua Hugo Device phan cung (0% can thiep bo nho game, khong lo bi khoa acc) |

### Danh Sach Cac Loai Sung Ho Tro (Supported Weapons)

| Nhom Sung (Category) | Cac Loai Sung Ho Tro (Supported Weapons) |
| :--- | :--- |
| **AR Dan 5.56mm** | M416, AUG, SCAR-L, QBZ, G36C, K2 |
| **AR Dan 7.62mm** | Beryl M762, AKM, ACE32, GROZA |
| **SMG / CQC** | UZI, MP5K, VECTOR, P90, JS9, MP9, PP-19 Bizon, Tommy Gun, UMP45 |
| **DMR / LMG** | M249, DP-28, MG3, FAMAS, M16A4, Mk47 Mutant, RPD |
| **Ong Ngam (Scopes)** | Ho tro toan bo Scope: Red Dot, Holo, 2x, 3x, 4x, 6x, 8x, 15x (Bu tru luc giat rieng cho tung loai) |
| **Phu Kien (Attachments)** | Tu dong nhan dien moi Tay cam (Vert, Angled, Half, Thumb, Light) & Dau nong (Comp, Flash, Brake, Supp) |

---

## 9. Ha Tang Cloud 4 Lop Tu Dong Chuyen Vung (Multi-Worker Failover)
He thong xac thuc Hugo AI tich hop co che failover da tang, tu dong chuyen server trong 0.5s neu 1 duong truyen bi loi:
1. **Server 1 (Primary):** `https://hugo-ai-pubg-auth.team-idma-dev.workers.dev`
2. **Server 2 (Custom Domain 1):** `https://hugoai.idma.dev` (Khong bao gio bi chan boi nha mang VN)
3. **Server 3 (Backup Account):** `https://hugo-ai-pubg-auth-backup.gafaba.workers.dev`
4. **Server 4 (Custom Domain 2):** `https://hugoai.gafaba.com` (Du phong da ten mien TLD)

---

## 10. Toi Uu Hieu Nang Do Hoa & Do Tre (NVIDIA & Windows Optimization)
De dat do tre thap nhat (Ultra Low Latency), game muot ma va Hugo AI nhan dien vu khi sieu toc:
- **Low Latency Mode:** Chon **Ultra** trong NVIDIA Control Panel.
- **Power Management Mode:** Chon **Prefer maximum performance**.
- **DirectX:** Chon **DirectX 11** hoac **DirectX 11 Enhanced** trong PUBG.
- **V-Sync:** Chon **Disable (Tat)**.

---

## 11. Ho Tro & Lien He (Support)
- **Developer:** Hugo
- **Telegram Support:** [@Hugo997911](https://t.me/Hugo997911)
- **Copyright:** DEV by Hugo (telegram: @Hugo997911)
