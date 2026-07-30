---
title: "Bản đề xuất"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Smart Parking System
## Giải pháp Hệ thống Bãi đỗ xe Thông minh Tích hợp AI & AWS Cloud

### 1. Tóm tắt điều hành
Hệ thống **Smart Parking System** được thiết kế nhằm giải quyết bài toán quản lý bãi đỗ xe hiện đại, tối ưu hóa quá trình tìm kiếm vị trí đỗ và tự động hóa nhận diện phương tiện ra/vào. Nền tảng kết hợp công nghệ Trí tuệ nhân tạo (AI/Computer Vision) với hạ tầng điện toán đám mây AWS mạnh mẽ, có khả năng tự động nhận diện biển số xe, giám sát ô trống thời gian thực và quản lý tập trung. Hệ thống tận dụng các dịch vụ AWS Serverless & Containerization (Amazon RDS PostgreSQL, Amazon ECS Fargate, Amazon ECR, Amazon CloudFront và AWS Amplify) nhằm đảm bảo tính sẵn sàng cao, khả năng mở rộng linh hoạt và tối ưu chi phí vận hành mà không cần phụ thuộc vào bộ cân bằng tải đắt đỏ.

### 2. Tuyên bố vấn đề
*Vấn đề hiện tại*  
Các bãi đỗ xe truyền thống đang gặp nhiều hạn chế:
- **Thu thập & quản lý thủ công**: Người lái xe mất nhiều thời gian tìm ô trống, gây ùn tắc giao thông nội bộ bãi xe.
- **Thiếu giám sát thời gian thực**: Ban quản lý không nắm bắt chính xác mật độ ô trống và lưu lượng xe theo thời gian thực.
- **Rủi ro thất thoát & chi phí nhân sự cao**: Kiểm soát xe ra vào phụ thuộc vào vé giấy hoặc thẻ từ thủ công, dễ phát sinh sai sót và gian lận.

*Giải pháp*  
Hệ thống Smart Parking System giúp người dùng có thể đăng ký trước chỗ trống, sinh QR giữ chỗ, thanh toán trước. Hệ thống sử dụng AI (Computer Vision) để tự động quét nhận diện biển số và QR tại cổng vào/ra.
- **Backend & Cơ sở dữ liệu**: Đóng gói trong Docker Container, lưu trữ image trên Amazon ECR và vận hành trên nền tảng Serverless Amazon ECS Fargate. Lưu trữ dữ liệu giao dịch và thông tin xe an toàn với Amazon RDS PostgreSQL.
- **Mạng phân phối & Giao diện**: Amazon CloudFront CDN kết nối trực tiếp đến ECS Backend giúp giảm độ trễ truyền tải dữ liệu thời gian thực; AWS Amplify lưu trữ ứng dụng Web Fullstack (Next.js/React) cho phép tài xế và ban quản lý truy cập bảng điều khiển (Dashboard) mọi lúc, mọi nơi.
- **Bảo mật**: Phân quyền chi tiết bằng AWS IAM và bảo vệ hạ tầng với Security Groups. (Bảo mật này chỉ sử dụng để demo, nếu triển khai production có thể sử dụng những service bảo mật cao hơn như WAF,...)

*Lợi ích và hoàn vốn đầu tư (ROI)*  
- Giảm 60% thời gian tìm kiếm chỗ đỗ xe cho người điều khiển phương tiện.
- Tự động hóa 90% quy trình kiểm soát xe vào/ra, cắt giảm chi phí nhân sự vận hành bãi xe.
- Tối ưu chi phí hạ tầng tối đa nhờ loại bỏ Load Balancer (ALB) không cần thiết và áp dụng mô hình Serverless/Pay-as-you-go của AWS.
- Thời gian hoàn vốn đầu tư (ROI) ước tính từ 6 đến 12 tháng.

