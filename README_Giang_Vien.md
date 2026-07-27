# 🛠️ HƯỚNG DẪN DÀNH CHO GIẢNG VIÊN ĐÓNG GÓP BÀI HỌC (NGÀY 05 -> NGÀY 14)

Chào các thầy/cô giảng viên! Nhằm thống nhất cấu trúc hệ thống bài học Python Core & FastAPI, khi xây dựng nội dung bài học mới (Từ Ngày 05 đến Ngày 14), các thầy/cô vui lòng thực hiện theo hướng dẫn sau:

---

## 📁 1. CẤU TRÚC THƯ MỤC BÀI HỌC CHUẨN

Mỗi ngày học tạo 1 thư mục riêng theo chuẩn đặt tên:
- `day05/` (cho Ngày 05: FastAPI Architecture)
- `day06/` (cho Ngày 06: Pydantic Schemas)
- ...
- `day14/` (cho Ngày 14: Thi Thử Mock Exam)

Bên trong thư mục gồm **2 file bắt buộc**:
1. `day05_python_core.html` (File giao diện HTML bài học)
2. `BT_Day05_PythonCore.docx` (File Word phiếu bài tập đính kèm cho học viên)

---

## 💻 2. KHÔNG CẦN KÈM BỘ NẠP PYODIDE HẶC THƯ MỤC NẶNG

Hệ thống đã tự động cấu hình **Pyodide CDN trực tuyến chuẩn**, các thầy/cô chỉ cần copy cấu hình script Pyodide chuẩn từ bài mẫu `day04/day04_python_core.html`.

---

## ⚙️ 3. CÁC THÀNH PHẦN CHUẨN TRONG FILE HTML BÀI HỌC

1. **Thanh Header & Navigation:** Giữ đúng định dạng logo Rikkei Academy, nút Đăng nhập Quản lý Giảng viên (`pass: rikkeiedu`).
2. **Khung Soạn Thảo VS Code Dark:** Sử dụng thẻ `<textarea class="code-textarea">` với vị trí cần điền code đánh dấu là `...` (TODO).
3. **Bộ Kiểm Tra Testcase (CodeLearn Style):**
   - Đặt biến `const CURRENT_LESSON_ID = "DAY_05";` (hoặc Ngày tương ứng).
   - Hàm kiểm tra Testcase tự động mở khóa nút màu đỏ **`📥 Tải File Word Bài Tập (.docx)`** khi học viên đạt 4/4 PASSED.
4. **Form Nộp Bài Sinh Viên:** Giữ nguyên danh sách 7 lớp (`CNTT1` ➔ `CNTT6` và `CNTT8`).
5. **Footer Liên Hệ Lark:** Chứa mã QR Code liên hệ Lark của thầy Lại Trung Lâm ở cuối trang.
