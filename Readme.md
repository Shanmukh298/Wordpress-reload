*****Automated Deployment of a WordPress Website Using Nginx, LEMP Stack, and GitHub Actions*****
----> I successfully set up an automated deployment process for a WordPress website using Nginx, the LEMP stack (Linux, Nginx, MySQL, PHP), and GitHub Actions as the CI/CD automation tool. Below is a step-by-step explanation of how I completed the deployment process, following best security and performance practices.
* Step 1: Server Provisioning
1.1 Setting Up the VPS
I provisioned a Virtual Private Server (VPS) on [AWS/Azure/GCP/DigitalOcean] with Ubuntu 22.04 LTS as the operating system.
The VPS was configured with 1GB RAM and 10GB storage to efficiently run WordPress.
1.2 Securing the ServerTo enhance security: Updated and upgraded all system packages,Configured UFW Firewall to allow only necessary traffic,Disabled root login and password authentication for SSH to prevent unauthorized access.
* Step 2: Installing and Configuring LEMP Stack
I installed the LEMP stack to serve WordPress efficiently.
2.2 Installing MySQL (or MariaDB) for the Database
Installed MySQL server:Created a WordPress database and user with limited privileges,Installed MySQL server,Installing nginx server.
2.3 Installing PHP
Installed PHP and necessary extensions.
* Step 3: Setting Up WordPress:
3.1 Downloading and Configuring WordPress:Configured the database connection,Updated database credentials.
3.2 Configuring Nginx for WordPress: Created a new Nginx configuration file,added the following Nginx configuration,Enabled the configuration and restarted Nginx.
* Step 4: Securing WordPress with SSL (Let's Encrypt):
Installed Certbot for free SSL,Set up automatic SSL renewal.
3.4
Step5:Automating Deployment with GitHub Actions:Created a GitHub repository (e.g., wordpress-deploy),Cloned the repository on the VPS.
5.1: Setting Up the GitHub Repository:Created a GitHub repository (e.g., wordpress-deploy).
Cloned the repository on the VPS.git clone: https://github.com/yourusername/wordpress-deploy.git
5.2 Setting Up GitHub Actions Workflow:Created the GitHub Actions workflow file,Added the deployment script,
5.3 Configuring GitHub Secrets:
Added the following secrets to GitHub repository settings:
SERVER_IP → VPS IP Address
SERVER_USER → ubuntu
SSH_PRIVATE_KEY → Private SSH key.
5.4 Deploying and Testing
Committed and pushed the workflow to
----->GitHub:git add .
---->git commit -m "Automated deployment setup"
---->git push origin main
---->Checked GitHub Actions → Actions tab to verify deployment.

CONCLUSION: This setup allows automatic deployment whenever code is pushed to the main branch. The combination of LEMP, Nginx, SSL, and GitHub Actions ensures a secure, scalable, and automated deployment process.







