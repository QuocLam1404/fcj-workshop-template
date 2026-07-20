---
title: "Tuần 12 Worklog"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

# TUẦN 12 WORKLOG

### Mục tiêu tuần 12:

* Thực hiện kiểm thử tải (Load Testing / Stress Testing) hệ thống để kiểm tra khả năng chịu tải của các AWS Lambda functions.
* Tinh chỉnh cấu hình tài nguyên (Memory, Concurrency) của Lambda và tối ưu hóa truy vấn Database.
* Tiến hành kiểm tra bảo mật (Security Audit) mã nguồn và rà soát phân quyền IAM Roles theo nguyên tắc đặc quyền tối thiểu.
* Đóng gói mã nguồn dự án (v1.0.0 Release), viết tệp tin nhật ký thay đổi (Changelog) và hoàn tất bàn giao kỹ thuật cuối khóa.

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 2 | - Thiết lập kịch bản kiểm thử tải (Load Testing scripts) bằng công cụ Artillery/k6 giả lập 500+ người dùng đồng thời nộp bài thi <br> - Đo lường độ trễ phản hồi (Response Latency) của API Gateway | 06/07/2026 | 06/07/2026 | <https://artillery.io/docs/> |
| 3 | - Thực hiện chạy thử nghiệm tải trên môi trường Staging <br> - Phân tích logs, giám sát tỷ lệ lỗi (Error Rate) và mức độ chiếm dụng CPU/Memory của RDS PostgreSQL | 07/07/2026 | 07/07/2026 | <https://docs.aws.amazon.com/rds/> |
| 5 | - Thực hiện rà soát bảo mật (Security Audit): Kiểm tra phân quyền IAM policies của các dịch vụ, đóng bớt các cổng mạng dư thừa trên VPC Security Groups | 09/07/2026 | 09/07/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/> |

### Tuần 12 Thành tựu:

* **Hoàn thành kiểm thử tải**: Xác định chính xác các điểm nghẽn hiệu năng của API Gateway và Lambda function dưới tải trọng lớn.
* **Tối ưu hóa tài nguyên hiệu quả**: Giảm thiểu độ trễ phản hồi API trung bình từ ~1.2 giây xuống ~350 mili giây nhờ phân bổ bộ nhớ Lambda và tối ưu SQL.
* **Bảo mật hệ thống vững chắc**: Giới hạn quyền truy cập an toàn cho các IAM Roles và cô lập thành công database RDS trong mạng nội bộ VPC.
* **Đóng gói và Bàn giao thành công**: Phát hành bản release chính thức v1.0.0 của LingoRise trên GitHub đi kèm đầy đủ tài liệu hướng dẫn kỹ thuật hoàn chỉnh.
