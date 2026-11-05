# Jokes API - Vietnamese Jokes Collection

API đơn giản chứa các câu chuyện cười tiếng Việt để sử dụng cho Zalo Bot "Joke of the Day".

## 📝 Cấu trúc dữ liệu

```json
{
  "version": "1.0.0",
  "language": "vi",
  "lastUpdated": "2026-11-05",
  "jokes": [
    {
      "id": 1,
      "content": "Nội dung joke...",
      "category": "classic"
    }
  ],
  "totalJokes": 15,
  "categories": ["classic", "wordplay", ...]
}
```

## 🚀 Cách deploy lên GitHub Pages

### Bước 1: Tạo repository mới trên GitHub
1. Đăng nhập GitHub
2. Tạo repository mới tên `jokes-api` (hoặc tên bạn thích)
3. Chọn **Public** để có thể truy cập qua GitHub Pages

### Bước 2: Upload file jokes.json
```bash
# Clone repository về máy
git clone https://github.com/YOUR_USERNAME/jokes-api.git
cd jokes-api

# Copy file jokes.json vào
cp /path/to/github-pages/jokes.json .

# Commit và push
git add jokes.json
git commit -m "Add Vietnamese jokes data"
git push origin main
```

### Bước 3: Bật GitHub Pages
1. Vào **Settings** của repository
2. Chọn **Pages** ở menu bên trái
3. Trong phần **Source**, chọn `main` branch và folder `/root`
4. Click **Save**
5. Sau vài phút, website sẽ được publish tại: `https://YOUR_USERNAME.github.io/jokes-api/`

### Bước 4: Kiểm tra API
Truy cập URL: `https://YOUR_USERNAME.github.io/jokes-api/jokes.json`

Bạn sẽ thấy dữ liệu JSON được trả về.

## 🔗 Sử dụng API trong Bot

Cập nhật file `.env` của bot:
```env
JOKES_API_URL=https://YOUR_USERNAME.github.io/jokes-api/jokes.json
```

## ➕ Cách thêm jokes mới

1. Mở file `jokes.json`
2. Thêm object mới vào mảng `jokes`:
```json
{
  "id": 16,
  "content": "Nội dung joke mới...",
  "category": "life"
}
```
3. Cập nhật `totalJokes` tăng lên 1
4. Commit và push lên GitHub
5. Chờ vài phút để GitHub Pages cập nhật

## 📊 Các loại jokes hiện có

- `classic` - Jokes kinh điển
- `wordplay` - Chơi chữ
- `kids` - Dành cho trẻ em
- `family` - Gia đình
- `technology` - Công nghệ
- `life` - Cuộc sống
- `health` - Sức khỏe
- `motivation` - Động lực
- `riddle` - Câu đố
- `food` - Đồ ăn
- `money` - Tiền bạc

## 📄 License

Free to use - Thoải mái sử dụng và chia sẻ! 🎉
