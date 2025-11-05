# Hướng dẫn Deploy lên Replit

## Bước 1: Tạo Repl mới trên Replit

1. Truy cập https://replit.com và đăng nhập
2. Click **"Create Repl"** hoặc **"+"** để tạo Repl mới
3. Chọn:
   - **Template**: `Node.js`
   - **Title**: Đặt tên cho Repl của bạn (ví dụ: `my-json-server`)

## Bước 2: Upload files vào Replit

1. Trong Replit, bạn sẽ thấy có file explorer bên trái
2. Upload **TẤT CẢ** files và folders từ thư mục `json-server-heroku`:
   - `db.json`
   - `package.json`
   - `server.js`
   - Thư mục `public/` (có chứa `images/`)

**Cách upload:**
- Click vào icon **"..."** hoặc **"Upload"** ở file explorer
- Chọn tất cả files và folders trong thư mục `json-server-heroku`
- Hoặc kéo thả files vào Replit

## Bước 3: Cài đặt dependencies

Trong Shell tool của Replit, chạy:

```bash
npm install
```

## Bước 4: Chạy server

Trong Shell tool, chạy:

```bash
npm start
```

Server sẽ chạy và hiển thị URL của Replit (ví dụ: `https://my-json-server.repl.co`)

## Bước 5: Test các endpoints

Sau khi server chạy, mở Webview tool và test các URL sau:

- **Base URL**: `https://<repl_name>.repl.co`
- **Dishes**: `https://<repl_name>.repl.co/dishes`
- **Leaders**: `https://<repl_name>.repl.co/leaders`
- **Comments**: `https://<repl_name>.repl.co/comments`
- **Promotions**: `https://<repl_name>.repl.co/promotions`
- **Images**: `https://<repl_name>.repl.co/images/logo.png`

Thay `<repl_name>` bằng tên Repl bạn đã đặt ở Bước 1.

## Lưu ý

- Server sẽ tự động chạy khi bạn mở Replit
- Nếu server không chạy, click vào nút **"Run"** hoặc chạy lại `npm start`
- URL của bạn sẽ có dạng: `https://<repl_name>.repl.co`

