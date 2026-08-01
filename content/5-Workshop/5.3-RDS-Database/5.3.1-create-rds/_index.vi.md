---
title: "Khởi tạo Amazon RDS (PostgreSQL)"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.3.1. </b> "
---

# Bước 3: Khởi tạo Amazon RDS (PostgreSQL)

Cơ sở dữ liệu là thành phần quan trọng nhất. Chúng ta sẽ sử dụng dịch vụ RDS để vận hành PostgreSQL một cách ổn định.

#### Các bước thực hiện:

1. Truy cập vào **AWS Management Console** và tìm kiếm dịch vụ **RDS**.
2. Chọn **Create database** (Tạo cơ sở dữ liệu) ➔ **Full Configuration**.
3. Thiết lập cấu hình Database:
   - **Engine Type**: PostgreSQL
   - **Creation method**: Full Configuration
   - **Templates**: Sandbox (với quy mô demo dự án nhỏ, tiết kiệm chi phí)

   ![RDS](/images/5-Workshop/5.3-RDS-Database/5.3.1-create-rds/postgres.png)

4. Trong phần **Settings**:
   - **DB instance identifier**: `parkflow-db`
   - **Master username**: `postgres`
   - **Credentials management**: Self managed (để có thể tự set mật khẩu theo cá nhân)

   ![RDS](/images/5-Workshop/5.3-RDS-Database/5.3.1-create-rds/db_instance.png)

5. Ở phần **Instance configuration**:
   - Tự lựa chọn Instance Types theo quy mô của project, ở đây chọn `db.t4g.micro`.
6. Tại mục **Connectivity**:
   - **Public access**: Chọn **Yes**  
     *(Lưu ý: Trong thực tế sản xuất, bạn nên chọn No. Chúng ta bật để máy local của bạn kết nối được phục vụ quá trình thực hành demo)*.
7. Mở tab **Additional configuration**:
   - Đặt tên cho database: `smart_parking`

   ![RDS](/images/5-Workshop/5.3-RDS-Database/5.3.1-create-rds/db_name.png)

8. Nhấn **Create database** (Đợi khoảng 5-10 phút để hệ thống khởi tạo).

![RDS](/images/5-Workshop/5.3-RDS-Database/5.3.1-create-rds/complete.png)
