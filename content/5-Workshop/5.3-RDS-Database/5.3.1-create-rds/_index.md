---
title: "Provision Amazon RDS (PostgreSQL)"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.3.1. </b> "
---

# Step 3: Provision Amazon RDS (PostgreSQL)

> **💡 Why use Amazon RDS (PostgreSQL)?**  
> The Smart Parking System requires high relational data integrity (ACID compliance) for parking slot availability, user accounts, and VNPay online payment logs. **Amazon RDS (Relational Database Service)** automates complex database management tasks such as periodic backups, security updates, and storage auto-scaling without manual DB server maintenance.

---

The database is the most critical core component. We will utilize the RDS service to run PostgreSQL reliably.

#### Steps:

1. Navigate to **AWS Management Console** and search for **RDS**.
2. Select **Create database** ➔ **Full Configuration**.
3. Database Configuration:
   - **Engine Type**: PostgreSQL
   - **Creation method**: Full Configuration
   - **Templates**: Sandbox (Optimal for small demo project scales and cost savings)

   ![RDS](/images/5-Workshop/5.3-RDS-Database/5.3.1-create-rds/postgres.png)

4. Under **Settings**:
   - **DB instance identifier**: `parkflow-db`
   - **Master username**: `postgres`
   - **Credentials management**: Self managed (Allows custom password setup)

   ![RDS](/images/5-Workshop/5.3-RDS-Database/5.3.1-create-rds/db_instance.png)

5. Under **Instance configuration**:
   - Select instance types matching your project scale, here we choose `db.t4g.micro`.
6. Under **Connectivity**:
   - **Public access**: Select **Yes**  
     *(Note: In production environments, select No. We enable Yes here to permit local workstation connections for lab demonstrations)*.
7. Under **Additional configuration**:
   - Initial database name: `smart_parking`

   ![RDS](/images/5-Workshop/5.3-RDS-Database/5.3.1-create-rds/db_name.png)

8. Click **Create database** (Wait 5-10 minutes for system initialization).

![RDS](/images/5-Workshop/5.3-RDS-Database/5.3.1-create-rds/complete.png)
