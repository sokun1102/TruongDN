# Hướng dẫn Deploy lên Render.com

## Bước 1: Tạo GitHub Repository

1. Truy cập https://github.com và đăng nhập
2. Click nút **"+"** ở góc trên bên phải → chọn **"New repository"**
3. Điền thông tin:
   - **Repository name**: Đặt tên (ví dụ: `my-restaurant-api`)
   - **Description**: (tùy chọn) Mô tả ngắn
   - **Visibility**: Chọn **Public** (bắt buộc để Render deploy miễn phí)
   - **KHÔNG** tích vào "Add a README file" (vì đã có code)
4. Click **"Create repository"**

## Bước 2: Push code lên GitHub

Mở terminal/PowerShell và chạy các lệnh sau:

```bash
cd json-server-heroku
git init
git add .
git commit -m "Initial commit: json-server setup"
git branch -M main
git remote add origin https://github.com/<your_username>/<repository_name>.git
git push -u origin main
```

**Thay thế:**
- `<your_username>` = tên GitHub của bạn
- `<repository_name>` = tên repository bạn vừa tạo

## Bước 3: Tạo Web Service trên Render.com

1. Truy cập https://render.com và đăng nhập (có thể dùng GitHub để đăng nhập)
2. Click **"New +"** → chọn **"Web Service"**
3. Điền thông tin:

   **Public Git repository:**
   - Paste URL: `https://github.com/<your_username>/<repository_name>.git`

   **Name:**
   - Đặt tên cho service (ví dụ: `my-restaurant-api`)

   **Region:**
   - Chọn: **Singapore (Southeast Asia)**

   **Branch:**
   - Chọn: `main`

   **Runtime:**
   - Chọn: `Node`

   **Build Command:**
   - Nhập: `npm install`

   **Start Command:**
   - Nhập: `npm start`

   **Instance Type:**
   - Chọn: **Free**

4. Click **"Create Web Service"**

## Bước 4: Chờ deploy và test

- Render sẽ tự động build và deploy
- Chờ khoảng 2-5 phút để deploy xong
- Khi thấy "Live" màu xanh → deploy thành công!

## Bước 5: Test các endpoints

Sau khi deploy thành công, test các URL:

- `https://<webservice_name>.onrender.com/dishes`
- `https://<webservice_name>.onrender.com/leaders`
- `https://<webservice_name>.onrender.com/comments`
- `https://<webservice_name>.onrender.com/promotions`
- `https://<webservice_name>.onrender.com/images/logo.png`

Thay `<webservice_name>` bằng tên service bạn đã đặt ở Bước 3.

