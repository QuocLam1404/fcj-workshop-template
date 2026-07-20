---
title: "Tuần 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

# TUẦN 4 WORKLOG

### Mục tiêu tuần 4:

* Thiết kế và xây dựng giao diện trang Dashboard dành cho quản trị viên (Admin) của nền tảng LingoRise, tập trung vào vận hành nội dung và ghi nhận lịch sử hoạt động.
* Thiết lập hệ thống phân quyền (RBAC) chặt chẽ ở backend để bảo vệ các tuyến API nhạy cảm.
* Xây dựng luồng phê duyệt và kiểm tra câu hỏi học tập (`/admin/content-operations`) tích hợp chẩn đoán từ trí tuệ nhân tạo (AI).

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 3 | - Phát triển middleware phân quyền dựa trên vai trò (RBAC - Role-Based Access Control) ở phía Express backend <br> - Chặn và kiểm tra quyền admin dựa trên JWT tokens trước khi cho phép thay đổi dữ liệu | 12/05/2026 | 12/05/2026 | <https://expressjs.com/> |
| 4 | - Định nghĩa database schema cho lịch sử hoạt động (Audit Logs) trong hệ cơ sở dữ liệu PostgreSQL <br> - Viết các hàm tự động ghi nhận hoạt động admin (ví dụ: log `admin.question_bank_quality_flagged`) | 13/05/2026 | 13/05/2026 | <https://www.postgresql.org/docs/> |
| 6 | - Kiểm thử tích hợp toàn trình các tính năng thay đổi dữ liệu của admin <br> - Viết các ca kiểm thử bảo mật thử nghiệm truy cập trái phép vào tài khoản admin | 15/05/2026 | 15/05/2026 | <https://playwright.dev/> |

### Tuần 4 Thành tựu:

* **Xây dựng giao diện quản trị**: Thiết kế thành công trang Dashboard cao cấp bằng Next.js hỗ trợ quản lý ngân hàng câu hỏi và bài đọc với lượng dữ liệu lớn.
* **Bảo mật phân quyền vững chắc**: Triển khai thành công middleware kiểm tra vai trò người dùng ở backend (RBAC), chặn đứng truy cập trái phép.
* **Hệ thống Audit Logs minh bạch**: Lưu trữ toàn bộ lịch sử thao tác dữ liệu nhạy cảm của Admin vào bảng cơ sở dữ liệu PostgreSQL một cách chính xác.
* **Tương tác trực quan cùng AI**: Hoàn thành luồng kiểm duyệt kết nối các cờ báo chất lượng câu hỏi từ AI lên màn hình quản lý của Admin.
* **Đạt chuẩn kiểm thử bảo mật**: Hoàn thiện bộ kiểm thử tự động, xác nhận độ an toàn tuyệt đối trước các truy cập leo thang đặc quyền.
