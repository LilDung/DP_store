# Quản Lý Đóng Góp Khởi Nghiệp

Ứng dụng web theo dõi dòng vốn của 2 người sáng lập. Chạy trực tiếp trên trình duyệt, không cần server.

## Deploy lên GitHub (dùng miễn phí qua GitHub Pages)

### Cách 1 — Không cần cài Git (nhanh nhất)

1. Đăng nhập [GitHub](https://github.com).
2. Bấm **+** → **New repository**.
3. Đặt tên repo (ví dụ: `startup-cashflow`), chọn **Public**, bấm **Create repository**.
4. Trên trang repo mới, chọn **uploading an existing file**.
5. Kéo thả toàn bộ file trong thư mục `game` vào (gồm `index.html`, `manifest.json`, `service-worker.js`, icon nếu có).
6. Bấm **Commit changes**.
7. Vào **Settings** → **Pages**:
   - **Source**: Deploy from a branch
   - **Branch**: `main` (hoặc `master`) / folder **/(root)**
   - **Save**
8. Đợi 1–2 phút, mở link dạng:  
   `https://<tên-github-của-bạn>.github.io/<tên-repo>/`

### Cách 2 — Dùng Git trên máy

1. Cài [Git for Windows](https://git-scm.com/download/win), mở lại terminal.
2. Trong thư mục `game`:

```powershell
cd "C:\Users\luudu\Downloads\game"
git init
git add .
git commit -m "Initial commit: startup cashflow app"
git branch -M main
git remote add origin https://github.com/LilDung/DP_store.git
git push -u origin main
```

3. Bật **GitHub Pages** như bước 7 ở Cách 1.

## Lưu ý

- `manifest.json` tham chiếu `icon-192.png` và `icon-512.png`. Nếu chưa có file icon, app vẫn chạy nhưng cài lên màn hình chính có thể thiếu biểu tượng.
- Dữ liệu lưu trong **localStorage** của trình duyệt — mỗi thiết bị/trình duyệt có bộ dữ liệu riêng.
