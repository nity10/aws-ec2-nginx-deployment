# aws-ec2-nginx-deployment
Project 1: Linux Web Server Deployment (EC2 &amp; NGINX)
# 🚀 High-Performance Web Server Deployment on AWS

## 📌 Project Overview
This project demonstrates the provisioning of a cloud-based web infrastructure using **Amazon EC2**. The goal was to deploy a lightweight **NGINX** web server on **Amazon Linux 2023** to handle HTTP traffic, simulating a real-world web hosting environment.

## 🛠 Tech Stack
- **Cloud Provider:** AWS (Free Tier)
- **Compute:** EC2 (t2.micro)
- **OS:** Amazon Linux 2023
- **Web Server:** NGINX 1.24
- **Protocols:** HTTP (Port 80), SSH (Port 22)

## ⚙️ Implementation Steps

### 1. Infrastructure Provisioning
- Launched an EC2 instance using the **Amazon Linux 2023 AMI**.
- Configured **Security Groups** to function as a virtual firewall:
  - **Inbound Rule 1:** SSH (Port 22) - Restricted access for management.
  - **Inbound Rule 2:** HTTP (Port 80) - Public access for web traffic.

### 2. Configuration & Automation (Commands Used)
I connected via SSH and performed the following system administration tasks:

```bash
# 1. Update the OS package repository to ensure security patches
sudo yum update -y

# 2. Install the NGINX web server
sudo yum install nginx -y

# 3. specific version check to verify installation
nginx -v

# 4. Enable the service to start automatically on system boot
sudo systemctl enable nginx

# 5. Start the web server immediately
sudo systemctl start nginx
