---
title: "Prerequisites & AWS CLI Setup"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

# Prerequisites & AWS CLI Setup

> **💡 Why AWS IAM & AWS CLI?**  
> - **AWS IAM**: Enforces the Principle of Least Privilege. Creating a dedicated IAM User (`parking-admin`) with scoped permissions instead of using the Root account secures cloud infrastructure against unauthorized modifications.  
> - **AWS CLI v2**: Enables command-line automation. Configuring the CLI allows local development tools (Docker, Git scripts) to authenticate, build, and deploy cloud resources seamlessly without repetitive manual Console actions.

---

### 1. System & Development Environment Requirements

Before starting the hands-on workshop, ensure your local workstation meets the following tool and software version requirements:

- **AWS Account**: 01 Active AWS Account with administrative access or an AWS Educate / Credit account.
- **Node.js & npm**: **Node.js v18.x LTS** or **v20.x LTS or higher** (`node -v`) and **npm v9.x+** (`npm -v`) to run the React Frontend & Express Backend.
- **Python**: **Python 3.9+ or higher** (`python --version`) for running automation and AI processing scripts.
- **Docker Desktop**: **Docker Engine v24.0+ or higher** (`docker --version`) running locally to package container images.
- **Git CLI**: **Git v2.35+ or higher** (`git --version`) configured with your GitHub account.
- **AWS CLI v2**: **AWS Command Line Interface version 2.x** (`aws --version`).

---

### 2. Step 1: Create IAM User & Assign Policies

To perform cloud resource operations securely following least-privilege principles, create a dedicated IAM user:

1. Log in to the **AWS Management Console** and navigate to **IAM (Identity and Access Management)**.
2. In the left navigation menu, select **Users** ➔ Click **Create user**.
3. Under **User details**:
   - **User name**: Enter `parking-admin`.
4. Under **Set permissions**:
   - Select **Attach policies directly**.
   - Search for and select the following 3 service administrator policies:
     - `AmazonEC2ContainerRegistryFullAccess` (ECR image push/pull permissions).
     - `AmazonECS_FullAccess` (ECS Fargate cluster operation permissions).
     - `AmazonRDSFullAccess` (Amazon RDS database management permissions).

    ![IAM](/images/5-Workshop/5.2-Prerequiste/iam.png)

5. Click **Next** ➔ Review configurations and click **Create user**.

---

### 3. Step 2: Create Access Keys & Configure AWS CLI

Generate access credentials for user `parking-admin` so the local AWS CLI tool can authenticate with AWS:

#### Create Access Key & Secret Access Key

1. In the **Users** list, click user `parking-admin`.
2. Navigate to the **Security credentials** tab.
3. Scroll down to **Access keys** ➔ Click **Create access key**.

![Accesskey](/images/5-Workshop/5.2-Prerequiste/accesskey.png)

4. Under **Access key best practices & alternatives**:
   - Select **Command Line Interface (CLI)**.
   - Check the confirmation box *I understand the above recommendation and want to proceed to create an access key*.
   - Click **Next** ➔ Click **Create access key**.
5. Securely save the 2 credential strings displayed on the screen:
   - **Access Key ID**: (Example: `AKIAIOSFODNN7EXAMPLE`)
   - **Secret Access Key**: (Example: `wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY`)

#### Execute AWS CLI Configuration

Open **Terminal** (macOS/Linux) or **PowerShell** (Windows) on your computer and execute:

```bash
aws configure
```

Enter the parameters sequentially when prompted:

```text
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: ap-southeast-1
Default output format [None]: json
```

*(Note: We select region `ap-southeast-1` - Singapore to ensure minimal network latency for the project)*.

Verify successful AWS CLI authentication by running:

```bash
aws sts get-caller-identity
```

If the terminal outputs your UserId, Account, and Arn for `parking-admin`, you are ready for the next step!