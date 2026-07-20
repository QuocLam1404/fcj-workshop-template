---
title: "Tuần 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# TUẦN 6 WORKLOG

### Mục tiêu tuần 6:

* Khắc phục triệt để lỗi thiếu sơ đồ, hình ảnh minh họa trong các đề thi IELTS Reading được sao chép từ internet.
* Sửa lỗi phân giải câu hỏi điền khuyết (gap-fill) không hiển thị ô nhập văn bản (text input box) cho học viên ghi đáp án.
* Thiết lập logic chấm điểm chuẩn hóa không phân biệt chữ hoa/chữ thường (case-insensitive) và xây dựng logic tự động tạo đề thi.
* Phát triển công cụ tự động tải ảnh ngoại vi và lưu trữ tập trung trên hệ thống Amazon S3.

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 2 | - Kiểm tra lỗi học viên phản ánh không xem được hình vẽ/sơ đồ trong đề thi Reading <br> - Nghiên cứu lỗi giao diện phần thi điền khuyết (gap-fill/summary-completion) không hiển thị ô nhập liệu (text input box) cho học viên ghi đáp án | 25/05/2026 | 25/05/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html> |
| 3 | - Viết công cụ tự động quét văn bản Markdown của câu hỏi, trích xuất tất cả thẻ ảnh ngoại vi và tải lên Amazon S3 <br> - Xây dựng bộ phân tích biểu thức chính quy (regex parser) ở frontend để phát hiện các ký hiệu khoảng trống (ví dụ: `[1]` hoặc `___`) và thay thế bằng thẻ `<input>` nhập liệu | 26/05/2026 | 26/05/2026 | <https://nodejs.org/api/> |
| 5 | - Nâng cấp màn hình thi (`lingorise-app`) tích hợp bộ sinh URL tạm thời (S3 Pre-signed URL) từ backend <br> - Thiết kế logic tạo đề thi ở backend: tự động sắp xếp câu hỏi theo phần (Section), áp dụng quy tắc thứ tự câu hỏi và lưu cấu trúc đề thi hoàn chỉnh trong database | 28/05/2026 | 28/05/2026 | <https://react.dev/reference/react> |

### Tuần 6 Thành tựu:

* **Giải quyết dứt điểm lỗi thiếu ảnh**: Khắc phục hoàn toàn sự cố thiếu hình vẽ minh họa trong đề thi Reading của học viên.
* **Sửa lỗi hiển thị ô nhập điền khuyết**: Đã hiển thị đúng các ô nhập dữ liệu văn bản trong đề thi điền khuyết thông qua bộ phân tích regex.
* **Logic chấm điểm chuẩn xác**: Triển khai thuật toán so khớp không phân biệt chữ hoa thường (case-insensitive) và loại bỏ khoảng trắng thừa cho câu hỏi điền khuyết.
* **Tự động tạo cấu trúc đề thi**: Xây dựng cấu trúc xử lý backend tự động lắp ghép câu hỏi theo thứ tự chuẩn hóa của đề thi thực tế.
* **Tự động hóa luồng tải tài nguyên**: Triển khai thành công công cụ Node.js cào và lưu trữ tự động mọi file ảnh ngoại vi lên S3.
* **Migration cơ sở dữ liệu sạch**: Cập nhật chính xác và an toàn hàng loạt URL ảnh bị hỏng sang liên kết S3 nội bộ.
* **Bảo mật hiển thị Frontend**: Xây dựng component React hỗ trợ phân giải và hiển thị ảnh từ S3 Pre-signed URL động.
* **Tối ưu hóa giao diện thi**: Định dạng kích thước ảnh co giãn linh hoạt (responsive), loại bỏ hiện tượng giật màn hình (CLS) khi tải trang thi Reading.
