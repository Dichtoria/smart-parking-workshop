---
title: "Deploy Frontend with AWS Amplify"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.6.2. </b> "
---

# Step 10: Deploy Frontend with AWS Amplify

> **💡 Why choose AWS Amplify Hosting?**  
> - **Automated GitHub CI/CD Pipeline**: AWS Amplify links directly with your GitHub repository. Whenever code is committed to the `main` branch, Amplify automatically triggers the Build (`npm run build`) and Deploy pipeline without manual intervention.  
> - **Optimized Web Hosting & Environment Governance**: Amplify serves compiled static React assets globally with built-in CDN acceleration, offering centralized and secure environment variable management (`VITE_API_URL`).

---

Finally, connect your source code from GitHub to deploy the user interface and link it with the Backend API.

#### Steps:

1. Log in to **AWS Management Console** and search for **AWS Amplify**.
2. On the Amplify homepage, scroll down to **Amplify Hosting** (Static Web Hosting).
3. Click **Get started** or **Host your web app** depending on your UI interface.
4. On the repository selection screen, check **GitHub** ➔ Click **Continue**.
5. A GitHub authorization popup opens: Log in and click **Authorize AWS Amplify** to grant source code read permissions.

![GitHub](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/github.png)

6. Automatically redirected back to AWS Amplify:
   - Under **Recently updated repositories**, select your Frontend React repository.
   - Under **Branch**, select the branch for automated deployment (usually `main` or `master`).
   - Ensure *“Connecting a monorepo”* checkbox is UNCHECKED.

   ![Choose repo](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/choose_repo.png)

   - Click **Next**.
7. Scroll down to **Advanced settings**:
   - Under **Environment variables**, click **Add variable**.
   - **Key**: Enter variable name (e.g. `VITE_API_URL`).
   - **Value**: Paste public IP or CloudFront HTTPS URL (`https://d123456xxxx.cloudfront.net`).

   ![Environment variables](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/ip_be.png)

8. Name the app, set build command to `npm run build` and output to `dist` (or `frontend/dist`). Or fill the YAML file.

![App name](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/app_name.png)

![YML file](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/yml.png)

9. Review configurations ➔ Click **Deploy**.

![Review](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/review.png)

10. Once complete, click the public domain URL to access the live website.

![Deploying](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/deploying.png)

![Done](/images/5-Workshop/5.6-CloudFront-Amplify/5.6.2-amplify/deploy_complete.png)
