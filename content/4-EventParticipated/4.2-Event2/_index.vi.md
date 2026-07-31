---
title: "Event 2: Seminar AI From Scratch"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo cáo Thu hoạch “Seminar AI From Scratch”

### Mục Đích Của Sự Kiện

Seminar "AI From Scratch" được tổ chức dành cho sinh viên và cộng đồng phát triển phần mềm nhằm mang đến góc nhìn toàn diện về quy trình ứng dụng Trí tuệ nhân tạo (AI), Học máy (Machine Learning) và Generative AI trên nền tảng AWS. Sự kiện giúp người tham dự nắm vững từ các dịch vụ AI Managed Services dựng sẵn, luồng kiến trúc xây dựng AI Agent đa ngôn ngữ, quy trình MLOps với Amazon SageMaker cho đến trải nghiệm ứng dụng Amazon Bedrock tạo Chatbot thông minh và tham gia trò chơi tương tác điều khiển bằng giọng nói.

### Danh Sách Diễn Giả

- **Nguyễn Tuấn Thịnh** - DevOps/Cloud Engineer, AWS Vietnam
- **Nguyễn Công Minh** - DevOps Engineer, AWS Vietnam
- **Thầy Mai Hoàng Đỉnh** - Giảng viên IA, Trường Đại học FPT TP.HCM (Giảng viên phụ trách chuyên môn)
- **Đội ngũ Chuyên viên Kỹ thuật** - Đại diện AWS Vietnam

### Nội Dung Nổi Bật

#### 1. Hệ sinh thái AWS AI Managed Services & Quy trình xây dựng AI Agent
- **Giới thiệu các dịch vụ AI chuyên dụng**: Khám phá bộ công cụ AI xử lý đa phương tiện qua API gồm:
  - *Amazon Transcribe*: Chuyển đổi giọng nói thành văn bản (Speech-to-Text).
  - *Amazon Translate*: Dịch thuật đa ngôn ngữ tự động.
  - *Amazon Comprehend*: Phân tích cảm xúc, trích xuất chủ đề và từ khóa.
  - *Amazon Lex*: Xử lý ngôn ngữ tự nhiên và nhận diện ý định hội thoại (Chatbot/Voicebot).
  - *Amazon Polly*: Chuyển đổi văn bản thành giọng đọc tự nhiên (Text-to-Speech).
  - *Amazon Textract*: Trích xuất dữ liệu và bóc tách tài liệu thông minh (OCR).
  - *Amazon Rekognition*: Nhận diện hình ảnh, phân tích khuôn mặt và phát hiện lỗi sản phẩm.
- **Kiến trúc luồng 6 bước xây dựng AI Agent hỗ trợ khách hàng đa ngôn ngữ**:
  1. *Transcribe*: Tiếp nhận cuộc gọi và chuyển giọng nói sang văn bản.
  2. *Translate*: Dịch ngôn ngữ sang dạng chuẩn hóa.
  3. *Comprehend*: Phân tích sắc thái cảm xúc và chủ đề cuộc gọi.
  4. *Lex*: Nhận diện ý định và các thông tin (Intent & Slots).
  5. *Backend Integration*: Gọi API nghiệp vụ và truy vấn CSDL.
  6. *Polly*: Phản hồi khách hàng bằng giọng nói tự nhiên.

#### 2. Xây dựng và Huấn luyện mô hình ML với Amazon SageMaker
- Hướng dẫn toàn diện quy trình MLOps end-to-end: Chuẩn bị và làm sạch dữ liệu, chọn lựa thuật toán huấn luyện mô hình tùy chỉnh, tự động tinh chỉnh tham số (Hyperparameter Tuning) và triển khai các điểm cuối phục vụ dự đoán thời gian thực (Real-time Inference Endpoints) trên Amazon SageMaker.

