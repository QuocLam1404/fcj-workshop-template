---
title: "Kiểm thử & tối ưu AI"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

# TUẦN 9 WORKLOG

### Mục tiêu tuần 9:

* Triển khai toàn bộ nền tảng LingoRise lên môi trường production AWS bằng SAM và Amplify.
* Cấu hình biến môi trường production, quản lý secrets, và chạy database migration trên Amazon RDS.
* Thiết lập CloudFront CDN distribution cho tài nguyên tĩnh frontend và phân phối media từ S3.
* Chạy smoke test trên production để xác nhận toàn bộ luồng người dùng hoạt động trên hạ tầng thực.

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 2 | - Chuẩn bị file SAM `template.yaml` cho production: cấu hình memory, timeout, và environment variables cho các Lambda function <br> - Chạy `sam build && sam deploy --guided` để provision toàn bộ Lambda functions và API Gateway endpoints | 15/06/2026 | 15/06/2026 | <https://docs.aws.amazon.com/serverless-application-model/> |
| 3 | - Triển khai frontend Next.js lên AWS Amplify Hosting với cấu hình tên miền tùy chỉnh <br> - Debug và sửa lỗi không khớp biến môi trường giữa local development và Amplify build settings (API base URL, Cognito pool IDs) | 16/06/2026 | 16/06/2026 | <https://docs.aws.amazon.com/amplify/> |
| 5 | - Tạo CloudFront distribution cho S3 bucket phục vụ hình ảnh đề thi và tài nguyên audio <br> - Cấu hình Origin Access Control (OAC) để giữ S3 bucket private trong khi phân phối nội dung qua CloudFront <br> - Thiết lập cache behaviors và chính sách TTL cho các loại tài nguyên khác nhau | 18/06/2026 | 18/06/2026 | <https://docs.aws.amazon.com/cloudfront/> |
| 6 | - Chạy smoke test production: đăng ký tài khoản mới → tạo phiên thi → nộp đáp án → xem kết quả <br> - Sửa lỗi cấu hình CORS trên API Gateway chặn request từ domain Amplify frontend <br> - Xác minh luồng xác thực Cognito hoạt động chính xác trên production | 19/06/2026 | 19/06/2026 | <https://docs.aws.amazon.com/apigateway/> |

### Tuần 9 Thành tựu:

* **Backend Production Hoạt Động**: Triển khai thành công toàn bộ Lambda functions và API Gateway routes qua SAM, với environment variables được cấu hình chính xác.
* **Frontend Hosting**: Triển khai frontend Next.js trên AWS Amplify với CI/CD tự động build khi push Git.
* **Database Sẵn Sàng Production**: Migration toàn bộ schema lên production RDS, xác minh tính toàn vẹn dữ liệu và seed dữ liệu tham chiếu thiết yếu.
* **Phân Phối CDN**: Cấu hình CloudFront với OAC để phân phối an toàn hình ảnh đề thi và file audio từ S3 bucket private.
* **Sửa Lỗi CORS**: Khắc phục lỗi CORS chỉ xuất hiện trên production khi API Gateway từ chối request từ domain Amplify frontend.
* **Xác Nhận End-to-End**: Xác nhận toàn bộ luồng học viên (đăng ký → thi → chấm điểm → xem lại) hoạt động trên hạ tầng AWS thực.
