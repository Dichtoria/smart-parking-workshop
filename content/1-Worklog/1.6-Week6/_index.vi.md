---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Tìm hiểu mạng phân phối nội dung toàn cầu Amazon CloudFront (Content Delivery Network - CDN).
* Tối ưu hóa hiệu năng, giảm độ trễ truy cập, tích hợp chứng chỉ SSL/TLS (ACM) và thiết lập bảo vệ ứng dụng web.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu tổng quan Amazon CloudFront: Khái niệm CDN, Edge Locations, Regional Edge Caches <br>- Phân biệt các loại Nguồn (Origins): S3 Bucket, ECS Service Domain/IP hoặc Custom Origin | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Tìm hiểu cơ chế Caching Behaviors, TTL (Time-To-Live), Query String & Header forwarding <br>- **Thực hành:** Tạo CloudFront Distribution trỏ đến S3 Bucket chứa website tĩnh | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Tăng cường bảo mật S3 Origin bằng Origin Access Control (OAC) / Origin Access Identity (OAI) nhằm ngăn chặn truy cập trực tiếp vào S3 | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Cấu hình tên miền tùy chỉnh (Custom Domain) kết hợp chứng chỉ HTTPS miễn phí từ AWS Certificate Manager (ACM) <br>- Tìm hiểu lệnh xóa cache CloudFront Invalidation | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Thực hành:** <br>&emsp; + Tạo CloudFront Distribution trỏ nguồn trực tiếp về cụm ứng dụng ECS Fargate <br>&emsp; + Thực hiện gửi lệnh Create Invalidation và kiểm tra tốc độ tải trang toàn cầu qua Edge Location | 04/07/2026 | 04/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 6:

* Thấu hiểu nguyên lý hoạt động của mạng phân phối nội dung toàn cầu Amazon CloudFront CDN.
* Triển khai thành công CloudFront Distribution giúp tăng tốc đáng kể tốc độ phản hồi cho trang web.
* Khóa an toàn S3 Bucket Origin bằng OAC, chỉ cho phép truy cập duy nhất thông qua CloudFront CDN.
* Nắm vững quy trình cấu hình chứng chỉ bảo mật HTTPS (SSL/TLS) và lệnh xóa bộ nhớ đệm CloudFront Invalidation.
