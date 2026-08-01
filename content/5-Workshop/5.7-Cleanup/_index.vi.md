---
title: "Dọn dẹp tài nguyên"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 5.7. </b> "
---

# Dọn dẹp Tài nguyên Cloud (Resource Cleanup)

Sau khi hoàn thành các bước thử nghiệm bài thực hành Workshop, việc xóa dọn dẹp các tài nguyên đã khởi tạo là nguyên tắc quan trọng hàng đầu giúp tránh phát sinh chi phí ngoài ý muốn trên tài khoản AWS.

Hãy thực hiện xóa dọn dẹp tài nguyên theo đúng trình tự đảo ngược dưới đây:

---

### 1. Xóa ứng dụng AWS Amplify Hosting

1. Truy cập dịch vụ **AWS Amplify Console**.
2. Chọn ứng dụng `smart-parking-frontend` của bạn.
3. Tại menu bên trái, chọn **App settings** ➔ Select **General settings**.
4. Nhấn nút **Delete app** ➔ Nhập chữ `delete` xác nhận và bấm **Delete**.

---

### 2. Vô hiệu hóa & Xóa Amazon CloudFront Distribution

1. Truy cập dịch vụ **CloudFront Console**.
2. Tích chọn Distribution `d123456xxxx.cloudfront.net` đã tạo.
3. Nhấn nút **Disable** ➔ Chờ khoảng 1-2 phút đến khi trạng thái chuyển sang Disabled.
4. Tích chọn lại Distribution ➔ Nhấn nút **Delete** để xóa hoàn toàn.

---

### 3. Xóa ECS Service & ECS Cluster

1. Truy cập dịch vụ **Amazon ECS Console**.
2. Chọn cụm `parkflow-cluster` ➔ Chuyển sang tab **Services**.
3. Chọn service `parkflow-backend-service` ➔ Nhấn nút **Update service**:
   - Chỉnh sửa **Desired tasks** về `0` ➔ Nhấn **Update**.
4. Tích chọn service `parkflow-backend-service` ➔ Nhấn nút **Delete service** ➔ Nhập `delete` để xác nhận.
5. Quay lại danh sách Clusters ➔ Tích chọn `parkflow-cluster` ➔ Nhấn nút **Delete cluster** ➔ Nhập `delete parkflow-cluster` để xóa cụm máy chủ.

---

### 4. Xóa ECR Repository

1. Truy cập dịch vụ **Amazon ECR Console**.
2. Tại danh sách **Repositories**, tích chọn kho `parkflow_backend`.
3. Nhấn nút **Delete** ➔ Nhập `delete` để xác nhận xóa toàn bộ Docker Container Images lưu trữ.

---

### 5. Xóa Cơ sở dữ liệu Amazon RDS PostgreSQL

1. Truy cập dịch vụ **Amazon RDS Console** ➔ Chọn mục **Databases**.
2. Tích chọn cơ sở dữ liệu `parkflow-db`.
3. Tại menu **Actions**, chọn **Delete**.
4. Bỏ chọn ô *Create final snapshot?* (Không tạo bản chụp đĩa cuối cùng để tránh tốn dung lượng).
5. Tích chọn ô *I acknowledge that upon database deletion, automated backups...*.
6. Nhập dòng chữ `delete me` vào ô xác nhận và nhấn **Delete**.

---

### 6. Xóa IAM User & Access Keys

1. Truy cập dịch vụ **AWS IAM Console** ➔ Chọn mục **Users**.
2. Chọn user `parking-admin`.
3. Tại tab **Security credentials**, cuộn xuống mục Access keys ➔ Chọn **Delete** để hủy mã truy cập.
4. Nhấn nút **Delete user** ở góc trên để thu hồi hoàn toàn người dùng quản trị.

---

> **Chúc mừng bạn đã hoàn thành trọn vẹn bài thực hành Workshop Triển khai Hệ thống Bãi đỗ xe Thông minh trên AWS Cloud!**
