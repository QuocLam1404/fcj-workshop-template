---
title: "Phát triển full-stack — Backend services, Frontend UI & Database"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# TUẦN 7 WORKLOG

### Mục tiêu tuần 7:

* Giải quyết triệt để lỗi thời gian phản hồi của AI khi tạo đề thi lúc nhanh lúc chậm gây nguy cơ timeout hệ thống.
* Triển khai kiến trúc xử lý bất đồng bộ (async queue) cho các tiến trình gọi API của AI.
* Cải tiến giao diện trang chủ Admin Dashboard để hiển thị các đề thi mới tạo và tối ưu hóa logic phê duyệt/kiểm duyệt đề ngay sau khi tạo xong.

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 3 | - Tách biệt tiến trình: chuyển luồng tạo đề thi của AI thành background job chạy bất đồng bộ qua hàng đợi (BullMQ) <br> - Trả về kết quả lập tức cho client kèm theo job ID để theo dõi tiến độ | 02/06/2026 | 02/06/2026 | <https://nodejs.org/api/> |
| 4 | - Tối ưu hóa prompt context và cấu hình caching cho các dữ liệu tĩnh <br> - Đo đạc và kiểm tra độ ổn định của tốc độ tạo đề thi sau khi áp dụng hàng đợi ngầm | 03/06/2026 | 03/06/2026 | <https://redis.io/documentation> |
| 5 | - Tái cấu trúc giao diện trang chủ Admin Dashboard (`/admin/dashboard`), bổ sung bảng danh sách các đề thi mới tạo cần kiểm duyệt (pending review) | 04/06/2026 | 04/06/2026 | <https://nextjs.org/docs/> |
| 6 | - Xây dựng logic kiểm duyệt nhanh tại trang chủ: thiết kế các nút Duyệt (Approve) và Từ chối (Reject) thao tác trực tiếp thay vì chuyển trang <br> - Chạy thử nghiệm và xác minh trạng thái chuyển đổi trong DB | 05/06/2026 | 05/06/2026 | <https://playwright.dev/> |

### Tuần 7 Thành tựu:

* **Ổn định tốc độ tạo đề bằng AI**: Khắc phục hoàn toàn lỗi xử lý chậm và nghẽn mạng nhờ triển khai hàng đợi xử lý ngầm và tối ưu hóa kích thước prompt.
* **Rút gọn quy trình kiểm duyệt**: Tích hợp danh sách đề thi chờ duyệt trực tiếp lên trang chủ Dashboard giúp quản trị viên nắm bắt tức thời.
* **Logic phê duyệt một chạm**: Thiết lập các nút phê duyệt nhanh tại trang chủ, cập nhật tức thì trạng thái đề thi trong cơ sở dữ liệu PostgreSQL.
* **Nâng cao tính chịu tải**: Luồng tạo đề được phân tách giúp server backend hoạt động mượt mà, không bị treo khi nhiều yêu cầu tạo đề diễn ra cùng lúc.
* **Bảo mật và Nguyên tử dữ liệu**: Đảm bảo luồng kiểm duyệt nhanh thực hiện thông qua các API endpoints được bảo mật và bọc trong transaction để tránh lỗi đồng bộ dữ liệu.
