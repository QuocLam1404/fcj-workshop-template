---
title: "Tuần 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

# TUẦN 3 WORKLOG

### Mục tiêu tuần 3:

* Làm chủ kiến trúc Serverless (AWS Lambda & API Gateway) thông qua phương pháp lập trình cặp cùng Trợ lý AI (AI Pair-programming).
* Nghiên cứu tích hợp các dịch vụ AI của AWS (Textract, Comprehend) và thiết kế Prompt Engineering.
* Ứng dụng Trợ lý AI vào quy trình làm việc hàng ngày để sinh mã, sửa lỗi cấu hình và tối ưu hóa hệ thống.

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 2 | - Tham vấn Trợ lý AI để phác thảo sơ đồ kiến trúc Serverless <br> - Phân tích ưu nhược điểm của các loại Trigger và cấu trúc mã nguồn Lambda | 04/05/2026 | 04/05/2026 | <https://docs.aws.amazon.com/lambda/> |
| 3 | - Sử dụng Trợ lý AI để sinh mã nguồn Node.js cho các Lambda function <br> - Cấu hình API Gateway và viết các template ánh xạ request/response | 05/05/2026 | 05/05/2026 | <https://docs.aws.amazon.com/apigateway/> |
| 4 | - Thiết lập Prompt Engineering cùng Trợ lý AI để định hình JSON schema cho kết quả xử lý <br> - Nghiên cứu tài liệu API của Textract để phục vụ trích xuất văn bản | 06/05/2026 | 06/05/2026 | <https://docs.aws.amazon.com/textract/> |
| 6 | - Kiểm thử tích hợp toàn trình luồng S3 -> Lambda -> Textract <br> - Cùng AI phân tích CloudWatch Logs để phát hiện chai sạn hiệu năng và viết tài liệu tổng kết tuần | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Tuần 3 Thành tựu:

* **Tối ưu tốc độ phát triển**: Đẩy nhanh tốc độ viết mã nguồn backend nhờ sự hỗ trợ sinh và gỡ lỗi code trực tiếp từ Trợ lý AI.
* **Xây dựng API Serverless**: Hoàn thành hệ thống RESTful API kết hợp Lambda và API Gateway bảo mật.
* **Nền tảng Prompt Engineering**: Xây dựng thành công các kịch bản Prompt chuẩn hóa để chuyển dữ liệu thô từ Textract sang JSON có cấu trúc.
* **Vận hành Event-Driven**: Triển khai thành công luồng xử lý tự động kích hoạt bởi event tải file lên S3.
* **Cải thiện chất lượng code**: Tận dụng AI để thực hiện đánh giá code (code review) cục bộ, đảm bảo tính bảo mật và sạch sẽ của mã nguồn.
