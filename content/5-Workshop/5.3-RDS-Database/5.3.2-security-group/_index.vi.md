---
title: "Cấu hình Security Group cho RDS"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.3.2. </b> "
---

# Bước 4: Cấu hình Security Group cho RDS

Việc thiết lập quy tắc bảo mật giúp máy local và các dịch vụ khác của AWS có thể kết nối được tới Database.

Sau khi RDS hiển thị trạng thái Available, bạn cần cho phép máy tính cá nhân kết nối đến nó:

#### Các bước thực hiện:

1. Bấm vào tên cơ sở dữ liệu `parkflow-db`.
2. Tại tab **Connectivity & security**, tìm mục Security và bấm vào link của **VPC security groups**.
3. Ta sẽ được chuyển qua tab Security Group của EC2 để cấp quyền cho các IP có thể truy cập được vào database.
4. Chọn Security Group đó, chuyển sang tab **Inbound rules** ➔ bấm **Edit inbound rules**.
5. Thêm một quy tắc mới:
   - **Type**: PostgreSQL
   - **Port range**: 5432
   - **Source**: Chọn **Anywhere-IPv4** (`0.0.0.0/0`) hoặc **My IP**.
6. Sang tab **Outbound rules** ➔ **Edit outbound rules** (sau này sẽ giúp ECS gọi database):
   - **Type**: All traffic
   - **Port range**: 5432
   - **Destination**: Chọn **Anywhere-IPv4** (`0.0.0.0/0`) hoặc **My IP**.

   ![Security Group](/images/5-Workshop/5.3-RDS-Database/5.3.2-security-group/inb.png)

   ![Security Group](/images/5-Workshop/5.3-RDS-Database/5.3.2-security-group/outb.png)


7. Bấm **Save rules**.
8. Quay lại trang chi tiết RDS, sao chép địa chỉ **Endpoint** (Ví dụ: `ecommerce-ai-db.xxxxxx.rds.amazonaws.com`).
