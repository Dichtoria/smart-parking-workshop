---
title: "Blog 1: AWS Reliability & Disaster Recovery"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# AWS Reliability & DR | Xây dựng chiến lược khắc phục sự cố (Disaster Recovery) và mạng phân tán trên AWS

Bài viết tìm hiểu giải pháp khắc phục sự cố (Disaster Recovery - DR) trên đám mây AWS nhằm đảm bảo hai chỉ số sống còn là RTO (Recovery Time Objective) và RPO (Recovery Point Objective) thấp nhất cho hệ thống doanh nghiệp qua việc kết hợp AWS Elastic Disaster Recovery (AWS DRS) và AWS Transit Gateway.

![Post1](/images/3-BlogsPosted/1.jpeg)

Các điểm chính cần nắm:

* **AWS Elastic Disaster Recovery (AWS DRS)** cho phép nhân bản liên tục ở mức khối đĩa (Block-level Replication) toàn bộ máy chủ từ On-Premises hoặc cross-region với chi phí tối ưu.
* **Tối ưu chi phí hạ tầng DR**: Dữ liệu chỉ nhân bản về EBS Volumes giá rẻ và chỉ thực sự khởi chạy EC2 Instances khi xảy ra sự cố (Failover).
* **Đồng bộ thời gian thực**: Đảm bảo chỉ số RPO tính bằng giây và RTO tính bằng phút.
* **Quản lý mạng tập trung**: Tận dụng AWS Transit Gateway làm "Hub" kết nối nhiều VPC, loại bỏ sự phức tạp của VPC Peering chồng chéo.
* **Quy trình 3 bước tiêu chuẩn**: Cài đặt DRS Agent -> Cấu hình Launch Settings -> Diễn tập DR Drill định kỳ không làm ảnh hưởng môi trường Production.

Mô hình DR này giúp doanh nghiệp chủ động ứng phó sự cố hạ tầng và đơn giản hóa công tác diễn tập phục hồi cho đội ngũ SysAdmin.