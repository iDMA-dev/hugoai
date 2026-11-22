# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

## [v6.3.89] - 2026-11-22
### 1. Nang Cap He Thong Tang Toc GPU Kep: NVIDIA CUDA / Tensor Core Boost & Smart DirectML Discrete Lock
- Bo sung che do tang toc phan cung **NVIDIA CUDA / Tensor Core Boost** (ho tro day du GTX 16xx, RTX 20xx, RTX 30xx, RTX 40xx va RTX 50xx Blackwell) song song voi **DirectML**: Cai dat ngam chi 1 lan duy nhat vao may, tu dong giu nguyen qua tat ca cac ban cap nhat `HugoAI` ve sau ma khong lam tang dung luong tai App (~98 MB).
- Ung dung cong nghe **Hardware CUDA Graph** va bo nho **Zero-Allocation Pinned IoBinding**: Gom toan bo 239 lop mang AI thanh 1 lenh GPU duy nhat, giam do tre suy luan tuc thi (dat ~550 - 720 FPS o khung FOV tieu chuan va nhanh hon 43% o khung 640px) dong thoi chong tranh chap 3D Queue khi PUBG chiem 99% GPU tren man 2K.
- Toi uu hoa **DirectML Native** cho Card **AMD Radeon / Intel Arc & Laptop Gaming**: Tu dong quet DXGI va khoa cung vao Card do hoa roi co VRAM lon nhat (loai bo 100% loi chay nham tren card tich hop iGPU onboard cua CPU Ryzen 7000/9000 hoac Intel) kem co che Pre-Flight Kernel Warmup chong khug khung hinh dau tien.
- Tich hop thanh trang thai & chuyen doi nhanh **1-Click GPU Engine Banner** ngay tren dau tab `Aim Assist` va trong `Settings -> Model Settings`.
- Bo sung huy hieu trang thai **AI AIM: ON / OFF** hien thi co dinh, sieu gon ngay tren thanh **In-Game HUD Overlay** (**Xanh la** khi `ON`, **Do** khi `OFF`, dong bo tuc thi voi phim tat va cong tac giao dien) va toi uu co che luu giu trang thai `Aim Assist` ben vung 100% qua moi lan chuyen doi GPU Engine hoac khoi dong lai.
---
## [v6.3.88] - 2026-11-21
### 1. Cap Nhat Nhanh Tai Cho (1-Click In-Place Update) & Nang Cap Key Combo Linh Hoat
- Bo sung tinh nang **1-Click Update** ngay tren thanh Topbar va muc `About`: Tu dong tai ban moi va cap nhat truc tiep ngay tai thu muc dang su dung, giu nguyen 100% cau hinh ca nhan, Windows Security Exclusion va NVIDIA Profile, tu dong don sach file tam sau khi khoi dong lai.
- Toi gian va nang cap tab **License Center** (cung nut loi tat `+ KEY / COMBO` tren man hinh chinh): Hop nhat ve 1 o nhap Key thong minh duy nhat cho phep kich hoat moi, nang cap len goi **Combo VIP (`HGCB-...`)** hoac cong don ngay dung bat cu luc nao ngay ca khi ban quyen hien tai chua het han.
- Tu dong dong bo ngam ban quyen Cloud tuc thi khi mo tab hoac khi duoc gia han/nang cap tu xa ma khong can bam nut thu cong hay khoi dong lai ung dung.
## [v6.3.86] - 2026-11-13
### 1. Toi Uu Hieu Nang GPU Khi Giu Ngam & Luu Cau Hinh Tu Dong Tuc Thi
- Toi uu hoa hieu nang xu ly GPU DirectML khi kich hoat AI Aim + Auto Recoil (tu dong toi uu kich thuoc khung quet ngam theo vung FOV ma van giu 100% thanh truot FOV Size tu do tung pixel, giam dang ke muc tai GPU va nhiet do).
- Luu va khoi phuc chinh xac 100% trang thai cac tuy chon (`Aim Assist`, `FOV`, `FOV Style`, `UI TopMost`, `StreamGuard`, `EMA Smoothening`, `Hotkeys`, `Sliders`) ngay khi thay doi va sau khi khoi dong lai ung dung.
- Bo sung nut **RESET CUSTOM** tren the Recoil va co che nhan dien xoa `weapons_custom.json` thong minh de tra ngay ve thong so Cloud chuan mac dinh ma khong bi tai lai ban cu.