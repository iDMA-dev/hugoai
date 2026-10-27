# Hugo AI Suite v6.3.65 - Huong Dan Su Dung & Cai Dat Toan Dien
> **Ban quyen / Author:** DEV by Hugo (telegram: @Hugo997911)  
> **Chuyen muc:** AI AIM, Auto Recoil & Ho tro PUBG Chuyen Nghiep

---

## 1. Yeu Cau He Thong (System Requirements)
- **He dieu hanh:** Windows 10 / Windows 11 (64-bit).
- **Yeu cau cai dat:** Zero Dependency (Ung dung da dong goi san .NET 8 runtime va cac thu vien AI, khong can cai them moi truong).
- **PHAN CUNG BAT BUOC (MANDATORY REQUIREMENT):** Bat buoc phai co thiet bi phan cung **Hugo Device** (ket noi qua cong USB may tinh) de dieu khien chuot phan cung 100% cach ly, 0% can thiep bo nho game.

---

## 2. Buoc Khoi Dau Quan Trong - Cai Dat Chung Chi & Bo Qua Defender
De tranh Windows Defender bao dong nham hoac chan file chay:
1. Click chuot phai vao file **`Cho_Phep_Chay_HugoAI.bat`** va chon **Run as Administrator**.
2. Script se tu dong:
   - Cai dat Chung chi so tin cay (Authenticode Root Certificate) vao may.
   - Tu dong them thu muc HugoAI vao danh sach loai tru (Folder Exclusion) cua Windows Defender.
   - Neu Windows 11 dang bat Tamper Protection, script se tu dong copy duong dan vao Clipboard va mo trang cai dat Windows Security de ban paste them trong 1 click.

---

