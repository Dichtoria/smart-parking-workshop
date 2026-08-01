---
title: "Cấu hình AWS CloudFront (CDN)"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.6.1. </b> "
---

# Bước 9: Cấu hình AWS CloudFront (CDN)

CloudFront giúp cung cấp chứng chỉ HTTPS miễn phí và tăng tốc độ truy cập API cho ứng dụng của bạn.

AWS CloudFront sẽ tự động bọc IP HTTP `http://18.141.13.150:8000` thành một đường dẫn HTTPS Miễn Phí do AWS cấp có dạng: `https://d123456xxxx.cloudfront.net`!

#### Các bước thực hiện:

1. Truy cập vào dịch vụ CloudFront trên giao diện AWS Console và nhấn nút **Create a CloudFront distribution**.
2. Chọn **free plan**.
3. **Distribution name**: Đặt theo ý muốn.
4. Tại phần **Origin domain** (chọn custom cloudfront), dán đường dẫn của cụm ECS Fargate (hoặc Application Load Balancer) mà bạn đã có được ở bước trước.
5. Chọn **custom origin setting**.
6. Trong phần **Protocol**, chọn **HTTP only**, chọn port **8000**.

![CloudFront](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.1-cloudfront/creating_1.png)

![CloudFront](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.1-cloudfront/creating_2.png)

7. Nhấn nút **Create distribution** ở cuối trang và chờ quá trình khởi tạo hoàn tất.
8. Sau khi trạng thái chuyển sang thành công, hãy sao chép **Distribution domain name** mới này. Đây chính là địa chỉ API siêu an toàn của bạn. Hãy ghi nhớ nó để sử dụng điền vào biến `VITE_API_URL` khi triển khai Frontend.
