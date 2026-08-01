---
title: "Đóng gói Docker và Push Image"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

# Bước 6: Đóng gói Docker và Push Image

> **💡 Tại sao chọn giải pháp đóng gói ứng dụng bằng Docker Container?**  
> - **Tích hợp mô hình Trí tuệ nhân tạo (AI & Computer Vision)**: Ứng dụng Bãi đỗ xe thông minh kết hợp mô hình AI tự động nhận diện biển số xe (ANPR) sử dụng các thư viện như OpenCV, Python và Node.js. Việc cài đặt thủ công các thư viện AI phức tạp này trên server truyền thống rất dễ gây ra lỗi xung đột phiên bản (Dependency Drift).  
> - **Tính đóng gói đồng nhất ("Build Once, Run Anywhere")**: Docker giúp gom toàn bộ mã nguồn Backend, môi trường chạy, các thư viện phụ thuộc AI và cấu hình vào trong **01 Container Image duy nhất**. Điều này đảm bảo ứng dụng chạy chính xác 100% từ môi trường Local cho đến khi triển khai lên đám mây AWS mà không sợ bị xung đột hệ điều hành hay thiếu thư viện.

---

Thực hiện đóng gói mã nguồn Backend thành Docker Image và đẩy trực tiếp lên kho lưu trữ ECR đã tạo.

#### Các bước thực hiện:

1. Mở Terminal (hoặc Command Prompt) trên máy tính cá nhân của bạn, di chuyển đến thư mục chứa file thiết lập Docker (dẫn vô thư mục `backend`).
2. Lần lượt sao chép từng câu lệnh trên màn hình console (từ cửa sổ **View push commands** ở Bước 5) và dán vào Terminal để chạy. Quá trình này bao gồm: Đăng nhập, Xây dựng (Build) Image, Gắn thẻ (Tag) và Đẩy (Push) lên Cloud.

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/build.png)

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/push.png)

3. Nếu thành công, nó sẽ hiện logs trên mục images của repo.

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/logs.png)
