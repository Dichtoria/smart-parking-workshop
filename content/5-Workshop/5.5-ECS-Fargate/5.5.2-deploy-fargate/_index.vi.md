---
title: "Triển khai và Chạy ECS Service"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.5.2. </b> "
---

# Bước 8: Triển khai và Chạy ECS Service

> **💡 Tại sao lựa chọn Amazon ECS Fargate (Serverless Container)?**  
> Vận hành ứng dụng bãi đỗ xe đòi hỏi hệ thống co giãn linh hoạt theo lưu lượng xe vào/ra thực tế. **AWS Fargate** cung cấp môi trường Container Serverless không máy chủ — bạn không cần phải tốn thời gian quản lý, nâng cấp hay vá lỗi hệ điều hành EC2. AWS Fargate tự động mở rộng tài nguyên khi cao điểm, tự phục hồi Task khi gặp lỗi và giúp tối ưu 100% chi phí vận hành.

---

Trong bước này, chúng ta sẽ tạo Cluster và Service để vận hành ứng dụng Backend trên hạ tầng Fargate không máy chủ.

#### 1. Tạo cụm máy chủ (Cluster):
- Tại màn hình của dịch vụ ECS, chọn mục **Clusters** ở menu bên trái.
- Nhấn nút **Create cluster**.
- Nhập tên Cluster: `parkflow-cluster` ➔ **Create**.

![Create Cluster](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/create_cluster.png)

#### 2. Tạo Dịch vụ (Service) trong Cluster:
- Bấm vào tên Cluster bạn vừa tạo (`parkflow-cluster`).
- Tại tab **Services**, nhấn nút **Create**.
- Tại phần **Compute options**, đảm bảo chọn **Fargate**.
- Tại phần **Deployment configuration**:
  - **Task definition family**: `parkflow-backend-task`
  - **Service name**: `parkflow-backend-service`
  - **Networking (quan trọng)**: VPC chọn `default`, subnet bỏ chọn những subnet private (ví dụ: `RDS-Pvt-subnet-2`,...)
  - **Public IP**: Phải **On**.

![Networking](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/create_service.png)

- Nhấn nút **Create**.

Khi vừa tạo xong, services sẽ tự động chạy dựa trên Task Definition đã setup từ trước.

![Creating](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/creating.png)

![Complete](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/complete.png)

Khi mục task hoàn thành, ta có thể lấy được địa chỉ Public IP khi nhấn vào Task đang chạy.

![Public IP](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/publicip_1.png)

![Public IP](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/publicip_2.png)

*(Khi đó là done backend nhé!)*
