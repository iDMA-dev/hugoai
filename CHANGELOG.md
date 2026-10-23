# Hugo AI Suite - Nhat Ky Cap Nhat (Update History)
> **DEV by Hugo (telegram: @Hugo997911)**

## [v6.3.43] - 2026-10-23
### 1. Dong Bo Cong Tac Recoil Tren App & Bo Sung Phim Giu Ghim Tam Phu (`recoil_hold`)
  - Khi bat/tat cong tac Recoil tren App (khong dung hotkey) thi khong co tac dung hoac bi ghi de nguoc trang thai; can bo sung phim phu de kich hoat ghim tam khi bam giu + Chuot Trai (khong can giu ADS Chuot Phai).
### 2. Lam Sach Giao Dien (Clean UI) & Co Che Luu Du Phong 03 Phien Ban Gan Nhat
## [v6.3.42] - 2026-10-23
### 1. Bao Ve Ma Nguon Tuyet Doi Voi Cython Native C/C++ Compilation (.pyd Machine Code)
  - Nang cap bao mat chong dich nguoc (Anti-Decompile) va tang toc do thuc thi cho Recoil Engine.
### 3. Toi Uu Dung Luong He Thong & Tu Dong Don Dep Build Cu
## [v6.3.41] - 2026-10-14
### 1. Triet Tieu Lo Hong Lo Token GitHub & Bao Mat Cloud Profile Sync (Zero-Trust Security Upgrade)
- **Trieu chung & Rui ro:**
  - Client binary truoc day chua token GitHub du phong (`FallbackToken`) trong `ProfileSyncManager.cs`. Bat ky ai decompile binary deu co the doc duoc token nay va truy cap kho ma nguon.
### 2. Nang Cap Dong Bo Hoa Tuyen Doan IPC Named Pipe (Thread-Safe IPC Synchronization)
- **Trieu chung & Rui ro:**
  - Khi nhieu luong C# goi `SendCommandAsync` dong thoi (click UI, hotkey, dinh ky kiem tra status, sync license), cac goi tin JSON co the bi ghi de/xen ke nhau gay ra `[IPC PARSE ERR]` o Python daemon.
### 3. Toi Uu Hoa Hieu Nang Real-Time Aimbot Loop & Dispatcher (Zero-Blocking Overlay Engine)
- **Trieu chung & Rui ro:**
  - Aimbot loop chay o tan so 120 - 240 FPS nhung truoc day goi `Application.Current.Dispatcher.Invoke(...)` dong bo, gay block luong tinh toan neu WPF UI thread ban render hoac keo cua so.
### 4. Triet Tieu Thread Churn Trong Recoil Firing Trigger (Persistent Recoil Worker)
- **Trieu chung & Rui ro:**
  - Moi lan nhan ban (LMB), ham `start_firing` tao moi mot `threading.Thread(target=recoil_loop)`, gay tieu ton CPU va do tre khoi tao thread (0.5 - 2ms) khi nhap chuot ban nhanh (DMR / tap).
### 5. An Toan Dinh Dang Ngay Thang Theo Chuan InvariantCulture (Culture-Invariant License Parsing)
- **Trieu chung & Rui ro:**
  - `DateTime.TryParse` mac dinh dung Culture cua he dieu hanh, co the loi tren cac may cai Region/Language dac thu (Vi, Ar, Th).
### 6. Xu Ly An Toan Buffer Staging RowPitch Trong CaptureManager