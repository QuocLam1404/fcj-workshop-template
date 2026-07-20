---
title: "Tuần 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

# TUẦN 8 WORKLOG

### Mục tiêu tuần 8:

* Hoàn thiện giao diện luồng thi cho học viên: xây dựng trang hiển thị kết quả với biểu đồ điểm số và màn hình xem lại đáp án chi tiết.
* Chuyển đổi toàn bộ giao diện thi và học sang thiết kế responsive ưu tiên mobile để đảm bảo tương thích đa thiết bị.
* Khắc phục lỗi quản lý phiên Cognito: token hết hạn giữa bài thi gây mất dữ liệu, triển khai middleware tự động làm mới token.
* Tích hợp module AI chấm bài Writing vào luồng nộp bài thi.

### Nhiệm vụ sẽ được thực hiện trong tuần này:

| Ngày | Nhiệm vụ | Bắt đầu ngày | Ngày hoàn thành | Tài liệu tham khảo |
| ---- | -------- | ------------- | --------------- | ------------------- |
| 2 | - Thiết kế và xây dựng trang tổng kết kết quả thi với bảng điểm phân loại theo từng kỹ năng (Listening/Reading/Writing/Speaking) <br> - Tích hợp component biểu đồ radar Chart.js để trực quan hóa phân bố band score | 08/06/2026 | 08/06/2026 | <https://www.chartjs.org/docs/> |
| 4 | - Sửa lỗi hết hạn token Cognito: học viên bị mất tiến trình bài thi khi access token hết hạn giữa phiên <br> - Triển khai interceptor tự động làm mới token trong Axios HTTP client để gia hạn token trước khi các lệnh gọi API bị lỗi | 10/06/2026 | 10/06/2026 | <https://docs.aws.amazon.com/cognito/> |
| 6 | - Kết nối module AI chấm bài Writing: gửi bài luận của học viên đến endpoint phân tích AI và hiển thị phản hồi có cấu trúc (task achievement, coherence, lexical resource, grammar) <br> - Kiểm thử end-to-end toàn bộ vòng đời bài thi trên cả trình duyệt desktop và mobile | 12/06/2026 | 12/06/2026 | <https://nextjs.org/docs/> |

### Tuần 8 Thành tựu:

* **Trực quan hóa kết quả thi**: Xây dựng trang tổng kết kết quả với biểu đồ radar hiển thị phân bố band score theo từng kỹ năng IELTS.
* **Màn hình xem lại đáp án**: Triển khai giao diện xem lại từng câu hỏi với chỉ thị màu sắc đúng/sai và giải thích từ AI.
* **Sửa lỗi token Cognito**: Khắc phục lỗi nghiêm trọng khiến học viên mất tiến trình thi do token hết hạn, bằng cách triển khai Axios interceptor tự động làm mới token.
* **Giao diện responsive mobile-first**: Chuyển đổi toàn bộ trang dành cho học viên sang bố cục responsive, sửa lỗi điều hướng cảm ứng trên thanh câu hỏi.
* **Tích hợp AI chấm bài Writing**: Kết nối module phân tích bài viết AI, cung cấp phản hồi có cấu trúc theo tiêu chí IELTS cho bài luận.
