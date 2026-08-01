---
title: "Triển khai Frontend với AWS Amplify"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.6.2. </b> "
---

# Bước 10: Triển khai Frontend với AWS Amplify

Cuối cùng, chúng ta sẽ kết nối mã nguồn từ GitHub để triển khai giao diện người dùng và liên kết với API Backend.

#### Các bước thực hiện:

1. Đăng nhập vào **AWS Management Console** và tìm kiếm dịch vụ **AWS Amplify**.
2. Tại trang chủ của Amplify, cuộn xuống phần **Amplify Hosting** (Lưu trữ web tĩnh).
3. Nhấn vào nút **Get started** (Bắt đầu) hoặc **Host your web app** tùy thuộc vào giao diện hiển thị.
4. Tại màn hình lựa chọn kho lưu trữ, đánh dấu chọn vào **GitHub** (hoặc GitLab/Bitbucket tùy kho mã nguồn của bạn) ➔ Nhấn **Continue**.
5. Cửa sổ ủy quyền GitHub bật lên: Đăng nhập tài khoản GitHub và nhấn **Authorize AWS Amplify** để cấp quyền cho AWS đọc mã nguồn.

![GitHub](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/github.png)

6. Màn hình tự động chuyển hướng lại giao diện AWS Amplify:
   - Tại mục **Recently updated repositories**, chọn đúng kho lưu trữ mã nguồn Frontend React của bạn.
   - Tại mục **Branch**, chọn nhánh muốn triển khai tự động (thông thường là `main` hoặc `master`).
   - Đảm bảo hộp thoại *“Connecting a monorepo”* KHÔNG được đánh dấu.

   ![Choose repo](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/choose_repo.png)

   - Nhấn **Next**.
7. Cuộn xuống phần **Advanced settings** (Cài đặt nâng cao):
   - Mở mục **Environment variables** ➔ Nhấn **Add variable**.
   - **Key**: Nhập tên biến (Ví dụ: `VITE_API_URL`).
   - **Value**: Dán địa chỉ IP công khai hoặc CloudFront HTTPS URL (`https://d123456xxxx.cloudfront.net`).

   ![Environment variables](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/ip_be.png)

8. Đặt tên app, fill build command bằng `npm run build` và output là `dist` (hoặc `frontend/dist` tùy project). Hoặc fill file yml.

![App name](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/app_name.png)

![YML file](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/yml.png)

9. Review lại mọi thứ ➔ Tiến hành **Deploy**.

![Review](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/review.png)

10. Sau khi hoàn tất, có thể truy cập domain công khai để vào trang web.

![Deploying](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/deploying.png)

![Done](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/deploy_complete.png)

*(Xong rồi đó!)*
