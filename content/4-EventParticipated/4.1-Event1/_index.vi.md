---
title: "Sự kiện 1: AWS First Cloud AI Journey — Community Day"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# AWS First Cloud AI Journey — Community Day

### Thông tin sự kiện
| | |
|---|---|
| **Event Name** | AWS First Cloud AI Journey — Community Day |
| **Date** | 23/05/2026 |
| **Location** | 26th Floor, Bitexco Financial Tower, 2 Hai Trieu Street, Ben Nghe Ward, District 1, Ho Chi Minh City |
| **Organizer** | AWS Study Group |
| **Role** | Participant / Intern |

![AWS First Cloud AI Journey — Community Day](/images/event_1.jpg)

### Mô tả sự kiện
**AWS First Cloud AI Journey — Community Day** là một hội thảo công nghệ quy mô được tổ chức trực tiếp tại tòa nhà Bitexco Financial Tower. Sự kiện quy tụ các chuyên gia hàng đầu, Cloud Architects, GenAI Engineers và DevOps Engineers đến chia sẻ về kinh nghiệm thực tế, mô hình kiến trúc và các chiến lược triển khai giải pháp GenAI, DevOps và Platform Engineering trên hạ tầng điện toán đám mây AWS.

### Điểm nổi bật trong sự kiện
- **Ứng dụng GenAI trong doanh nghiệp**: Các diễn giả đến từ VIB và VPBank chia sẻ về cách áp dụng mô hình Generative AI trong hệ thống ngân hàng nhằm tối ưu hóa phân tích nghiệp vụ và tự động hóa hỗ trợ khách hàng.
- **DevOps & Platform Engineering**: Các kỹ sư từ FCAJ và GoTymeX chia sẻ kinh nghiệm xây dựng các tầng kỹ thuật nền tảng (platform engineering) và tối ưu hóa luồng triển khai CI/CD serverless trên AWS.
- **Tư vấn Cloud & Thiết kế kiến trúc**: Các chuyên gia từ G-AsiaPacific và Cloud Kinetics trình bày về các mẫu thiết kế kiến trúc hệ thống lớn chịu tải cao, tính sẵn sàng và các thực hành tối ưu hóa chi phí đám mây.

### Chuyên đề nổi bật: "Context Is Everything — Making AI Actually Work for You"
Trình bày bởi diễn giả **Tinh Truong** (Platform Engineer, GoTymeX), chuyên đề tập trung vào tầm quan trọng cốt lõi của "ngữ cảnh" (context) khi làm việc với mô hình ngôn ngữ lớn (LLM).

#### Các nội dung cốt lõi:
1. **Tại sao AI thất bại nếu thiếu ngữ cảnh**: Dù mô hình AI rất mạnh mẽ, kết quả đầu ra vẫn sẽ mơ hồ và không thực tế nếu dữ liệu đầu vào (input) quá sơ sài và thiếu thông tin thực tế.
2. **Thế nào là "Ngữ cảnh" (Context)?**: Là toàn bộ thông tin giúp AI hiểu rõ "nhiệm vụ ẩn sau nhiệm vụ". Ngữ cảnh chất lượng bao gồm:
   - **Mục tiêu (Your Goal)**: Kết quả cuối cùng mong muốn là gì.
   - **Tình huống (Your Situation)**: Vai trò người hỏi (mới bắt đầu, sinh viên, dự án nhóm, thời hạn...).
   - **Ràng buộc (Your Constraints)**: Ngôn ngữ lập trình, tech stack, văn phong, ngân sách, định dạng.
   - **Bằng chứng liên quan (Relevant Evidence)**: Các đoạn mã nguồn, tài liệu API, ví dụ mẫu, yêu cầu nghiệp vụ.
   - *Thông điệp*: "Ngữ cảnh biến một yêu cầu mơ hồ thành một bài toán có thể giải quyết được."
3. **Sai lầm phổ biến: Vấn đề "Internet Puller"**:
   - *Thói quen xấu*: Sao chép vô tội vạ toàn bộ bài báo, tệp PDF lớn, ảnh chụp màn hình và ghi chú thô vào một ô chat duy nhất.
   - *Tác hại*: Ngữ cảnh không liên quan gây nhiễu AI, làm giảm độ chính xác vì thông tin quan trọng bị chôn vùi trong mớ hỗn độn, đồng thời làm tăng chi phí token.
   - *Thông điệp*: "Không phải cứ nhiều ngữ cảnh hơn là tốt hơn."
