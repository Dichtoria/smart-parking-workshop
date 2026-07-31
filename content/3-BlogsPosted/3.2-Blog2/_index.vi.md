---
title: "Blog 2: Amazon EventBridge Scheduler"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Amazon EventBridge Scheduler | Một dịch vụ nhỏ nhưng rất hữu ích khi làm project trên AWS

![Amazon EventBridge Scheduler](/images/3-BlogsPosted/2.jpeg)

Bài viết chia sẻ trải nghiệm sử dụng **Amazon EventBridge Scheduler** để tự động hóa các tác vụ lập lịch theo thời gian trên AWS mà không cần khởi tạo hay quản lý máy chủ Cron Job thủ công.

Các điểm chính cần nắm:

* **Không cần duy trì máy chủ (Serverless)**: Thay thế hoàn toàn việc tạo EC2 chỉ để chạy Cron Job, giúp tiết kiệm chi phí vận hành và không tốn công quản trị server.
* **Dễ dàng tích hợp hệ sinh thái AWS**: Cho phép gọi trực tiếp các dịch vụ như AWS Lambda, Amazon ECS, AWS Step Functions, Amazon SNS, SQS và EventBus chỉ với vài thao tác cấu hình.
* **Lập lịch linh hoạt**: Hỗ trợ đa dạng kiểu lập lịch từ chạy một lần (One-time), chạy định kỳ (Recurring), biểu thức Rate Expression đến Cron Expression.
* **Tính năng hỗ trợ nâng cao**: Tích hợp sẵn cơ chế thử lại (Retry) khi lỗi, vùng thời gian linh hoạt (Flexible Time Window) chống quá tải và lưu vết tác vụ hỏng qua Dead-letter Queue (DLQ).

Dịch vụ giúp đơn giản hóa quy trình tự động hóa các tác vụ định kỳ cho dự án, tiêu biểu như tự động kích hoạt AWS Lambda cập nhật dữ liệu mỗi 30 phút trong môi trường thực hành.

* **Đường dẫn tài liệu chi tiết**: [Amazon EventBridge Scheduler User Guide](https://docs.aws.amazon.com/scheduler/latest/UserGuide/what-is-scheduler.html)