### 3. Kiến trúc giải pháp
Hệ thống áp dụng kiến trúc hiện đại kết hợp AI và AWS Cloud Services để xử lý luồng dữ liệu thời gian thực từ các bãi đỗ xe:

![Architecture](/images/2-Proposal/FINAL_ARCHITECTURE.png)

*Dịch vụ AWS sử dụng*  
- **AWS CLI & IAM**: Quản lý dòng lệnh và phân quyền truy cập bảo mật theo nguyên tắc quyền tối thiểu.
- **Amazon RDS (PostgreSQL)**: Cơ sở dữ liệu quan hệ quản lý lưu trữ dữ liệu biển số, lịch sử ra/vào và trạng thái ô đỗ.
- **Amazon ECR (Elastic Container Registry)**: Lưu trữ và quản lý các Docker Container Images an toàn.
- **Amazon ECS (AWS Fargate)**: Điều phối và chạy ứng dụng Backend Container ở chế độ Serverless không cần quản lý máy chủ.
- **Amazon CloudFront**: Mạng phân phối nội dung (CDN) toàn cầu trỏ trực tiếp nguồn về ECS Service giúp tăng tốc truyền tải API & dữ liệu thời gian thực.
- **AWS Amplify**: Triển khai và lưu trữ ứng dụng Frontend Web Fullstack với quy trình tự động hóa CI/CD.

*Thiết kế thành phần*  
- **Thiết bị camera & xử lý AI**: Camera ghi hình tại cổng ra/vào và các ô đỗ, mô hình AI trích xuất biển số xe & trạng thái ô trống.
- **Tiếp nhận & xử lý backend**: Amazon CloudFront định tuyến trực tiếp yêu cầu API về cụm ECS Fargate Tasks xử lý logic nghiệp vụ.
- **Lưu trữ dữ liệu**: Amazon RDS PostgreSQL lưu trữ dữ liệu giao dịch; Amazon ECR lưu trữ hình ảnh ứng dụng.
- **Giao diện người dùng (Dashboard)**: AWS Amplify cung cấp giao diện Web hiển thị sơ đồ bãi xe thời gian thực cho khách hàng và ban quản lý.

### 4. Triển khai kỹ thuật
*Các giai đoạn triển khai*  
1. **Nghiên cứu & Thiết kế kiến trúc**: Nghiên cứu mô hình AI nhận diện biển số và vẽ kiến trúc tổng thể AWS (Tháng 1).
2. **Xây dựng & Đóng gói Container**: Xây dựng backend ứng dụng, đóng gói Docker Images và đưa lên Amazon ECR (Tháng 1 - Tháng 2).
3. **Triển khai Hạ tầng AWS Cloud**: Khởi tạo RDS PostgreSQL, VPC, ECS Fargate Cluster, CloudFront CDN và AWS Amplify (Tháng 2).
4. **Tích hợp & Kiểm thử End-to-End**: Kết nối toàn bộ luồng từ camera/AI -> ECS Backend -> RDS Database -> Amplify Frontend (Tháng 2 - Tháng 3).

*Yêu cầu kỹ thuật*  
- **Hệ thống AI Biên**: Mô hình Computer Vision (YOLO/OCR) tối ưu chạy trên thiết bị biên hoặc máy chủ trung tâm.
- **Hạ tầng AWS Cloud**: Yêu cầu kiến thức vận hành AWS CLI, Docker, Amazon ECR, Amazon ECS Fargate, Amazon RDS PostgreSQL, CloudFront CDN và AWS Amplify.