4. **Mô hình "Bộ não AI thứ hai" (Second AI Brain)**:
   - Chia sẻ về cách xây dựng hệ thống ghi nhớ tiến trình học tập, hiểu rõ mục tiêu dự án, tự động truy xuất đúng ngữ cảnh trước khi trả lời và hoàn thiện dần khi kho kiến thức lớn lên.
   - *Thông điệp*: "Bộ não AI thứ hai không phải phép thuật. Đó chỉ là sự kết hợp chuẩn xác giữa Ngữ cảnh + Trí nhớ."


### Chuyên đề nổi bật: "GenAI-Powered Auto Audit for AWS Workload"
Trình bày bởi diễn giả **Pham Nguyen Hai Anh** (Cloud Consultant tại G-AsiaPacific Vietnam, AWS Community Builder - Security), chuyên đề giới thiệu giải pháp tự động hóa kiểm định hệ thống thông qua các trợ lý GenAI, giải quyết các khó khăn thường nhật của doanh nghiệp.

#### Các nội dung cốt lõi:
1. **Khó khăn của người dùng nghiệp vụ**: Chỉ ra nỗi đau của các phòng ban khi phải tìm kiếm dữ liệu thủ công từ nhiều nguồn rời rạc, phụ thuộc vào chuyên gia khi cần phân tích tập dữ liệu chuyên sâu và lặp lại các công việc nhàm chán tốn thời gian.
2. **Kiến trúc Amazon Q Business (Quick Suite)**: Phân tích mô hình hoạt động đa tác vụ:
   - **Insights**: Giao tiếp bằng ngôn ngữ tự nhiên để tra cứu và hỏi đáp.
   - **BI & Automation**: Tạo dashboard tự động, giả lập các kịch bản và kích hoạt luồng tự động hóa quy trình (HR, Sales, Support).
   - **Tích hợp nguồn dữ liệu**: Kết nối hơn 40 cổng dữ liệu doanh nghiệp (Google Workspace, S3, databases) dựa trên nền tảng Bedrock và thực hiện hành động trên ứng dụng bên thứ ba.
   - **Bảo mật & Kiểm soát**: Tích hợp phân quyền chặt chẽ và lọc tuân thủ quy chuẩn.
3. **Use Case - PM Assistant**: Trực quan hóa cách trợ lý ảo tự động ghi biên bản cuộc họp (MoM) từ file ghi âm, gửi email cập nhật cho các bên liên quan và tự động lên lịch họp tiếp theo.
4. **Kiểm toán an toàn thông tin tự động**: Minh họa cách sử dụng LLM để tự động quét kiến trúc AWS, đối chiếu tiêu chuẩn bảo mật và phát hiện lỗ hổng hệ thống.


### Chuyên đề nổi bật: "From Edge to Origin: CloudFront as Your Foundation"
Trình bày bởi diễn giả **Nguyen Tuan Thinh** (DevOps Engineer, First Cloud AI Journey), chuyên đề khai thác vai trò của Amazon CloudFront như một lớp phân phối nền tảng, đồng thời phân tích các rủi ro tài chính liên quan đến chi phí CDN trên đám mây.

#### Các nội dung cốt lõi:
1. **Nền tảng phân phối Edge-to-Origin**: Tận dụng CloudFront làm chốt chặn đầu tiên giúp cache và phân phối tài nguyên tĩnh/động từ các Edge Location toàn cầu, giảm tối đa độ trễ cho người dùng.
2. **Nghịch lý chi phí Pay-As-You-Go**: Dù AWS cung cấp gói Free Tier CloudFront 1TB cực kỳ hào phóng (phù hợp cho các dự án nhỏ với chi phí bắt đầu từ $0), mô hình tính phí theo lưu lượng thực tế (pay-as-you-go) vẫn tiềm ẩn nhiều rủi ro:
   - **Khó ước lượng chi phí**: Lưu lượng truy cập biến động liên tục khiến việc dự báo ngân sách hàng tháng rất phức tạp.
   - **Đột biến lưu lượng**: Khi ứng dụng có lượng người dùng tăng đột biến (viral) hoặc bị tấn công DDoS, hóa đơn CDN có thể tăng vọt ngoài tầm kiểm soát.
   - **Rủi ro tài chính**: Các trường hợp hóa đơn đám mây tăng bất ngờ lên hàng chục, hàng trăm nghìn USD gây nguy cơ tổn thất tài chính nghiêm trọng cho các nhà sáng lập.
