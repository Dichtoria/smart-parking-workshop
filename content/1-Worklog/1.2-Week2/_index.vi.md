---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Nắm vững các khái niệm bảo mật cốt lõi và dịch vụ quản lý danh tính AWS Identity and Access Management (IAM).
* Thiết lập chính sách bảo mật theo nguyên tắc quyền tối thiểu (Least Privilege), quản lý IAM Users, Groups, Roles và MFA.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Nghiên cứu mô hình trách nhiệm chung (Shared Responsibility Model) của AWS <br>- Khái niệm cốt lõi dịch vụ AWS IAM: Users, User Groups, Roles và Policies | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Phân tích cấu trúc file IAM Policy (JSON Format: Effect, Action, Resource, Condition) <br>- Phân biệt AWS Managed Policies vs Customer Managed Policies vs Inline Policies | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Thực hành AWS IAM:** <br>&emsp; + Tạo IAM Users cho các phòng ban và gán vào các IAM Groups tương ứng <br>&emsp; + Kích hoạt xác thực đa yếu tố (MFA - Multi-Factor Authentication) cho Root Account và IAM Users | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Nghiên cứu khái niệm IAM Roles và Trust Relationships <br>- **Thực hành:** Tạo IAM Role cho phép EC2 instance truy cập dịch vụ Amazon S3 an toàn không cần lưu credentials cứng | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Kiểm thử phân quyền IAM bằng công cụ IAM Policy Simulator và thực hiện audit bảo mật bằng AWS Credential Report | 06/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 2:

* Thấu hiểu sâu sắc cơ chế quản lý danh tính và phân quyền trên đám mây AWS.
* Xây dựng cấu trúc quản lý IAM Users/Groups chuẩn hóa, bật MFA bắt buộc nâng cao an toàn tài khoản.
* Viết và tùy chỉnh thành công các IAM Policies đáp ứng tiêu chuẩn quyền tối thiểu (Least Privilege).
* Áp dụng IAM Role cho tài nguyên EC2, loại bỏ rủi ro lộ bí mật Access Key / Secret Key trên môi trường ứng dụng.
