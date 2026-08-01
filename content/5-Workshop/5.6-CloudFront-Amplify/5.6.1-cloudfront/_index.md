---
title: "Configure AWS CloudFront (CDN)"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.6.1. </b> "
---

# Step 9: Configure AWS CloudFront (CDN)

CloudFront provides free HTTPS certificates and accelerates API access for your application.

AWS CloudFront automatically wraps your HTTP IP `http://18.141.13.150:8000` into a Free HTTPS endpoint provided by AWS: `https://d123456xxxx.cloudfront.net`!

#### Steps:

1. Navigate to CloudFront on AWS Console and click **Create a CloudFront distribution**.
2. Select **free plan**.
3. **Distribution name**: Name as desired.
4. Under **Origin domain** (select custom cloudfront), paste your ECS Fargate (or ALB) address obtained from the previous step.
5. Select **custom origin setting**.
6. Under **Protocol**, select **HTTP only**, port **8000**.

![CloudFront](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.1-cloudfront/creating_1.png)

![CloudFront](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.1-cloudfront/creating_2.png)

7. Click **Create distribution** at the bottom and wait for initialization to complete.
8. Once status displays success, copy this new **Distribution domain name**. This is your secure API endpoint. Keep it ready to set in `VITE_API_URL` during Frontend deployment.
