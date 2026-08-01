---
title: "Resource Cleanup"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 5.7. </b> "
---

# Cloud Resource Cleanup

After completing the hands-on workshop steps, deleting provisioned cloud resources is a crucial best practice to prevent unexpected charges on your AWS account.

Follow the step-by-step cleanup sequence in reverse order below:

---

### 1. Delete AWS Amplify Hosting App

1. Navigate to **AWS Amplify Console**.
2. Select your `smart-parking-frontend` application.
3. In the left menu, select **App settings** ➔ Select **General settings**.
4. Click **Delete app** ➔ Type `delete` to confirm and click **Delete**.

---

### 2. Disable & Delete Amazon CloudFront Distribution

1. Navigate to **CloudFront Console**.
2. Select the distribution `d123456xxxx.cloudfront.net`.
3. Click **Disable** ➔ Wait 1-2 minutes until status updates to Disabled.
4. Select the distribution again ➔ Click **Delete**.

---

### 3. Delete ECS Service & ECS Cluster

1. Navigate to **Amazon ECS Console**.
2. Select cluster `parkflow-cluster` ➔ Navigate to the **Services** tab.
3. Select service `parkflow-backend-service` ➔ Click **Update service**:
   - Change **Desired tasks** to `0` ➔ Click **Update**.
4. Select service `parkflow-backend-service` ➔ Click **Delete service** ➔ Type `delete` to confirm.
5. Return to the Clusters list ➔ Select `parkflow-cluster` ➔ Click **Delete cluster** ➔ Type `delete parkflow-cluster`.

---

### 4. Delete Amazon ECR Repository

1. Navigate to **Amazon ECR Console**.
2. In the **Repositories** list, select `parkflow_backend`.
3. Click **Delete** ➔ Type `delete` to confirm purging all stored Docker images.

---

### 5. Delete Amazon RDS PostgreSQL Database

1. Navigate to **Amazon RDS Console** ➔ Select **Databases**.
2. Select database `parkflow-db`.
3. From the **Actions** menu, select **Delete**.
4. Uncheck *Create final snapshot?* (To save storage costs).
5. Check *I acknowledge that upon database deletion...*.
6. Type `delete me` into the confirmation field and click **Delete**.

---

### 6. Delete IAM User & Access Keys

1. Navigate to **AWS IAM Console** ➔ Select **Users**.
2. Select user `parking-admin`.
3. Under **Security credentials**, delete active Access keys.
4. Click **Delete user** to revoke all administrator credentials.

---

> **Congratulations on successfully completing the Smart Parking System Deployment Workshop on AWS Cloud!**