3. **Giải quyết lo ngại của khách hàng**: Đưa ra lời giải cho các băn khoăn về cách dự báo chi phí CDN hàng tháng, bảo vệ máy chủ gốc (origin) khỏi lưu lượng độc hại và đơn giản hóa bảng kê hóa đơn.
4. **Các thực hành tốt nhất (Best Practices)**: Thiết lập CloudWatch Billing Alerts để cảnh báo chi phí sớm, tích hợp AWS WAF ngăn chặn lưu lượng tấn công ảo, và tối ưu hóa chính sách TTL để đạt tỷ lệ hit-ratio cache cao nhất.


### Chuyên đề nổi bật: "36 hrs with LotusHacks: Building UTMorpho from Idea to Reality"
Trình bày bởi **Team VIB** (đại diện nhóm kỹ sư GenAI và phát triển phần mềm của VIB), chuyên đề chia sẻ về trải nghiệm thực tế đầy áp lực khi tham gia cuộc thi hackathon LotusHacks kéo dài 36 giờ để xây dựng và ra mắt sản phẩm **UTMorpho**.

#### Các nội dung cốt lõi:
1. **Hành trình từ con số 0 đến ý tưởng (Brainstorming)**: Quá trình từ "Giờ thứ 0" khi đầu óc trống rỗng, đến việc quan sát các vấn đề bất tiện trong công việc hàng ngày trong ngày khai mạc, giúp định hình rõ bài toán cần giải quyết và khai sinh ra UTMorpho.
2. **Quy trình chạy nước rút 36 giờ (36-Hour Hackathon Sprint)**: Phương pháp làm việc khoa học để chuyển giao sản phẩm cực nhanh dưới áp lực thời gian lớn:
   - **Setup & Alignment**: Đồng thuận trong nhóm về phạm vi sản phẩm khả thi tối thiểu (MVP).
   - **First Slice**: Định hình kiến trúc cốt lõi, schema dữ liệu và ranh giới API.
   - **Build the core**: Phát triển song song với tốc độ cao các tính năng cốt lõi.
   - **The hard middle**: Giải quyết các lỗi phát sinh bất ngờ và xung đột tích hợp ở giai đoạn giữa.
   - **Integration & Polish**: Ghép nối frontend và backend, trau chuốt giao diện người dùng.
   - **Submit & Pitch**: Hoàn thiện kịch bản demo và thuyết trình giá trị sản phẩm trước ban giám khảo.
3. **Các bài học rút ra**: Tầm quan trọng của việc xây dựng prototype nhanh, quản lý nợ kỹ thuật (technical debt) một cách linh hoạt, duy trì sự gắn kết của nhóm và tập trung giải quyết triệt để một vấn đề thay vì tham lam quá nhiều tính năng.


### Chuyên đề nổi bật: "Non-Determinism of 'Deterministic' LLM Settings"
Trình bày bởi diễn giả **Duc Dao** (Solution Architect - Cloud Kinetics), chuyên đề đi sâu nghiên cứu cơ chế chọn lựa token của LLM, các thiết lập lấy mẫu (sampling), và lý do thực tế tại sao cài đặt Temperature = 0 vẫn không đảm bảo tính nhất quán (deterministic) hoàn toàn ở đầu ra.

#### Các nội dung cốt lõi:
1. **Cơ chế sinh token**: LLM tạo văn bản theo từng token nối tiếp. Ở mỗi bước, mô hình tính điểm số (logits) cho toàn bộ từ vựng, chuyển đổi thành phân phối xác suất qua hàm softmax, và chọn token tiếp theo từ phân phối này.
2. **Vai trò của tham số Temperature**: Quy định mức độ phân tán của xác suất. Trong khi nhiệt độ cao tăng tính ngẫu nhiên/sáng tạo, thì thiết lập Temperature = 0 *trên lý thuyết* sẽ kích hoạt argmax selection (luôn chọn token có xác suất cao nhất) để cho ra kết quả cố định giống nhau.
3. **Nghịch lý tính phi nhất quán (Non-determinism)**: Thực tế chạy Temperature = 0 trên hạ tầng GPU vẫn cho ra các kết quả khác biệt do:
   - **Cơ chế xử lý song song của GPU**: Phép cộng dấu phẩy động không có tính kết hợp `(a + b) + c != a + (b + c)`. Khi chạy song song hàng nghìn lõi GPU, thứ tự cộng dồn thay đổi dẫn tới sai số làm lệch phân phối xác suất token.
   - **Tác động từ lớp API**: Tải hệ thống, cân bằng tải server và sự khác biệt phần cứng tại nhà cung cấp cloud làm sai lệch nhẹ kết quả.
