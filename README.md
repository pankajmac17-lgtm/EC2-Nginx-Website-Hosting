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

<!--bash
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudosystemctl status nginx -->

### 3. Verified Nginx Status

sudo systemctl status nginx

### 4. Navigated to Nginx HTML Directory

cd /usr/share/nginx/html
ls

### 5. Edited index.html
<!--
<!DOCTYPE html>
<html>
<head>
    <title>My AWS Website</title>
</head>
<body>
    <h1>Welcome to My AWS EC2 Website</h1>
    <p>This website is hosted on Amazon EC2 using Nginx.</p>
    <p>Created by Pankaj Jangid</p>
</body>
</html>
-->

### 6. Restarted Nginx
sudo systemctl restart nginx

### 7. Accessed Website

Opened the public IP in browser and verified the website was accessible.

## Commands Used
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl status nginx
cd /usr/share/nginx/html
sudo nano index.html
sudo systemctl restart nginx



