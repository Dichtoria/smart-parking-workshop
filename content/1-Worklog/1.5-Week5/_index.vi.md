---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Tìm hiểu dịch vụ điều phối và vận hành container chuyên nghiệp Amazon Elastic Container Service (ECS).
* Triển khai ứng dụng container chạy trên chế độ Serverless AWS Fargate tối ưu chi phí hạ tầng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu tổng quan Amazon ECS: Kiến trúc ECS Cluster, Task Definitions, Tasks & Services <br>- Phân biệt 2 chế độ khởi chạy: ECS EC2 Launch Type vs ECS Fargate Launch Type (Serverless) | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Tìm hiểu cách cấu hình ECS Task Definition (Container Image URI từ ECR, vCPU, RAM, Port Mappings, Environment Variables) <br>- Cấu hình Task Execution IAM Role | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Thực hành Amazon ECS:** <br>&emsp; + Tạo ECS Cluster trên nền tảng AWS Fargate <br>&emsp; + Khai báo ECS Task Definition sử dụng Docker Image đã đẩy lên ECR ở tuần 4 | 25/06/2026 | 25/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Cấu hình ECS Service, thiết lập số lượng mong muốn (Desired Tasks) và quy tắc mạng VPC Security Groups cho Task | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Thực hành:** Khởi chạy ECS Service trên Fargate, kiểm tra khả năng tự phục hồi khi Task bị dừng và kiểm tra truy cập HTTP/HTTPS trực tiếp đến container | 27/06/2026 | 27/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 5:

* Thấu hiểu mô hình điều phối container Amazon ECS và ưu điểm của mô hình Serverless AWS Fargate.
* Tạo thành công ECS Task Definition định nghĩa đầy đủ tài nguyên phần cứng và thông số container.
* Triển khai ứng dụng container hoạt động ổn định trên AWS Fargate không cần trực tiếp vận hành EC2 instance.
* Định tuyến mạng và cấu hình cổng truy cập an toàn cho cụm ECS Tasks.
