# Release Notes – Zalo for Linux v1.1.3

Chào mừng bạn đến với bản phát hành **Zalo for Linux v1.1.3** – Bản port desktop client không chính thức của Zalo dành cho hệ điều hành Linux (dựa trên bản Zalo macOS và vận hành qua runtime Electron 22.3.27).

---

## 🚀 Hướng dẫn khởi chạy nhanh (AppImage)

Không cần cài đặt phức tạp, bạn chỉ cần tải gói AppImage độc lập:

1. Tải tệp tin `Zalo-v1.1.3-x86_64.AppImage` từ mục **Assets** bên dưới.
2. Cấp quyền thực thi cho tệp tin:
   ```bash
   chmod +x Zalo-v1.1.3-x86_64.AppImage
   ```
3. Khởi chạy ứng dụng:
   ```bash
   ./Zalo-v1.1.3-x86_64.AppImage
   ```

*(Hoặc cài đặt tự động qua mã nguồn bằng cách clone repo và chạy `./install.sh`)*

---

## ✨ Tính năng hoạt động (What's Working)

- **Nhắn tin & Trò chuyện**: Gửi nhận tin nhắn văn bản, hình ảnh, tập tin, sticker và emotion mượt mà.
- **Cơ sở dữ liệu tin nhắn cục bộ**: Tích hợp binary `node_sqlite3.node` (Linux ELF) thay thế cho binary macOS, giúp lưu trữ và đồng bộ tin nhắn ngay trên máy.
- **Khôi phục dữ liệu sao lưu (`db-cross-v4`)**: Engine C++ được thiết kế lại để giải mã và giải nén các container sao lưu ZDB4.0 (AES-256-CBC & LZMA2), hỗ trợ khôi phục đầy đủ lịch sử trò chuyện.
- **Xem ảnh Zalo Photo**: Cửa sổ xem ảnh đã được tích hợp khung cửa sổ chuẩn của hệ điều hành Linux (đầy đủ nút Đóng / Thu nhỏ / Phóng to).
- **Hỗ trợ tự động môi trường Debian / Ubuntu**: Script khởi chạy tự động nhận diện hệ điều hành và thêm cờ `--no-sandbox` tương thích.

---

## ⚠️ Hạn chế đã biết (Known Limitations)

- ❌ **Gọi thoại và gọi video (`zcall`)**: Chưa hỗ trợ do phụ thuộc vào VoIP/WebRTC stack độc quyền với mã hóa ZRTP viết riêng cho macOS.
- ❌ **Ảnh JPEG-XL (`zjxl`) & Thumbnail MP4 (`mp4thumb`)**: Chưa hỗ trợ xem ảnh định dạng `.jxl` và trích xuất thumbnail preview cho tệp video `.mp4`.
- ❌ **Kiến trúc phần cứng**: Hiện tại mới chỉ hỗ trợ kiến trúc `x86_64` (Intel/AMD 64-bit), chưa có bản build cho ARM64.

---

## 🤝 Đóng góp & Báo lỗi

- Mã nguồn: [https://github.com/Nhatgreen/Zalo-for-linux](https://github.com/Nhatgreen/Zalo-for-linux)
- Báo lỗi hoặc đóng góp bản vá: [GitHub Issues](https://github.com/Nhatgreen/Zalo-for-linux/issues)

*Disclaimer: Đây là bản port cộng đồng phi thương mại, không có bất kỳ liên kết hay tài trợ chính thức nào từ VNG Corporation.*
