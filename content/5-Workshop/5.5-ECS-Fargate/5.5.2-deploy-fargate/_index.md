---
title: "Deploy & Run ECS Service"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.5.2. </b> "
---

# Step 8: Deploy & Run ECS Service

> **💡 Why choose Amazon ECS Fargate (Serverless Containers)?**  
> Operating backend services for a smart parking platform demands dynamic auto-scaling tailored to fluctuating vehicle entry/exit traffic. **AWS Fargate** provides a serverless container environment eliminating EC2 OS management, patching, and provisioning overhead. Fargate automatically handles compute scaling, task auto-recovery, and optimizes operational costs by charging strictly for active container consumption.

---

In this step, we create the Cluster and Service to run the Backend application on serverless Fargate infrastructure.

#### 1. Create Server Cluster:
- On the ECS service dashboard, select **Clusters** in the left menu.
- Click **Create cluster**.
- Enter Cluster Name: `parkflow-cluster` ➔ Click **Create**.

![Create Cluster](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/create_cluster.png)

#### 2. Create Service within Cluster:
- Click your newly created Cluster name (`parkflow-cluster`).
- Under the **Services** tab, click **Create**.
- Under **Compute options**, ensure **Fargate** is selected.
- Under **Deployment configuration**:
  - **Task definition family**: `parkflow-backend-task`
  - **Service name**: `parkflow-backend-service`
  - **Networking (Critical)**: Select `default` VPC, deselect private subnets (e.g. `RDS-Pvt-subnet-2`,...)
  - **Public IP**: Must be **On**.

![Networking](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/create_service.png)

- Click **Create**.

Upon creation, the service automatically runs based on the pre-configured Task Definition.

![Creating](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/creating.png)

![Complete](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/complete.png)

Once the task finishes initializing, click the running Task to retrieve its Public IP address.

![Public IP](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/publicip_1.png)

![Public IP](/images/5-Workshop/5.5-ECS-Fargate/5.5.2-deploy-fargate/publicip_2.png)
