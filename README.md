# EC2 Nginx Website Hosting

Hosted a static website on AWS EC2 using Nginx.

## Project Overview

This project demonstrates how to launch an EC2 instance, install Nginx, configure security groups, and host a custom static website.

## Services Used

- AWS EC2
- Amazon Linux 2023
- Nginx
- Security Groups
- EC2 Instance Connect

## Architecture

User Browser → Public IP → EC2 Instance → Nginx → HTML Website

## Steps Performed

### 1. Created EC2 Instance
- Launched Amazon Linux 2023 EC2 instance
- Allowed SSH (22) and HTTP (80)
- Connected using EC2 Instance Connect

### 2. Installed Nginx

```bash
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
