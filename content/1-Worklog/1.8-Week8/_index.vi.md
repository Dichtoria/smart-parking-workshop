---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Bước vào giai đoạn cao điểm triển khai dự án Workshop (Giai đoạn 1): Chuẩn bị hạ tầng điện toán, phân quyền bảo mật và khởi tạo hệ thống lưu trữ/cơ sở dữ liệu.
* Đóng gói ứng dụng vào Container và đẩy thành công các bản build Docker Image lên kho chứa riêng tư trên đám mây.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Chuẩn bị môi trường làm việc, khởi tạo cấu hình công cụ lệnh AWS CLI và thiết lập các vai trò IAM Roles bảo mật cho hệ thống | 14/07/2026 | 14/07/2026 | Nội dung tổng hợp của nhóm |
| 3 | - Thiết lập hệ thống Cơ sở dữ liệu quan hệ Amazon RDS (PostgreSQL Engine) phục vụ lưu trữ dữ liệu chính cho dự án | 15/07/2026 | 15/07/2026 | Nội dung tổng hợp của nhóm |
| 4 | - Cấu hình chuỗi quy tắc kiểm soát truy cập an toàn (Security Groups) cho các cổng giao tiếp của cơ sở dữ liệu RDS | 16/07/2026 | 16/07/2026 | Nội dung tổng hợp của nhóm |
| 5 | - Khởi tạo kho chứa Container riêng tư trên Amazon Elastic Container Registry (Amazon ECR) | 17/07/2026 | 17/07/2026 | Nội dung tổng hợp của nhóm |
| 6 | - Đóng gói ứng dụng Backend/Services thành các Docker Container Images và thực hiện push an toàn lên Amazon ECR | 18/07/2026 | 18/07/2026 | Nội dung tổng hợp của nhóm |

### Kết quả đạt được tuần 8:

* Hoàn thành khởi tạo môi trường lệnh CLI và phân quyền IAM bảo mật toàn diện cho hạ tầng dự án.
* Triển khai thành công cụm Cơ sở dữ liệu quan hệ Amazon RDS PostgreSQL hoạt động ổn định.
* Cấu hình tường lửa Security Group khóa chặt cổng kết nối cơ sở dữ liệu, đảm bảo tiêu chuẩn bảo mật.
* Đóng gói thành công ứng dụng vào Docker Container và đẩy hoàn tất các Container Images lên Amazon ECR.
