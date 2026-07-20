---
title: "S3, RDS, DynamoDB & IAM"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

# TUẦN 2 WORKLOG

### Mục tiêu tuần 2:

* Áp dụng quản lý định danh nâng cao và truy cập tài nguyên an toàn bằng IAM Roles.
* Thiết lập giải pháp lưu trữ dữ liệu an toàn, chống ghi đè trên Amazon S3 với Bucket Policy và Object Versioning.
* Nghiên cứu, cấu hình và triển khai các hệ quản trị cơ sở dữ liệu quan hệ (RDS PostgreSQL) và phi quan hệ (DynamoDB).
* Kết nối an toàn giữa các máy chủ tính toán (EC2) và cơ sở dữ liệu (RDS) thông qua các lớp bảo mật VPC.

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 2 | - Thiết lập thuộc tính Amazon S3: Kích hoạt Versioning bảo vệ đối tượng, bật mã hóa mặc định <br> - Viết custom Bucket Policy để chỉ cho phép các IP đáng tin cậy truy xuất dữ liệu | 27/04/2026 | 27/04/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/> |
| 4 | - Nghiên cứu sâu về phân quyền IAM: Tạo các JSON policy tùy biến <br> - Tạo IAM Role chuyên biệt gắn vào EC2 Instance Profile giúp EC2 tự xác thực với S3 mà không cần lưu trữ key tĩnh | 29/04/2026 | 29/04/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/> |
| 5 | - Cấu hình Security Group cho cơ sở dữ liệu để chỉ cho phép nhận kết nối từ Security Group của EC2 <br> - Viết code kết nối thử nghiệm từ máy ảo EC2 đến cơ sở dữ liệu RDS | 30/04/2026 | 30/04/2026 | <https://docs.aws.amazon.com/vpc/> |

### Tuần 2 Thành tựu:

* **Bảo mật dữ liệu nâng cao**: Quản lý S3 hiệu quả bằng cách áp dụng mã hóa, ngăn ngừa xóa nhầm nhờ Versioning và phân quyền chặt chẽ với Bucket Policy.
* **Làm chủ Database đa dạng**: Có kinh nghiệm thực tế triển khai và vận hành cả RDS (SQL) lẫn DynamoDB (NoSQL), nắm rõ ưu/nhược điểm từng loại.
* **Bảo mật cấp độ ứng dụng**: Loại bỏ hoàn toàn rủi ro lộ mã bảo mật nhờ ứng dụng IAM Role thay thế cho Access Key tĩnh trên EC2.
* **Thiết lập mạng nội bộ an toàn**: Cách ly thành công cơ sở dữ liệu trong mạng riêng tư, kiểm soát lưu lượng truy cập bằng quy tắc Security Group chéo.
* **Tích hợp hệ thống thành công**: Hoàn thành kiểm thử liên kết ứng dụng EC2 - RDS - S3 hoạt động ổn định và an toàn.