### 5. Lộ trình & Mốc triển khai
- **Giai đoạn 1 (Tuần 1 - 4)**: Tìm hiểu kiến thức AWS cơ bản, phân quyền IAM, thiết lập VPC & khởi tạo CSDL Amazon RDS PostgreSQL.
- **Giai đoạn 2 (Tuần 5 - 7)**: Đóng gói Docker Container, đẩy ECR, triển khai cụm ECS Fargate, tích hợp CloudFront & AWS Amplify.
- **Giai đoạn 3 (Tuần 8 - 9)**: Triển khai cao điểm dự án Workshop, tích hợp end-to-end toàn bộ hệ thống bãi đỗ xe thông minh.
- **Giai đoạn 4 (Tuần 10 - 12)**: Đánh giá an toàn bảo mật, tối ưu hóa chi phí vận hành (Cost Optimization) và tổng kết báo cáo.

### 6. Ước tính ngân sách
Chi phí hạ tầng được tính toán dựa trên [AWS Pricing Calculator](https://calculator.aws/):

*Chi phí hạ tầng AWS ước tính hàng tháng:*
- **Amazon RDS PostgreSQL (db.t4g.micro / Free Tier)**: ~14.50 USD/tháng (0.00 USD nếu dùng Free Tier).
- **Amazon ECS Fargate (0.25 vCPU, 0.5 GB RAM)**: ~9.00 USD/tháng.
- **Amazon ECR (Lưu trữ 5 GB Container Images)**: ~0.50 USD/tháng.
- **Amazon CloudFront (10 GB Data Transfer Out)**: ~0.85 USD/tháng.
- **AWS Amplify (Hosting & Build time)**: ~1.50 USD/tháng.
- **Route 53 & Tên miền**: ~1.00 USD/tháng.

*Tổng chi phí AWS ước tính*: **~27.35 USD/tháng** (Ước tính < 10 USD/tháng khi áp dụng gói AWS Free Tier và không phát sinh chi phí ALB).

### 7. Đánh giá rủi ro
*Ma trận rủi ro*  
- **Sự cố mất kết nối mạng Internet**: Ảnh hưởng Cao, Xác suất Trung bình.
- **Lỗi nhận diện AI do ánh sáng/biển số mờ**: Ảnh hưởng Trung bình, Xác suất Trung bình.
- **Vượt ngân sách chi phí AWS**: Ảnh hưởng Trung bình, Xác suất Thấp.

*Chiến lược giảm thiểu*  
- **Mạng**: Thiết lập bộ đệm dữ liệu cục bộ (Local Caching) tại thiết bị biên khi mất mạng tạm thời.
- **AI**: Kết hợp xử lý tiền ảnh (Pre-processing) và cho phép xác nhận thủ công trên Dashboard khi độ tin cậy AI < 85%.
- **Chi phí**: Cấu hình cảnh báo ngân sách AWS Budgets khi chi phí vượt quá 80% ngưỡng dự kiến.

*Kế hoạch dự phòng*  
- Sử dụng CloudFormation / AWS CDK để khôi phục nhanh toàn bộ hạ tầng trong trường hợp gặp sự cố.
- Chuyển sang chế độ nhập biển số thủ công trên Web Dashboard nếu camera gặp hỏng hóc.

### 8. Kết quả kỳ vọng
*Cải tiến kỹ thuật*: Tự động hóa hoàn toàn quy trình nhận diện và quản lý bãi đỗ xe theo thời gian thực. Hạ tầng đám mây Serverless tối giản không cần ALB giúp tối ưu chi phí vận hành tối đa.  
*Giá trị dài hạn*: Cung cấp nguồn dữ liệu chuẩn hóa cho các bài toán phân tích giao thông đô thị, tối ưu chi phí vận hành bãi xe và nâng cao trải nghiệm người dùng.

### 9. Demo một số kết quả đạt được

**Giao diện menu-login**

![Menu-login](/images/2-Proposal/menu_login.png)

**Giao diện booking**

![Booking](/images/2-Proposal/menu_booking.png)

**Giao diện admin**

![Admin](/images/2-Proposal/menu_admin.png)

**Giao diện thanh toán VNPay**

![VNPay1](/images/2-Proposal/vnp1.png)

![VNPay2](/images/2-Proposal/vnp2.png)