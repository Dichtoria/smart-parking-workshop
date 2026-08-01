---
title: "Workshop: Smart Parking System"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Triển khai Hệ thống Bãi đỗ xe Thông minh (Smart Parking System) tích hợp AI & AWS Cloud

#### Tổng quan Bài thực hành

Workshop này hướng dẫn từng bước quy trình xây dựng và triển khai một **Hệ thống bãi đỗ xe thông minh (Smart Parking System)** hoàn chỉnh trên đám mây AWS. Hệ thống tích hợp công nghệ AI (nhận diện biển số tự động ANPR & quét mã QR đặt chỗ), xử lý thanh toán trực tuyến qua cổng VNPay và vận hành hạ tầng trên dịch vụ Container Serverless.

#### Mục tiêu Học tập

- Thành thạo thao tác quản lý danh tính và phân quyền an toàn với **AWS IAM & AWS CLI v2**.
- Vận hành Cơ sở dữ liệu quan hệ **Amazon RDS PostgreSQL** kết hợp cấu hình Security Groups đa lớp.
- Đóng gói ứng dụng Backend Node.js bằng **Docker** và quản lý Image trên **Amazon ECR**.
- Điều phối hạ tầng Container Serverless tự động co giãn với **Amazon ECS Fargate**.
- Tăng tốc API và cấp chứng chỉ bảo mật HTTPS tự động bằng **Amazon CloudFront CDN**.
- Triển khai quy trình CI/CD tự động cho Frontend React Vite với **AWS Amplify Hosting**.

#### Nội dung các chuyên mục thực hành

1. [1. Tổng quan về Workshop](5.1-workshop-overview/)
2. [2. Yêu cầu chuẩn bị & Cấu hình AWS CLI](5.2-prerequiste/)
3. [3. Khởi tạo Amazon RDS PostgreSQL & Security Group](5.3-rds-database/)
4. [4. Tạo Kho ECR & Đóng gói Docker Backend](5.4-ecr-docker/)
5. [5. Cấu hình Task Definition & Triển khai ECS Fargate](5.5-ecs-fargate/)
6. [6. Cấu hình CloudFront CDN & Triển khai AWS Amplify](5.6-cloudfront-amplify/)
7. [7. Dọn dẹp tài nguyên](5.7-cleanup/)