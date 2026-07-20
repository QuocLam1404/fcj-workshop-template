---
title: "Bàn giao, báo cáo tổng kết & thuyết trình"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

# TUẦN 10 WORKLOG

### Mục tiêu tuần 10:

* Sửa các lỗi production phát hiện trong quá trình smoke test Tuần 9: edge case trong chấm điểm thi, lỗi upload file, và sai lệch hiển thị giao diện.
* Tăng cường bảo mật nền tảng: triển khai input validation trên tất cả API endpoints, thêm rate limiting middleware, và đảm bảo sử dụng parameterized SQL queries.
* Tối ưu hiệu năng: giảm thời gian cold start Lambda, nén media assets trên S3, và tinh chỉnh execution plan truy vấn database.
* Dọn dẹp code cuối cùng và đảm bảo tất cả lệnh build/lint/test đều pass.

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 3 | - Triển khai Joi input validation schemas trên tất cả API Gateway endpoints <br> - Thêm express-rate-limit middleware ngăn chặn tấn công brute-force trên các endpoint xác thực <br> - Kiểm tra toàn bộ SQL queries để xác nhận đều sử dụng parameterized execution | 23/06/2026 | 23/06/2026 | <https://express-validator.github.io/docs/> |
| 4 | - Tối ưu cold start Lambda: giảm kích thước package bundle bằng tree-shaking các dependency không sử dụng <br> - Cấu hình provisioned concurrency cho Lambda handler nộp bài thi để đảm bảo thời gian phản hồi ổn định | 24/06/2026 | 24/06/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/provisioned-concurrency.html> |
| 6 | - Dọn dẹp code cuối cùng: xóa console.log, unused imports, và dead code branches <br> - Chạy bộ xác minh đầy đủ: `npm run build`, `npm run typecheck`, `npm run lint`, `npm test` — tất cả đều pass green | 26/06/2026 | 26/06/2026 | <https://eslint.org/docs/> |

### Tuần 10 Thành tựu:

* **Sửa Lỗi Chấm Điểm**: Sửa logic partial scoring cho câu hỏi Reading nhiều đáp án đã bị đếm thiếu số câu trả lời đúng.
* **Xử Lý Lỗi Upload**: Thêm error boundaries và thông báo người dùng cho file upload vượt quá giới hạn 5MB của S3.
* **Tăng Cường Bảo Mật**: Triển khai input validation, rate limiting, và xác nhận parameterized queries trên tất cả API endpoints.
* **Tối Ưu Cold Start**: Giảm thời gian cold start Lambda khoảng 40% thông qua tree-shaking dependency và provisioned concurrency trên các handler quan trọng.
* **Tối Ưu Tài Nguyên**: Nén toàn bộ ảnh đề thi qua Sharp, giảm kích thước ảnh trung bình 60% và cải thiện thời gian tải trang.
* **Hiệu Năng Database**: Thêm indexes chiến lược, giảm thời gian truy vấn trung bình cho tra cứu exam session từ ~200ms xuống ~15ms.
* **Codebase Sạch**: Tất cả lệnh build, lint, typecheck, và test đều pass green với zero warnings.
