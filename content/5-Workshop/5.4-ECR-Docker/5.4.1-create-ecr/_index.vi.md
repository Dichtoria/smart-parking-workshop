---
title: "Truy cập Amazon ECR và Tạo Kho Lưu Trữ"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.4.1. </b> "
---

# Bước 5: Truy cập Amazon ECR và Tạo Kho Lưu Trữ

> **💡 Tại sao sử dụng Amazon ECR (Elastic Container Registry)?**  
> **Amazon ECR** là kho lưu trữ Docker Image riêng tư (Private Container Registry) tích hợp sâu vào hệ sinh thái AWS. Sử dụng ECR giúp lưu trữ an toàn mã nguồn ứng dụng đã đóng gói, tự động quét lỗ hổng bảo mật (Vulnerability Scanning) và giúp cụm máy chủ ECS kéo (pull) Image về khởi chạy với độ trễ cực thấp trong cùng mạng nội bộ AWS.

---

Amazon ECR là nơi lưu trữ các Docker Image của ứng dụng trước khi được triển khai lên ECS.

#### Các bước thực hiện:

1. Đăng nhập vào **AWS Management Console** và tìm kiếm dịch vụ **Elastic Container Registry (ECR)**.
2. Tại màn hình chính của ECR, nhấn vào nút **Create repository** để bắt đầu tạo kho lưu trữ mới.
3. **Đặt tên**: `parkflow_backend`.
4. Giữ nguyên các cài đặt mặc định còn lại, cuộn xuống cuối trang và nhấn nút **Create repository**.

![Create Repository](/images/5-Workshop/5.4-ECR-Docker/5.4.1-create-ecr/create_repo.png)

5. ECR cung cấp các câu lệnh thực thi như 1 hướng dẫn để push các docker image, chọn repo vừa tạo.

![Create Repository](/images/5-Workshop/5.4-ECR-Docker/5.4.1-create-ecr/complete.png)

6. Ở góc phải chọn **View push commands**.

![Create Repository](/images/5-Workshop/5.4-ECR-Docker/5.4.1-create-ecr/push_commands.png)

7. Lúc này, AWS sẽ hiển thị một bảng Popup chứa 4 bước thực hiện tương ứng với 4 câu lệnh. Các câu lệnh này đã được AWS tự động điền sẵn ID Tài khoản AWS của bạn, Region và Tên Repository mà bạn vừa đặt.

![Create Repository](/images/5-Workshop/5.4-ECR-Docker/5.4.1-create-ecr/commands.png)
