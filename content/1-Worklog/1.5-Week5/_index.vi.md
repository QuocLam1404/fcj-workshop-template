---
title: "Tuần 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

# TUẦN 5 WORKLOG

### Mục tiêu tuần 5:

* Khởi động dự án LingoRise: xây dựng đề xuất dự án, thiết kế kiến trúc hệ thống, và thiết lập repository.
* Nghiên cứu tài liệu và xây dựng giải pháp tích hợp cổng thanh toán tự động Sepay.
* Triển khai giải pháp AI tự động tạo câu hỏi trắc nghiệm từ nội dung đề thi dạng Markdown sao chép trên mạng.
* Nghiên cứu cách khắc phục các lỗi phát sinh từ bộ phân tích câu hỏi của AI (cắt cụt JSON, phản hồi kèm giải thích, lỗi đáp án).

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 2 | - Phác thảo đề xuất dự án, xác định stack dịch vụ AWS chính và khởi tạo cấu trúc monorepo cho frontend (`lingorise-app`) và backend (`lingorise-backend`) | 18/05/2026 | 18/05/2026 | <https://docs.aws.amazon.com/> |
| 4 | - Nghiên cứu tài liệu API của Sepay: phân tích cấu trúc webhook callback từ ngân hàng, các tham số đầu vào và cơ chế kiểm tra chữ ký số (signature) | 20/05/2026 | 20/05/2026 | <https://docs.sepay.vn/> |
| 5 | - Xây dựng API route `/api/v1/payments/sepay-webhook` trong Express backend để tiếp nhận payload và trích xuất thông tin chuyển khoản từ ngân hàng | 21/05/2026 | 21/05/2026 | <https://expressjs.com/> |
| 6 | - **Thử nghiệm bộ phân tích đề thi Markdown bằng AI:** Thử nghiệm sao chép dữ liệu đề thi thô dạng Markdown từ các nguồn trên mạng cho AI tự tạo câu hỏi <br> - Xử lý lỗi phát sinh: 1) AI tự trả lời thêm text giải thích ngoài JSON (khắc phục bằng Regex parser `extractJsonObject()`), 2) JSON bị cắt giữa chừng (tăng `max_tokens` lên 4000+), 3) Lỗi sai lệch đáp án key (khắc phục bằng ràng buộc trích xuất chuỗi bằng chứng `excerpt` chính xác từ passage và validate ở server) | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Tuần 5 Thành tựu:

* **Khởi tạo hạ tầng dự án**: Thiết lập thành công monorepo, database migrations ban đầu và chuẩn bị môi trường triển khai SAM.
* **Nắm bắt giải pháp Sepay**: Hiểu rõ luồng gửi và nhận thông báo biến động số dư từ Sepay để ánh xạ vào database của LingoRise.
* **Thiết kế Database thanh toán**: Thiết kế hoàn chỉnh lược đồ lưu trữ giao dịch tài chính dùng kiểu dữ liệu số nguyên để tránh lỗi tính toán sai số.
* **AI Question Bank Generator**: Xây dựng thành công pipeline biến các tài liệu đề thi thô dạng Markdown sao chép trên mạng thành các bộ câu hỏi JSON cấu trúc sạch sẽ.
* **Xử lý JSON bền bỉ**: Khắc phục triệt để lỗi AI trả thêm văn bản giải thích bằng cách áp dụng bộ tách chuỗi JSON dựa trên biểu thức chính quy (Regex).
* **Quy chuẩn Validation đầu ra**: Triển khai các bộ lọc xác thực tính đúng đắn của đáp án, chuẩn hóa định dạng TFNG và so khớp chính xác chuỗi bằng chứng từ bài đọc.
