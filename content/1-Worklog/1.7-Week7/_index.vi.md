---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Nghiên cứu nền tảng AWS Amplify dành cho việc phát triển và lưu trữ ứng dụng Web/Mobile Fullstack.
* Thiết lập đường ống tự động hóa triển khai (CI/CD Pipeline) kết nối kho mã nguồn GitHub và tích hợp dịch vụ xác thực Amazon Cognito.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan nền tảng AWS Amplify Hosting & AWS Amplify Studio <br>- So sánh triển khai Web ứng dụng tĩnh (SSG) vs Động (SSR - Server Side Rendering) với Next.js/React | 07/07/2026 | 07/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Thực hành AWS Amplify Hosting:** <br>&emsp; + Kết nối tài khoản GitHub repository chứa mã nguồn ứng dụng Web <br>&emsp; + Cấu hình file build specification (`amplify.yml`) và các môi trường (Branch deployments) | 08/07/2026 | 08/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Cấu hình biến môi trường (Environment Variables), thiết lập Custom Domains và chứng chỉ SSL tự động trên AWS Amplify | 09/07/2026 | 09/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Nghiên cứu tích hợp dịch vụ quản lý người dùng Amazon Cognito (User Pools & Identity Pools) với ứng dụng Amplify | 10/07/2026 | 10/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Thực hành:** Kiểm thử luồng CI/CD tự động (khi push code mới lên branch `main` GitHub, Amplify tự động trigger build & deploy phiên bản mới) | 11/07/2026 | 11/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 7:

* Nắm vững cách xây dựng và triển khai ứng dụng Web Fullstack hiện đại bằng AWS Amplify.
* Xây dựng thành công quy trình tự động hóa CI/CD liên kết trực tiếp với GitHub Repository.
* Quản lý linh hoạt các môi trường phát triển (Preview Branches) và cấu hình biến môi trường an toàn.
* Tích hợp cơ chế xác thực người dùng Amazon Cognito và hoàn tất chuẩn bị cho giai đoạn cao điểm dự án.
