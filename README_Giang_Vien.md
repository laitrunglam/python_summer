# 📖 HƯỚNG DẪN CÁCH TẠO BÀI HỌC MỚI (DÀNH CHO GIẢNG VIÊN)
**Chương trình: Python Core & FastAPI • Rikkei Academy**

Tài liệu này hướng dẫn các thầy/cô cách tạo 1 bài học mới (Từ **Bài 05 đến Bài 14**) một cách **đơn giản nhất** chỉ trong 3 bước. 

Sau khi làm xong, các thầy/cô gửi lại folder bài học (ví dụ `day05`) cho thầy **Lại Trung Lâm** để tích hợp trực tiếp vào hệ thống Portal chung.

---

## 📁 BƯỚC 1: TẠO THƯ MỤC BÀI HỌC
Tạo 1 thư mục mới trùng tên với ngày học (viết thường).
- Ví dụ bài Ngày 05: Tạo thư mục **`day05`**

Bên trong thư mục **`day05`**, các thầy/cô chỉ cần chuẩn bị đúng **2 file**:
1. `day05_python_core.html` (Giao diện bài học HTML)
2. `BT_Day05_PythonCore.docx` (File Word phiếu bài tập đính kèm cho sinh viên)

```text
📂 day05/
   ├── 📄 day05_python_core.html
   └── 📝 BT_Day05_PythonCore.docx
```

---

## 💻 BƯỚC 2: TẠO FILE HTML BÀI HỌC (`day05_python_core.html`)
Các thầy/cô **chỉ cần copy toàn bộ file mẫu `day04/day04_python_core.html`** dán sang `day05/day05_python_core.html`, sau đó chỉnh sửa 3 chỗ đơn giản sau:

### 1. Đổi Mã Bài Học & Tiêu Đề Bài (ở đầu đoạn Script `<script>`):
```javascript
const CURRENT_LESSON_ID = "DAY_05"; // Đổi thành mã bài tương ứng (DAY_05, DAY_06...)
```

### 2. Soạn Đề Bài & Code Mẫu (Khung VS Code Dark):
Trong phần giao diện HTML, tìm ô `<textarea id="day5_ex1_code" class="code-textarea">`:
- Điền đoạn code Python mẫu của bài tập.
- Các vị trí yêu cầu sinh viên hoàn thiện thì điền dấu ba chấm **`...`** (TODO).

### 3. Cấu Hình Kiểm Tra Testcase (CodeLearn Style):
Trong hàm `checkDay5Exercise1()`:
- Đổi điều kiện kiểm tra từ khóa Output kỳ vọng:
```javascript
const noPlaceholder = !hasUnfilledPlaceholders(code);
const isNoErr = !txt.includes('❌ Lỗi') && !txt.includes('SyntaxError');

// Đánh dấu Passed nếu Output in ra từ khóa chính xác của bài
let tc1 = noPlaceholder && isNoErr;
```

---

## ⚙️ 4 THÀNH PHẦN ĐÃ CÓ SẴN (KHÔNG CẦN CHỈNH SỬA):
Khi copy từ bài mẫu `day04`, các tính năng sau đã được thiết lập sẵn 100%:
1. **Khung soạn thảo & Chạy thử Python:** Tự động nạp qua Pyodide CDN siêu nhẹ.
2. **Nút Mở Khóa File Word:** Tự động mở khóa nút tải màu đỏ `BT_Day05_PythonCore.docx` khi sinh viên vượt qua 4/4 Testcase.
3. **Form Nộp Bài Sinh Viên:** Đã có đủ danh sách 7 lớp (`CNTT1` ➔ `CNTT6` và `CNTT8`).
4. **Bảng Quản Lý Giảng Viên:** Đã tích hợp sẵn ô dán Google Sheet Webhook URL và nút xuất Báo Cáo Excel.

---

## 📤 BƯỚC 3: BÀN GIAO FILE BÀI HỌC
Sau khi hoàn thành:
- Các thầy/cô nén thư mục (ví dụ `day05.zip`) gửi cho thầy **Lại Trung Lâm** qua Lark / Zalo.
- Hoặc push trực tiếp lên GitHub: [https://github.com/laitrunglam/python_summer](https://github.com/laitrunglam/python_summer)

Thầy Lâm sẽ copy thư mục `day05` vào dự án là bài học mới sẽ lập tức hoạt động chuẩn xác trên Portal!
