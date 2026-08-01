---
title: "Cấu hình Task Definition cho ECS"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.5.1. </b> "
---

# Bước 7: Cấu hình Task Definition cho ECS

Task Definition đóng vai trò như một bản thiết kế, định nghĩa cách các Container của bạn sẽ chạy trên dịch vụ ECS (có thể chỉnh biến môi trường trực tiếp thông qua task).

#### Các bước thực hiện:

1. Truy cập vào **AWS Management Console** và tìm kiếm dịch vụ **Elastic Container Service (ECS)**.
2. Ở thanh menu bên trái, chọn **Task definitions**.
3. Nhấn vào nút **Create new task definition with JSON** (Tạo bản vẽ cấu hình mới).  
   *(Ở bước này có thể set-up thủ công, nhưng nếu có file json được cấu hình trước thì tốt)*.
4. Copy nội dung file `ecs-task-definition.json` dán vào ➔ **Create**.

![Task Definition](/images/5-Workshop/5.5-ECS-Fargate/5.5.1-task-definition/complete.png)
