---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Tìm hiểu dịch vụ Cơ sở dữ liệu quan hệ quản trị Amazon Relational Database Service (Amazon RDS).
* Khởi tạo, cấu hình chuỗi hạ tầng CSDL PostgreSQL/MySQL, cấu hình DB Subnet Groups, Security Groups và các chiến lược sao lưu dữ liệu DB Snapshots.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan về dịch vụ Amazon RDS: Phân biệt tự quản trị CSDL trên EC2 vs Amazon RDS managed service <br>- Tìm hiểu các Database Engines được hỗ trợ: PostgreSQL, MySQL, MariaDB, Oracle, SQL Server | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Nghiên cứu kiến trúc độ sẵn sàng cao Multi-AZ Deployment (Primary & Standby Replica) <br>- Khái niệm Read Replicas tối ưu hiệu năng đọc cho CSDL quan hệ | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Thực hành Amazon RDS:** <br>&emsp; + Tạo DB Subnet Group liên kết các Subnet riêng tư (Private Subnets) <br>&emsp; + Khởi tạo Amazon RDS PostgreSQL instance trong Private Subnet | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Cấu hình VPC Security Group cho RDS instance: Khóa chặt cổng 5432, chỉ cho phép kết nối từ Security Group của EC2/Application layer <br>- Kết nối thử nghiệm từ máy chủ EC2 tới RDS Database | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Tìm hiểu chiến lược sao lưu: Automated Backups & Manual DB Snapshots <br>- **Thực hành:** Tạo Manual Snapshot, khôi phục CSDL từ Snapshot và thực hiện sao chép snapshot | 13/06/2026 | 13/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 3:

* Thấu hiểu kiến trúc CSDL đám mây Amazon RDS và mô hình triển khai Multi-AZ đảm bảo tính sẵn sàng cao.
* Khởi tạo thành công cụm Cơ sở dữ liệu Amazon RDS PostgreSQL nằm an toàn trong Private Subnet.
* Thiết lập tường lửa Security Groups bảo vệ CSDL chỉ nhận kết nối nội bộ từ tầng ứng dụng.
* Nắm vững quy trình tự động hóa sao lưu và khôi phục dữ liệu an toàn bằng DB Snapshots.
