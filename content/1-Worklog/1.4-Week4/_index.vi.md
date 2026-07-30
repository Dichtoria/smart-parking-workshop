---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Nắm vững kỹ thuật đóng gói ứng dụng bằng Docker Container và quản lý kho chứa ảnh riêng tư trên Amazon ECR (Elastic Container Registry).
* Xây dựng Docker Image nhẹ, tối ưu và thực hiện quy trình đăng nhập/push/pull container image lên Amazon ECR.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu tổng quan công nghệ Containerization vs Virtual Machines (VMs) <br>- Cài đặt Docker Engine, tìm hiểu kiến trúc Docker Daemon, Client & Image Layers | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Tìm hiểu cú pháp viết `Dockerfile` (FROM, WORKDIR, COPY, RUN, EXPOSE, CMD/ENTRYPOINT) <br>- **Thực hành:** Viết Dockerfile đóng gói ứng dụng Web Node.js / Python và build Docker Image | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Tìm hiểu dịch vụ lưu trữ container Amazon Elastic Container Registry (ECR): Repositories, Image Tags, Image Scanning & IAM Authorization Tokens | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **Thực hành Amazon ECR:** <br>&emsp; + Tạo Private ECR Repository trên AWS Management Console <br>&emsp; + Sử dụng AWS CLI đăng nhập xác thực `aws ecr get-login-password` | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Thực hành:** Gắn tag (`docker tag`) và push Docker Image thành công lên Amazon ECR, kiểm tra tính năng quét lỗ hổng bảo mật Image Vulnerability Scanning | 20/06/2026 | 20/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 4:

* Thành thạo quy trình đóng gói ứng dụng web vào container bằng Dockerfile chuẩn tối ưu dung lượng.
* Khởi tạo và quản lý kho lưu trữ container riêng tư trên Amazon ECR.
* Xác thực thành công giữa Docker CLI cục bộ và dịch vụ AWS ECR thông qua AWS CLI token.
* Tải (push) và quản lý phiên bản container image an toàn trên kho lưu trữ đám mây Amazon ECR.