## 3. Thiet Bi Phan Cung (Hugo Device) - BAT BUOC
- **Lien he (Support) de mua Hugo Device:**
  - Chi phi tu 499 ca den 2.999 ca (da bao gom ban quyen su dung).
  - Telegram Support: [@Hugo997911](https://t.me/Hugo997911)
- **Huong dan ket noi thiet bi:**
  - Cam thiet bi Hugo Device vao cong USB may tinh truoc khi khoi dong ung dung.
  - He thong se tu dong quet va ket noi cong COM tuong thich (Auto COM Detection).

---

## 4. Cach Kich Hoat Ban Quyen (License Activation)
Hugo AI ho tro 2 hinh thuc kich hoat tien loi:
- **Cach 1 (Khuyen dung - Online Key):**
  - Mo ung dung `HugoAI.exe`, chuyen den the **License**.
  - Nhap ma kich hoat Online Key nhan tu Admin (@Hugo997911) va bam **Kich hoat Online**.
  - He thong se tu dong xac thuc RSA qua Cloud, cap nhat thoi han va tu dong cong don ngay su dung.
- **Cach 2 (Offline License):**
  - Chep truc tiep file ban quyen `*.lic` nhan tu Admin vao **cung thu muc** voi file `HugoAI.exe`.
  - Khi khoi chay, ung dung se tu dong nhan dien va kich hoat offline ngay lap tuc.

---

## 5. Bang Phim Tat Mac Dinh Trong Game (Default In-Game Hotkeys)

| Phim Tat (Hotkey) | Chuc Nang (Function) |
| :--- | :--- |
| **F1** | Bat / Tat Auto Recoil (Ghim tam tu dong) |
| **F2** | Chuyen doi sung nhanh / Bat tat Recoil phu |
| **F3** | Bat / Tat Smart Auto Loot (Nhat do tu dong qua Vision AI) |
| **F4** | Bat / Tat Prone Macro (Tu dong nam ban - Drop Shot khi say) |
| **Mui ten Len (Up)** | Tang luc giat doc (Recoil Vertical +) truc tiep trong tran dau |
| **Mui ten Xuong (Down)** | Giam luc giat doc (Recoil Vertical -) truc tiep trong tran dau |
| **Mui ten Trai / Phai** | Bu tru do giat ngang (Horizontal Recoil Bias Left/Right) |
| **F11** | Bat / Tat giao dien In-Game HUD Overlay |
| **Shift + Esc** | Thoat nhanh khan cap va dong toan bo tien trinh ngam (Panic Exit) |

---

## 6. Tinh Nang Noi Bat & Danh Sach Vu Khi Ho Tro

### Bang Tinh Nang Noi Bat (Key Features)

| Tinh Nang (Feature) | Mo Ta Chi Tiet (Description) |
| :--- | :--- |
| **AI Aim Alignment** | Tu dong nhan dien va bam muc tieu thoi gian thuc bang AI (GPU/CPU) toc do cao |
| **Auto Recoil Engine** | Tu dong nhan dien sung, ong ngam, phu kien de ghim tam chuan xac tuyet doi |
| **Smart Auto Loot** | Tu dong quet va nhat nhanh trang bi, dan duoc, phu kien sieu toc qua Vision AI |
| **Prone Macro (Drop Shot)** | Ho tro macro tu dong nam ban linh hoat trong cac pha giao tranh |
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

## 7. Ha Tang Cloud 4 Lop Tu Dong Chuyen Vung (Multi-Worker Failover)
He thong xac thuc Hugo AI tich hop co che failover da tang, tu dong chuyen server trong 0.5s neu 1 duong truyen bi loi:
1. **Server 1 (Primary):** `https://hugo-ai-pubg-auth.team-idma-dev.workers.dev`
2. **Server 2 (Custom Domain 1):** `https://hugoai.idma.dev` (Khong bao gio bi chan boi nha mang VN)
3. **Server 3 (Backup Account):** `https://hugo-ai-pubg-auth-backup.gafaba.workers.dev`
4. **Server 4 (Custom Domain 2):** `https://hugoai.gafaba.com` (Du phong da ten mien TLD)

---

## 8. Huong Dan Khoi Chay & Cai Dat Game (Launch & Game Settings)
1. **Quyen quan tri (Administrator):** Luon click chuot phai vao file `HugoAI.exe` va chon **Run as Administrator**.
2. **Che do man hinh trong PUBG:**
   - Cai dat game o che do **Borderless (Khong vien)** hoac **Windowed (Cua so)**.
   - *Luu y quan trong:* Tuyet doi khong dung che do Fullscreen doc quyen vi AI Vision can chup man hinh de nhan dien vu khi.
3. **Do phan giai ho tro:** Ho tro tot nhat tren man hinh **1920x1080 (Full HD)** va **2560x1440 (2K)**.

---

## 9. Toi Uu Hieu Nang Do Hoa & Do Tre (NVIDIA & Windows Optimization)
De dat do tre thap nhat (Ultra Low Latency), game muot ma va Hugo AI nhan dien vu khi sieu toc, hay thiet lap rieng biet cho PUBG va Hugo AI theo huong dan sau:

### A. Thiet Lap Rieng Cho Game PUBG (`TslGame.exe`)
*Muc tieu:* Giup PUBG dat FPS cao va on dinh, loai bo do tre chuot (Input Lag), khong de PUBG chiem dung 100% GPU gay nghen pipeline chup man hinh cua AI.

1. Mo **NVIDIA Control Panel** -> Vao muc **Manage 3D Settings** -> Chon tab **Program Settings**.
2. Bam nut **Add** -> Chon `TslGame.exe` (PUBG):
   - **Low Latency Mode:** Chon **Ultra** (Giai phap thay the cho NVIDIA Reflex, tu dong ha thap render queue xuong 0-1 frame, triet tieu do tre render giua game va AI capture).
   - **Power Management Mode:** Chon **Prefer maximum performance** (Giu xung nhip GPU luon o muc cao nhat khi giao tranh).
   - **Max Frame Rate:** Neu man hinh 144Hz hoac 240Hz, nen khoa FPS game o muc `Tan so quet - 3` (vi du 141 hoac 237 FPS) de GPU khong bi qua tai 100% full load, giu lai bang thong cho Tensor/CUDA cores cua AI.
   - **Threaded Optimization:** Chon **On**.
   - **Vertical Sync (V-Sync):** Chon **Off** (tat ca trong Nvidia Panel va trong game PUBG).
3. Trong cai dat game PUBG:
   - **Graphics -> DirectX Version:** Chon **DirectX 11** hoac **DirectX 11 Enhanced** (on dinh va chup man hinh nhanh nhat, tranh dung DirectX 12).
   - **Graphics -> V-Sync:** Chon **Disable (Tat)**.

### B. Thiet Lap Rieng Cho Hugo AI (`HugoAI.exe` & `HugoCore.exe`)
*Muc tieu:* Uu tien tien trinh AI suy luan (inference) tuc thi, phan hoi nhan dien sung, phu kien trong 1-2 ms. Ten file da duoc chuan hoa co dinh, chi can add 1 lan duy nhat.

1. Trong **NVIDIA Control Panel** -> **Manage 3D Settings** -> Tab **Program Settings**:
2. Bam nut **Add** -> Chon file `HugoAI.exe` (va `HugoCore.exe`):
   - **Power Management Mode:** Chon **Prefer maximum performance** (Bat buoc, giup GPU cap xung ngay khi AI thuc hien suy luan).
   - **CUDA - GPUs:** Chon chinh xac card roi NVIDIA GeForce (tranh bi Windows nhan dien sang iGPU Onboard).
   - **Low Latency Mode:** Chon **Ultra** hoac **On**.
   - **Max Frame Rate:** Chon **Off** (khong gioi han cho AI).
3. Trong **NVIDIA App / GeForce Experience**:
   - **NEN TAT Game Filters** (bo loc mau overlay) vi cac filter mau se lam sai lech pixel nhan dien phu kien va lam giam FPS capture cua Vision AI.

### C. Cai Dat Windows Graphics (Hardware-Accelerated GPU Scheduling - HAGS)
1. Nhan phim `Windows + S` -> Tim kiem **Graphics Settings (Cai dat do hoa)**.
2. Bat **Hardware-accelerated GPU scheduling (HAGS)** -> **On** (khoi dong lai may neu moi bat lan dau).
3. Muc *Custom options for apps*:
   - Bam **Browse** -> Chon file `HugoAI.exe`.
   - Bam **Options** -> Chon **High Performance** (chi dinh card roi NVIDIA).

---

## 10. Ho Tro & Lien He (Support)
- **Developer:** Hugo
- **Telegram Support:** [@Hugo997911](https://t.me/Hugo997911)
- **Copyright:** DEV by Hugo (telegram: @Hugo997911)
