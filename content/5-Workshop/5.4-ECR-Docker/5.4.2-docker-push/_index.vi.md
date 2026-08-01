---
title: "Đóng gói Docker và Push Image"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

# Bước 6: Đóng gói Docker và Push Image

Thực hiện đóng gói mã nguồn Backend thành Docker Image và đẩy trực tiếp lên kho lưu trữ ECR đã tạo.

#### Các bước thực hiện:

1. Mở Terminal (hoặc Command Prompt) trên máy tính cá nhân của bạn, di chuyển đến thư mục chứa file thiết lập Docker (dẫn vô thư mục `backend`).
2. Lần lượt sao chép từng câu lệnh trên màn hình console (từ cửa sổ **View push commands** ở Bước 5) và dán vào Terminal để chạy. Quá trình này bao gồm: Đăng nhập, Xây dựng (Build) Image, Gắn thẻ (Tag) và Đẩy (Push) lên Cloud.

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/build.png)

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/push.png)

3. Nếu thành công, nó sẽ hiện logs trên mục images của repo.

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/logs.png)
