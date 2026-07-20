---
title: "Đề xuất dự án"
date: 2026-07-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---
Phần này trình bày đề xuất dự án cho **LingoRise** — sản phẩm chính được xây dựng trong chương trình thực tập FCAJ Cloud.

# LingoRise — Nền tảng luyện thi IELTS & TOEIC hỗ trợ AI

{{% notice info %}}
* **Trang web đã triển khai:** [lingorise.xyz](https://www.lingorise.xyz/)
* **Video Demo dự án:** [Thư mục Google Drive Demo](https://drive.google.com/drive/u/0/folders/1p3dhFRWf3rbgyNnlVk-R2KkELfWrA1Ce)
{{% /notice %}}

### 1. Bối cảnh & Động lực

Lúc mới vào thực tập ở First Cloud Journey, em có thử dùng mấy trang luyện thi IELTS/TOEIC phổ biến thì thấy đa số đều bằng tiếng Anh hết, mà phí thì cũng không rẻ. Với lại mấy trang đó cũng không có chức năng nào giúp mình biết mình yếu chỗ nào để tập trung ôn. Nhiều bạn sinh viên mới bắt đầu còn chưa quen giao diện tiếng Anh thì đã nản rồi, chưa kịp học gì.

Từ đó em nảy ra ý tưởng làm **LingoRise** — một trang web luyện thi IELTS và TOEIC giao diện tiếng Việt, có tích hợp AI để phân tích bài làm và gợi ý cho từng người. Toàn bộ hệ thống chạy trên AWS serverless nên chi phí vận hành thấp, phù hợp cho một dự án sinh viên tự làm.

### 2. Phân tích vấn đề

#### Đối tượng người dùng mục tiêu
- Sinh viên đại học Việt Nam chuẩn bị thi chứng chỉ IELTS Academic/General hoặc TOEIC.
- Người tự học không có điều kiện tham gia các khóa luyện thi đắt đỏ hoặc học kèm một-một.
- Giáo viên và người tạo nội dung cần công cụ tập trung để quản lý và phân phối tài liệu đề thi.

#### LingoRise giải quyết những vấn đề cụ thể nào?

| Vấn đề | Cách LingoRise giải quyết |
|--------|--------------------------|
| Nền tảng chỉ có tiếng Anh tạo rào cản cho người mới | Giao diện ưu tiên tiếng Việt với nội dung song ngữ xuyên suốt |
| Nội dung thi chất lượng đắt đỏ và phân tán | Ngân hàng đề thi tập trung với AI hỗ trợ tạo câu hỏi từ nguồn markdown thô |
| Không có phản hồi cá nhân hóa về kết quả luyện tập | AI phân tích bài Writing (task achievement, coherence, grammar, lexical resource), biểu đồ radar điểm số, xem lại đáp án từng câu kèm giải thích AI |
| Tạo nội dung thủ công chậm và dễ lỗi | Pipeline nội dung admin với phân tích tự động, phát hiện trùng lặp, và nhật ký kiểm toán |
| Tích hợp thanh toán cho thị trường Việt Nam còn hạn chế | Tích hợp webhook chuyển khoản ngân hàng Sepay để xác minh thanh toán tự động |

### 3. Kiến trúc kỹ thuật

LingoRise sử dụng kiến trúc tách biệt (decoupled), frontend và backend giao tiếp qua REST API, với các dịch vụ AWS xử lý xác thực, lưu trữ file, và phân phối nội dung.

![Sơ đồ kiến trúc kỹ thuật LingoRise](/images/so_do_kien_truc.png)

#### Công nghệ sử dụng
| Tầng | Công nghệ | Lý do chọn |
|------|-----------|-----------|
| **Frontend** | Next.js 15, React 19, TailwindCSS | Server-side rendering cho SEO, kiến trúc component hiện đại |
| **Backend** | Express.js trên AWS Lambda (qua SAM) | Triển khai serverless giảm chi phí quản lý server |
| **Database** | Supabase PostgreSQL (External) | Đảm bảo tính toàn vẹn quan hệ cho chấm điểm, tiến trình học, và giao dịch thanh toán |
| **Xác thực** | AWS Cognito (JWT) | User pool quản lý với MFA, token refresh, và phân quyền role |
| **Lưu trữ** | Amazon S3 + CloudFront (OAC) | Bucket private với CDN phân phối qua Origin Access Control |
| **Dịch vụ AI** | OpenRouter API | Định tuyến model linh hoạt cho tạo đề thi và phản hồi bài viết |
| **Thanh toán** | PayOS webhook (tự động hóa thanh toán) | Xác minh giao dịch thanh toán qua mã QR động của cổng PayOS |
| **Triển khai** | AWS SAM + AWS Amplify | Infrastructure-as-code cho backend; managed hosting cho frontend |

#### Tích hợp dịch vụ AWS
- **AWS Lambda** — Chạy backend Express như một serverless function duy nhất, xử lý toàn bộ API routes.
- **Amazon API Gateway** — Proxy định tuyến HTTP với cấu hình CORS cho frontend trên Amplify.
- **Amazon S3** — Lưu trữ hình ảnh đề thi, file audio phát âm, và tài liệu upload. Bucket private không cho phép truy cập công khai.
- **Amazon CloudFront** — CDN với Origin Access Control phân phối tài nguyên S3 an toàn mà không lộ bucket.
- **Amazon Cognito** — User pool quản lý tài khoản học viên và admin với xác thực dựa trên JWT.
- **AWS Polly** — Tạo audio phát âm cho tính năng sổ từ vựng.

### 4. Tính năng chính

#### Dành cho học viên
| Tính năng | Mô tả |
|-----------|-------|
| **Exam Engine IELTS/TOEIC** | Mô phỏng bài thi đầy đủ với đồng hồ đếm ngược, thanh điều hướng câu hỏi, lưu trạng thái phiên thi (tiếp tục giữa chừng), và Cambridge band scoring |
| **Trực quan hóa điểm số** | Biểu đồ radar (Chart.js) hiển thị phân bố band score theo Listening, Reading, Writing, Speaking |
| **Xem lại đáp án** | Xem lại từng câu với chỉ thị màu đúng/sai, đáp án đúng, và giải thích do AI tạo ra |
| **AI chấm bài Writing** | Phân tích bài luận theo 4 tiêu chí IELTS: task achievement, coherence & cohesion, lexical resource, grammatical range |
| **Câu hỏi điền khuyết** | Dựng ô nhập văn bản động qua regex parser cho câu hỏi fill-in-the-blank, chấm điểm không phân biệt hoa thường |
| **Sổ từ vựng** | Ngân hàng từ cá nhân với audio phát âm AWS Polly và theo dõi lặp lại ngắt quãng |

#### Dành cho admin
| Tính năng | Mô tả |
|-----------|-------|
| **Tạo đề thi bằng AI** | Dán nội dung đề thi markdown thô; AI phân tích và cấu trúc thành định dạng câu hỏi trong database |
| **Dashboard chờ duyệt** | Đề thi vừa tạo xong xuất hiện ngay trên trang chủ dashboard với nút Duyệt/Từ chối một chạm |
| **Hàng đợi kiểm duyệt** | Hàng đợi xét duyệt với cờ chất lượng và nhật ký kiểm toán theo dõi mọi hành động admin |
| **Pipeline tải ảnh tự động** | Công cụ cào tự động tải ảnh ngoại vi từ nội dung đề thi sao chép và upload lên S3 |
| **Giám sát thanh toán PayOS** | Webhook receiver xác minh giao dịch qua mã QR động, hiển thị trạng thái giao dịch trong bảng admin |

### 5. Tiến trình phát triển

Quá trình phát triển theo hướng tiếp cận tuần tự, xây dựng từ nền tảng hạ tầng AWS đến phát triển tính năng, sau đó triển khai và tối ưu:

| Giai đoạn | Tuần | Hoạt động chính |
|-----------|------|-----------------|
| **Nền tảng AWS** | 1–2 (20/04–01/05) | Bảo mật tài khoản (IAM, MFA), chính sách mã hóa S3, cấu hình liên kết mạng và bảo mật VPC Security Groups |
| **Lập trình cặp với AI** | 3 (04/05–08/05) | Tham vấn AI thiết kế kiến trúc serverless, viết Lambda handlers, prompt engineering cho phân tích đề thi |
| **Cổng Admin** | 4 (11/05–15/05) | Giao diện dashboard admin, middleware RBAC, hàng đợi xét duyệt, nhật ký kiểm toán database |
| **Thanh toán & AI đề thi** | 5 (18/05–22/05) | Tích hợp webhook PayOS, AI tạo ngân hàng câu hỏi từ markdown, regex parser trích xuất JSON |
| **Sửa lỗi đề thi** | 6 (25/05–29/05) | Thiếu ảnh Reading (S3 scraper pipeline), dựng ô nhập điền khuyết, chấm điểm case-insensitive, logic tạo đề |
| **Tốc độ AI & Kiểm duyệt** | 7 (01/06–05/06) | Hàng đợi job bất đồng bộ cho AI, widget chờ duyệt trên dashboard, nút kiểm duyệt một chạm |
| **Hoàn thiện Frontend** | 8 (08/06–12/06) | Biểu đồ điểm số, màn hình xem lại đáp án, sửa lỗi token refresh Cognito, responsive mobile, AI chấm Writing |
| **Triển khai Production** | 9 (15/06–19/06) | SAM deploy lên AWS, Amplify hosting, Supabase migration, CloudFront CDN, sửa CORS, smoke testing |
| **Tối ưu & Bảo mật** | 10 (22/06–26/06) | Sửa lỗi chấm điểm, input validation, rate limiting, tối ưu cold start Lambda, nén ảnh, database indexing |
| **Beta & Tài liệu** | 11–12 (29/06–10/07) | Thu thập phản hồi người dùng, cải tiến UX, website báo cáo thực tập, nộp bài cuối |

### 6. Ước tính chi phí

Tất cả dịch vụ hoạt động trong hoặc gần với AWS Free Tier, giúp dự án bền vững cho sinh viên:

| Dịch vụ | Chi phí hàng tháng | Ghi chú |
|---------|--------------------|---------| 
| AWS Lambda | ~$0.00 | Free tier hỗ trợ 1 triệu request/tháng |
| Amazon S3 | ~$0.23 | Hình ảnh đề thi và file audio |
| Amazon CloudFront | ~$0.10 | Phân phối CDN với OAC |
| Amazon Cognito | ~$0.00 | Free tier cho <50,000 người dùng |
| Supabase PostgreSQL | ~$0.00 | Free tier hỗ trợ đầy đủ tính năng |
| AWS Polly | ~$4.00 | Trả theo ký tự cho audio từ vựng |
| OpenRouter AI API | ~$5.00 | Tạo đề thi và phản hồi bài viết |
| **Tổng** | **~$9.33/tháng** | |

### 7. Đánh giá rủi ro & Phương án giảm thiểu

| Rủi ro | Mức tác động | Phương án đã áp dụng |
|--------|-------------|---------------------|
| Tốc độ tạo đề AI không ổn định gây timeout | Cao | Chuyển sang hàng đợi job bất đồng bộ (BullMQ); phản hồi tức thì kèm job tracking ID |
| Thiếu hình ảnh trong nội dung đề thi sao chép | Trung bình | Xây dựng công cụ cào Node.js tự động tải và lưu trữ lại tài nguyên trên S3 |
| Token Cognito hết hạn giữa bài thi | Cao | Triển khai Axios interceptor tự động làm mới token |
| CORS chặn request trên production | Trung bình | Cấu hình origin whitelist rõ ràng trên API Gateway cho domain Amplify |
| Độ trễ cold start Lambda | Trung bình | Áp dụng tree-shaking dependency và provisioned concurrency trên handler quan trọng |

### 8. Kết quả mong đợi

#### Sản phẩm kỹ thuật
- Nền tảng luyện thi IELTS/TOEIC triển khai hoàn chỉnh trên hạ tầng serverless AWS.
- Pipeline tạo đề thi bằng AI chuyển đổi markdown thô thành ngân hàng câu hỏi có cấu trúc.
- Dashboard admin với kiểm duyệt nội dung thời gian thực và quy trình phê duyệt một chạm.
- Giao diện học viên responsive mobile-first với trực quan hóa điểm số và phản hồi bài viết AI.
- Pipeline quản lý tài nguyên tự động (cào ảnh, upload S3, phân phối CloudFront).

#### Kết quả học tập
- Kinh nghiệm thực tế triển khai và vận hành các dịch vụ AWS trong môi trường production thực tế.
- Thành thạo phát triển full-stack với Next.js 15, Express, TypeScript, và Supabase PostgreSQL.
- Kỹ năng giải quyết vấn đề thực tế: quản lý token, CORS, pipeline tài nguyên ảnh, và edge case chấm điểm.
- Kinh nghiệm tích hợp AI: prompt engineering, trích xuất JSON, xử lý job bất đồng bộ, và phân tích bài viết.