# 🎂 Birthday Celebration Web App — Chúc Mừng Sinh Nhật

Một trang web chúc mừng sinh nhật tương tác (interactive single-page web app) nhẹ nhàng, tinh tế và đầy đủ hiệu ứng âm thanh, nến, pháo hoa, bóng bay lời chúc và hộp quà bất ngờ.

Được thiết kế để chạy trực tiếp trên trình duyệt hoặc triển khai miễn phí qua **GitHub Pages**.

---

## ✨ Tính năng nổi bật

- 🕯️ **Tương tác thổi nến**: Chạm vào bánh sinh nhật để thổi tắt từng ngọn nến tương ứng với số tuổi, căn phòng tối dần theo thời gian thực.
- 🎆 **Hiệu ứng tiệc tùng**: Sau khi thổi hết nến, đèn tự động bật sáng kèm pháo giấy (confetti) rực rỡ và phát nhạc chúc mừng sinh nhật.
- 🎁 **Hộp quà blindbox & bó hoa**: Bóc quà tương tác với những quả bóng bay mang theo từng lời chúc ý nghĩa.
- 🌓 **Giao diện Light / Dark Mode**: Dễ dàng chuyển đổi giữa chủ đề sáng và tối.
- 🔊 **Trình phát nhạc tích hợp**: Bật/tắt nhạc nền tuỳ thích, mượt mà trên cả máy tính và điện thoại.

---

## 📁 Cấu trúc thư mục

```text
sinh_nhat/
├── .gitignore             # Bỏ qua các file tạm/hệ thống
├── README.md              # Tài liệu giới thiệu & hướng dẫn triển khai
├── index.html             # Mã nguồn ứng dụng (HTML/CSS/JS thuần, không cần build)
└── khuc_hat_mung_sn.mp3   # Nhạc nền chúc mừng sinh nhật
```

---

## ⚙️ Hướng dẫn tuỳ chỉnh nội dung

Bạn có thể dễ dàng sửa lại tên người nhận, số tuổi và các lời chúc trực tiếp trong file `index.html`. Tìm đoạn mã `CAU_HINH` (khoảng dòng 1135):

```javascript
const CAU_HINH = {
  ten: "Minh Tâm",                  // Tên (hoặc biệt danh) người nhận
  tuoi: 23,                         // Số tuổi = số ngọn nến = số lần chạm
  nhac: "khuc_hat_mung_sn.mp3",     // Tên file nhạc, đặt cùng thư mục với index.html

  // Danh sách lời chúc trong bóng bay blindbox (thêm/bớt tùy ý)
  loiChuc: [
    "Tuổi 23: vui, vui nữa, vui mãi",
    "Chúc anh không phải nói \"không sao đâu\" những lúc thật ra có sao.",
    "Chúc bạn tìm được công việc mình thích, đồng nghiệp thân thiện",
    // ...
  ],

  // Lời chúc cuối cùng (xuất hiện sau khi mở hết bóng bay)
  loiCuoi: "Hết lời chúc rồi, nhưng mà sinh nhật vui nha anh trai."
};
```

> **Lưu ý:**
> - Mỗi lời chúc nằm trong cặp dấu ngoặc kép `"..."` và kết thúc bằng dấu phẩy `,` (trừ dòng cuối cùng).
> - Nếu trong lời chúc có dấu ngoặc kép, hãy dùng `\"` hoặc dấu nháy đơn `'`.

---

## 🚀 Triển khai miễn phí lên GitHub Pages

Để chia sẻ link cho người nhận xem trực tiếp trên mạng:

1. **Tạo Repository mới trên GitHub**:
   - Truy cập [github.com/new](https://github.com/new).
   - Đặt tên repository (ví dụ: `sinh-nhat`).
   - Đặt chế độ **Public**.
   - Không cần tích chọn *Initialize with README*.
2. **Đẩy mã nguồn lên GitHub** (xem các lệnh git ở bên dưới).
3. **Kích hoạt GitHub Pages**:
   - Trong repository trên GitHub, chọn tab **Settings** → chọn **Pages** ở cột menu bên trái.
   - Tại mục **Build and deployment** > **Branch**: Chọn nhánh `main`, thư mục `/ (root)`.
   - Nhấn **Save**.
4. **Nhận link chia sẻ**:
   - Sau khoảng 1–2 phút, tải lại trang Pages, bạn sẽ nhận được đường link có định dạng:
     ```
     https://<ten-tai-khoan>.github.io/<ten-repo>/
     ```
   - Gửi đường link này đến người nhận! 🎉

---

## 🛠️ Công nghệ sử dụng

- **HTML5 / Vanilla CSS3 / JavaScript (ES6+)**: Không cần thư viện ngoài hay cài đặt `node_modules`.
- **Google Fonts**: `Dancing Script` & `Quicksand`.
- **Canvas Confetti & SVG Animations**: Hiệu ứng mượt mà, tối ưu hiệu năng.