#### 3. Khai phá Generative AI & Triển khai Chatbot với Amazon Bedrock
- Giới thiệu dịch vụ Amazon Bedrock cho phép truy cập an toàn vào các mô hình nền tảng lớn (Foundation Models) như Anthropic Claude, Meta Llama. Hướng dẫn kỹ thuật Prompt Engineering, tích hợp RAG (Retrieval-Augmented Generation) để tạo ra các Chatbot thông minh xử lý tri thức nội bộ cho doanh nghiệp.

#### 4. Trải nghiệm Game Demo tương tác bằng Giọng nói (Voice-Controlled Game)
- Trực tiếp trải nghiệm trò chơi demo sáng tạo do các diễn giả AWS xây dựng. Game sử dụng tích hợp kết hợp giữa Amazon Transcribe và Amazon Lex, cho phép người chơi phát lệnh bằng giọng nói trực tiếp qua micro để điều khiển nhân vật di chuyển và thực hiện hành động theo thời gian thực.

### Những Gì Học Được

#### Tư Duy Thiết Kế
- **Tư duy phát triển ứng dụng AI-First**: Nắm vững phương pháp kết hợp các dịch vụ AI sẵn có qua API để rút ngắn thời gian phát triển sản phẩm từ hàng tháng xuống còn vài ngày.
- **Tư duy thiết kế Agent đa kênh**: Thấu hiểu cách phối hợp linh hoạt giữa xử lý giọng nói, dịch thuật, phân tích cảm xúc và truy vấn CSDL backend.

#### Kiến Trúc Kỹ Thuật
- **Chuẩn hóa kiến trúc AI Agent**: Nắm rõ 6 bước xử lý luồng thoại/văn bản và các thành phần bổ trợ như OCR (Textract) và Computer Vision (Rekognition).
- **Lập trình Generative AI & MLOps**: Thấu hiểu cơ chế hoạt động của Amazon Bedrock và quy trình triển khai mô hình học máy trên Amazon SageMaker.

#### Chiến Lược Hiện Đại Hóa
- Tận dụng điện toán đám mây để đơn giản hóa việc đưa các mô hình AI/ML phức tạp vào ứng dụng thực tế mà không cần đầu tư hạ tầng GPU đắt đỏ ban đầu.

### Ứng Dụng Vào Công Việc

- **Tích hợp AI Services vào dự án**: Áp dụng các dịch vụ Amazon Transcribe, Polly và Lex để xây dựng tính năng tương tác giọng nói / Chatbot tự động cho ứng dụng.
- **Nâng cấp giải pháp Web/Mobile**: Sử dụng Amazon Textract và Rekognition để tự động hóa quy trình bóc tách chứng từ và xác thực dữ liệu hình ảnh.
- **Nghiên cứu Generative AI**: Thử nghiệm tích hợp Amazon Bedrock với CSDL để xây dựng trợ lý ảo tra cứu thông tin cho các đồ án tiếp theo.

### Trải nghiệm trong event

Buổi Seminar "AI From Scratch" tại Thư viện FPTU đã mang lại một không gian học tập vô cùng sôi nổi và bổ ích. Trải nghiệm ấn tượng nhất là phần chơi game điều khiển bằng giọng nói cuối buổi cùng sự hướng dẫn tận tình, gần gũi từ hai anh Nguyễn Tuấn Thịnh, Nguyễn Công Minh và Thầy Mai Hoàng Đỉnh, giúp các khái niệm AI/ML trở nên trực quan và dễ tiếp thu hơn bao giờ hết.

#### Một số hình ảnh khi tham gia sự kiện

![Hình ảnh Seminar AI From Scratch 1](/images/4-Events/Event2/event2_1.jpeg)
![Hình ảnh Seminar AI From Scratch 2](/images/4-Events/Event2/event2_2.jpeg)
![Hình ảnh Seminar AI From Scratch 3](/images/4-Events/Event2/event2_3.jpeg)

> Sự kiện đã mở ra những góc nhìn công nghệ mới mẻ, giúp em tự tin hơn trong việc khám phá và ứng dụng các dịch vụ AI hàng đầu của AWS vào dự án học tập và định hướng nghề nghiệp tương lai.