4. **Giải pháp khắc phục**: Thiết lập JSON schema validation nghiêm ngặt, tăng cường ràng buộc trong system prompt, sử dụng tham số seed và xây dựng các bộ parser xử lý ngoại lệ ở backend.


### Chuyên đề nổi bật: "Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring"
Trình bày bởi diễn giả **Vy Lam** (Senior Business Systems Analyst, VPBank), chuyên đề phân tích rào cản hệ thống khi đánh giá tín dụng doanh nghiệp khởi nghiệp và mô hình AI Multi-Agent khắc phục các nhược điểm của Single-Agent.

#### Các nội dung cốt lõi:
1. **Sự lệch pha về cấu trúc dữ liệu**: Các ngân hàng truyền thống yêu cầu báo cáo tài chính 3+ năm, tài sản thế chấp và doanh thu ổn định. Startup thực tế chỉ hoạt động 6-18 tháng, tài sản chủ yếu là sở hữu trí tuệ (IP) và chỉ số tăng trưởng, dẫn đến việc bị loại khỏi mô hình duyệt tín dụng cứng nhắc dù có tiềm năng.
2. **Hạn chế của mô hình Single-Agent**: Một AI agent duy nhất duyệt tín dụng sẽ gặp các giới hạn: giới hạn cửa sổ ngữ cảnh (context limits), loãng chuyên môn (dilution), thiếu cơ chế kiểm soát chéo (checks & balances) và là điểm lỗi đơn nhất (single point of failure).
3. **Mô hình Multi-Agent**: Đề xuất mô hình "Hội đồng tín dụng ảo", tách biệt việc đánh giá thành các nhóm AI agent chuyên môn hóa sâu (phân tích tài chính, thẩm định công nghệ/IP, kiểm toán rủi ro) phối hợp dưới một layer điều phối trung tâm.
4. **Kiểm soát & Bảo mật cấp doanh nghiệp**: Bảo vệ khối lượng công việc LLM qua 5 lớp kiến trúc:
   - *Perimeter*: WAF, chống DDoS và rate limiting.
   - *Mạng VPC*: Subnet riêng tư, cổng kết nối bảo mật (PrivateLink) và Security Groups.
   - *Identity*: IAM, Cognito, phân quyền vai trò (RBAC) và xác thực đa yếu tố (MFA).
   - *Ứng dụng*: Input validation, phòng chống prompt injection và lọc đầu ra model.
   - *Dữ liệu*: Mã hóa dữ liệu lưu trữ/đang truyền và ghi nhật ký kiểm toán không thể sửa xóa.

### Bài học và Trải nghiệm thực tế
- **Ngữ cảnh là then chốt**: Rút ra bài học sâu sắc về việc cung cấp dữ liệu ngữ cảnh sạch và chọn lọc cho mô hình AI khi lập trình cặp, giúp code sinh ra chất lượng và ít lỗi hơn.
- **Hệ thống Multi-Agent và phân rã nghiệp vụ**: Thấy rõ tầm quan trọng của việc chia nhỏ các tác vụ AI phức tạp thay vì gộp chung một mô hình lớn. Điều này củng cố cách em phân chia logic AI của LingoRise: một luồng tạo đề thi riêng và một luồng đánh giá chấm điểm bài luận Writing riêng.
- **Tập trung vào giá trị kinh doanh ngắn hạn**: Hiểu rằng bài toán định giá và mô hình tài chính phải được kiểm chứng trước khi tối ưu hóa hạ tầng bên dưới.
- **Đóng gói phòng thủ trước biến động LLM**: Bài thuyết trình của anh Đức giúp em hiểu sâu sắc nguyên nhân vì sao AI tạo đề thi thỉnh thoảng trả về định dạng JSON bị lệch hoặc lỗi cú pháp. Điều này khẳng định sự cần thiết của bộ parser xử lý fallback bằng biểu thức chính quy `extractJsonObject()` mà em đã xây dựng ở Tuần 5 để chủ động xử lý các biến động này.
- **Bảo mật & Dự toán ngân sách CDN**: Hiểu được tầm quan trọng cực kỳ của việc thiết lập các ngưỡng cảnh báo chi phí chặt chẽ và cấu hình CloudFront Origin Access Control (OAC) để bảo vệ tài nguyên S3 của LingoRise.
- **Giao lưu kết nối**: Có cơ hội trao đổi trực tiếp với các chuyên gia đám mây và mentor kỳ cựu, tiếp thu ý kiến đóng góp cho thiết kế cơ sở dữ liệu và phương án thanh toán của dự án LingoRise.
