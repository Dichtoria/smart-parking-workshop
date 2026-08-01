---
title: "Yêu cầu chuẩn bị & Cấu hình AWS CLI"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

# Yêu cầu chuẩn bị & Cấu hình AWS CLI

> **💡 Tại sao chọn AWS IAM & AWS CLI?**  
> - **AWS IAM**: Giúp tuân thủ nguyên tắc phân quyền tối thiểu (Least Privilege). Việc tạo một IAM User riêng biệt (`parking-admin`) cấp đúng các quyền cần thiết thay vì dùng tài khoản Root giúp bảo vệ an toàn tuyệt đối cho tài nguyên đám mây.  
> - **AWS CLI v2**: Giúp tự động hóa công việc qua dòng lệnh. Việc cấu hình CLI giúp các công cụ local (như Docker, Git script) có thể trực tiếp tương tác, đóng gói và triển khai tài nguyên AWS một cách nhanh chóng mà không cần thao tác thủ công liên tục trên Console.

---

### 1. Chuẩn bị Môi trường & Phần mềm Hệ thống

Trước khi bắt đầu bài thực hành, hãy đảm bảo máy tính cá nhân của bạn đã cài đặt các công cụ và môi trường phiên bản tiêu chuẩn sau:

- **Tài khoản AWS**: 01 Tài khoản AWS đang hoạt động (Active AWS Account) có quyền quản trị IAM hoặc tài khoản sinh viên được cấp AWS Credit.
- **Node.js & npm**: Phiên bản **Node.js v18.x LTS** hoặc **v20.x LTS trở lên** (`node -v`) và **npm v9.x+** (`npm -v`) để vận hành mã nguồn Frontend React & Backend Express.
- **Python**: Phiên bản **Python 3.9+ trở lên** (`python --version`) hỗ trợ chạy các công cụ script AI/ML và tự động hóa.
- **Docker Desktop**: Phiên bản **Docker v24.0+ trở lên** (`docker --version`) đang khởi chạy sẵn sàng trên máy tính để đóng gói Container Image.
- **Git CLI**: Phiên bản **Git v2.35+ trở lên** (`git --version`) đã cấu hình liên kết tài khoản GitHub.
- **AWS CLI v2**: Công cụ dòng lệnh **AWS CLI phiên bản 2.x** (`aws --version`).

---

### 2. Bước 1: Tạo IAM User & Phân quyền Quản trị

Để thực hiện các thao tác triển khai dịch vụ một cách an toàn theo nguyên tắc quyền tối thiểu, ta cần khởi tạo một IAM User dành riêng cho bài thực hành:

1. Đăng nhập vào **AWS Management Console** và tìm kiếm dịch vụ **IAM (Identity and Access Management)**.
2. Tại menu bên trái, chọn mục **Users** ➔ Nhấn nút **Create user**.
3. Tại phần **User details**:
   - **User name**: Nhập `parking-admin`.
4. Tại phần **Set permissions**:
   - Chọn tùy chọn **Attach policies directly**.
   - Tìm kiếm và tích chọn 3 chính sách (Policies) quản trị dịch vụ tương ứng:
     - `AmazonEC2ContainerRegistryFullAccess` (Quyền quản trị ECR đẩy/kéo Docker Image).
     - `AmazonECS_FullAccess` (Quyền quản trị và vận hành cụm máy chủ ECS Fargate).
     - `AmazonRDSFullAccess` (Quyền khởi tạo và quản lý CSDL Amazon RDS).

    ![IAM](/images/5-Workshop/5.2-Prerequiste/iam.png)
5. Nhấn nút **Next** ➔ Kiểm tra lại thông tin và nhấn **Create user**.

---

### 3. Bước 2: Tạo Access Key & Cấu hình AWS CLI

Sau khi khởi tạo người dùng `parking-admin`, ta cần cấp mã định danh Access Key để công cụ AWS CLI trên máy tính cá nhân có thể tương tác trực tiếp với đám mây AWS.

#### Tạo Access Key & Secret Access Key

1. Tại danh sách **Users**, bấm chọn user `parking-admin` vừa khởi tạo.
2. Chuyển sang tab **Security credentials**.
3. Cuộn xuống phần **Access keys** ➔ Nhấn nút **Create access key**.

![Accesskey](/images/5-Workshop/5.2-Prerequiste/accesskey.png)

4. Tại bước **Access key best practices & alternatives**:
   - Chọn tùy chọn **Command Line Interface (CLI)**.
   - Tích chọn xác nhận *I understand the above recommendation and want to proceed to create an access key*.
   - Nhấn **Next** ➔ Nhấn **Create access key**.
5. Lưu trữ an toàn 2 chuỗi ký tự định danh hiển thị trên màn hình:
   - **Access Key ID**: (Ví dụ: `AKIAIOSFODNN7EXAMPLE`)
   - **Secret Access Key**: (Ví dụ: `wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY`)

#### Thực thi cấu hình lệnh AWS CLI

Mở ứng dụng **Terminal** (macOS/Linux) hoặc **PowerShell** (Windows) trên máy tính và chạy câu lệnh:

```bash
aws configure
```

Nhập lần lượt các thông số theo yêu cầu:

```text
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: ap-southeast-1
Default output format [None]: json
```

*(Lưu ý: Chúng ta chọn vùng `ap-southeast-1` - Singapore để đảm bảo độ trễ kết nối thấp nhất cho dự án)*.

Kiểm tra kết nối AWS CLI thành công bằng câu lệnh:

```bash
aws sts get-caller-identity
```

Nếu màn hình trả về thông tin UserId, Account và Arn của `parking-admin`, bạn đã sẵn sàng cho bước tiếp theo!