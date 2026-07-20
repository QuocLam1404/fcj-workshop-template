---
title: "Chia sẻ, đóng góp ý kiến"
date: 2026-07-07
weight: 7
chapter: false
pre: " <b> 7. </b> "
---
# Chia sẻ và đóng góp ý kiến

## Phản hồi về chương trình thực tập FCAJ

### Những điều em thích (Dưới góc nhìn một người mới)
1. **Lộ trình học từ cơ bản đến nâng cao:** Giai đoạn nền tảng AWS 4 tuần đầu là bước chuẩn bị vô giá cho một newbie như em. Việc đi từ các dịch vụ đơn lẻ (EC2, S3, Lambda) đến cách phối hợp chúng giúp em không bị ngợp trước hệ sinh thái khổng lồ của AWS.
2. **Học thông qua dự án thực tế:** Triển khai **LingoRise** trên hạ tầng đám mây thực tế giúp em thấu hiểu những bài toán thực chiến mà một Cloud Engineer phải giải quyết như: bảo mật dữ liệu, phân quyền truy cập, thiết lập CDN và tối ưu hóa cơ sở dữ liệu.
3. **Môi trường rèn luyện tiếng Anh chuyên nghiệp:** Yêu cầu viết mọi tài liệu bằng tiếng Anh ban đầu là một thử thách lớn, nhưng đã giúp em làm quen với ngôn ngữ kỹ thuật quốc tế và tự tin hơn rất nhiều khi đọc tài liệu gốc của AWS.
4. **Sự hỗ trợ nhiệt tình từ Mentor:** Mentor luôn kiên nhẫn định hướng kiến trúc đám mây và chỉ dẫn các phương pháp deploy an toàn cho một người mới vào ngành.

### Đề xuất cải thiện
1. **Bổ sung các buổi sửa lỗi (Troubleshooting Workshops):** Đối với người mới bắt đầu, việc xử lý các lỗi như cấu hình VPC, lỗi định tuyến IP của NAT Gateway, hay lỗi CORS là cực kỳ khó khăn. Chương trình nên bổ sung các bài học tình huống thực tế để thực hành debug các lỗi kinh điển này.
2. **Các phiên Code Review hạ tầng:** Hướng dẫn cách tối ưu hóa các tệp cấu hình AWS SAM/Terraform chuẩn doanh nghiệp để tránh nợ kỹ thuật (technical debt) từ đầu.

---

## Chia sẻ với các bạn thực tập sinh tương lai

### Bí quyết cho người mới bắt đầu (Newbies)

**Tuần 1–4 (Giai đoạn nền tảng):**
- **Đừng chỉ đọc, hãy gõ lệnh:** Đừng chỉ click chuột trên Console. Hãy tập sử dụng AWS CLI để quen tay. Những dòng lệnh gõ trực tiếp sẽ giúp bạn nhớ bài lâu hơn.
- **Ghi chép log lỗi từ ngày đầu:** Đối với một Cloud Engineer tương lai, lỗi chính là bài học lớn nhất. Hãy ghi lại các lỗi deploy bạn gặp và cách bạn đã vượt qua nó vào worklog.

**Tuần 5–9 (Giai đoạn dự án):**
- **Tận dụng tài liệu chính thức (AWS Docs) và StackOverflow:** Khi gặp các lỗi deploy YAML phức tạp của SAM hoặc cấu hình IAM Policies chồng chéo, đừng đoán mò. Hãy chủ động tra cứu mã lỗi trên tài liệu AWS hoặc tham khảo các cộng đồng công nghệ để hiểu rõ cơ chế và tìm ra giải pháp.
- **Tập trung vào phần cốt lõi trước:** Đừng cố xây dựng một hệ thống quá đồ sộ ngay từ đầu. Hãy deploy thành công một pipeline API-to-Lambda-to-RDS cơ bản trước, sau đó mới bổ sung WAF, CloudFront hay Cognito.

**Tuần 10–12 (Giai đoạn báo cáo):**
- **Đầu tư cho Portfolio:** Trang báo cáo thực tập này chính là hồ sơ năng lực (portfolio) trực quan nhất của bạn. Hãy trình bày nó thật rõ ràng và chuyên nghiệp để chứng minh sự trưởng thành của bạn sau khóa học.

### Công cụ đắc lực nhất cho một Newbie Cloud Engineer
| Công cụ | Lý do |
|---------|-------|
| **AWS SAM CLI** | Công cụ tuyệt vời để tiếp cận Infrastructure as Code (IaC) ở mức độ cơ bản, giúp deploy lặp lại dễ dàng. |
| **CloudWatch Logs** | Công cụ bắt buộc phải làm quen để biết hệ thống đám mây đang chạy ra sao và tìm lỗi ở đâu. |


