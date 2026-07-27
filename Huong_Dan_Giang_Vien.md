# 👑 HƯỚNG DẪN DÀNH CHO GIẢNG VIÊN VÀ QUẢN LÝ
**Hệ thống Quản lý & Đồng bộ Bài nộp Python Core - Rikkei Academy**

---

## 🔑 1. Đăng nhập Bảng Quản Lý Giảng Viên
- Tại trang Portal (`index.html`) hoặc bất kỳ trang bài học nào (Bài 1 ➔ Bài 4), các thầy/cô nhấn vào nút **`🔑 Đăng Nhập Giảng Viên`** trên góc phải màn hình.
- Nhập mật khẩu quản trị: **`rikkeiedu`**
- Nhấn **Xác nhận**. Bảng quản lý tổng hợp dành riêng cho Giảng viên sẽ lập tức hiển thị.

---

## 📊 2. Các tính năng quản lý bài nộp

### A. Theo dõi sỉ số bài nộp theo Lớp (Realtime)
- Bảng quản lý tự động thống kê số lượng sinh viên đã nộp bài theo từng lớp cụ thể:
  - **Khu vực Hà Nội:** `HN-KS25-CNTT1` ➔ `HN-KS25-CNTT8`
  - **Khu vực Hồ Chí Minh:** `HCM-KS25-CNTT5` ➔ `HCM-KS25-CNTT8`

### B. Lọc dữ liệu linh hoạt
- **Lọc theo Bài học:** Xem bài nộp của riêng Ngày 1, Ngày 2, Ngày 3, Ngày 4...
- **Lọc theo Lớp học:** Chọn một lớp bất kỳ để xem danh sách sinh viên lớp đó đã nộp bài hay chưa.

### C. Xuất Báo Cáo File Excel (`.xls`)
- Nhấn nút **`📊 Xuất File Excel Chuẩn Format`**.
- Hệ thống sẽ tự động xuất ra file Excel được trình bày đẹp mắt, gom nhóm sẵn theo từng Lớp và từng Bài học để thầy/cô lưu trữ hoặc gửi báo cáo trung tâm.

---

## 🔗 3. Hướng dẫn kết nối Đồng bộ 2 chiều với Google Sheet

Để bài nộp của sinh viên tự động đẩy về file Google Sheet quản lý riêng của thầy/cô:

1. **Bước 1:** Mở file Google Sheet của thầy/cô ➔ Vào **Extensions (Tiện ích mở rộng)** ➔ Chọn **Apps Script**.
2. **Bước 2:** Dán đoạn mã script Webhook (đã cung cấp trong tài liệu Google Sheet) ➔ Bấm **Deploy (Triển khai)** dưới dạng **Web App**.
3. **Bước 3:** Đặt quyền *Anyone (Bất kỳ ai)* có thể truy cập ➔ Copy đường link Webhook dạng `https://script.google.com/macros/s/.../exec`.
4. **Bước 4:** Tại Bảng Quản Lý Giảng Viên trên trang web, dán đường link Webhook vào ô **"Cấu hình Webhook Google Sheet"** và nhấn **Lưu URL**.
5. Từ thời điểm này, tất cả bài nộp của sinh viên sẽ tự động chảy về file Google Sheet của thầy/cô theo thời gian thực!

---

## 🗑️ 4. Xóa bài nộp trùng lặp hoặc nộp nhầm
- Trong danh sách bài nộp, ở mỗi dòng sinh viên đều có nút **`🗑️ Xóa`**.
- Khi thầy/cô bấm xóa, hệ thống sẽ xóa bài nộp đó trên trang web đồng thời tự động gửi lệnh xóa tương ứng về file Google Sheet để dữ liệu 2 bên luôn đồng bộ.
