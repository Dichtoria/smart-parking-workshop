---
title: "Configure Security Group for RDS"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.3.2. </b> "
---

# Step 4: Configure Security Group for RDS

> **💡 Why configure EC2 Security Groups?**  
> An **EC2 Security Group** acts as a stateful virtual firewall controlling inbound and outbound network traffic. Scoping access strictly to PostgreSQL port `5432` protects the relational database from public port scanners and guarantees that only authorized backend services can connect.

---

Configuring security rules enables your local workstation and other AWS services to connect to the database.

Once RDS displays the Available status, allow your local computer to connect:

#### Steps:

1. Click database name `parkflow-db`.
2. Under the **Connectivity & security** tab, locate Security and click the **VPC security groups** link.
3. You will be redirected to the EC2 Security Groups console to grant IP access to the database.
4. Select the Security Group, switch to the **Inbound rules** tab ➔ click **Edit inbound rules**.
5. Add a new rule:
   - **Type**: PostgreSQL
   - **Port range**: 5432
   - **Source**: Select **Anywhere-IPv4** (`0.0.0.0/0`) or **My IP**.
6. Switch to the **Outbound rules** tab ➔ **Edit outbound rules** (Helps ECS call the database later):
   - **Type**: All traffic
   - **Port range**: 5432
   - **Destination**: Select **Anywhere-IPv4** (`0.0.0.0/0`) or **My IP**.

   ![Security Group](/images/5-Workshop/5.3-RDS-Database/5.3.2-security-group/inb.png)

   ![Security Group](/images/5-Workshop/5.3-RDS-Database/5.3.2-security-group/outb.png)

7. Click **Save rules**.
8. Return to the RDS details page and copy the **Endpoint** address (Example: `ecommerce-ai-db.xxxxxx.rds.amazonaws.com`).
