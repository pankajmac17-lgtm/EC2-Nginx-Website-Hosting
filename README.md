# EC2 Nginx Website Hosting

## Project Overview

This project demonstrates how to launch an AWS EC2 instance, install and configure Nginx, and host a custom static website.

The website is hosted on an Amazon Linux 2023 EC2 instance using Nginx as the web server.

---

## Services Used

* AWS EC2
* Amazon Linux 2023
* Nginx
* Security Groups
* EC2 Instance Connect

---

## Architecture

```text
User Browser → Public IP → EC2 Instance → Nginx → HTML Website
```

---

## Steps Performed

### 1. Created EC2 Instance

* Launched an Amazon Linux 2023 EC2 instance
* Allowed inbound traffic for:

  * SSH (Port 22)
  * HTTP (Port 80)
* Connected to the instance using EC2 Instance Connect

---

### 2. Installed Nginx

```bash
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl status nginx
```

---

### 3. Verified Nginx Status

```bash
sudo systemctl status nginx
```

---

### 4. Navigated to Nginx HTML Directory

```bash
cd /usr/share/nginx/html
ls
```

---

### 5. Edited the Website Content

```bash
sudo nano index.html
```

Example HTML content:

```html
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
```

---

### 6. Restarted Nginx

```bash
sudo systemctl restart nginx
```

---

### 7. Accessed the Website

* Opened the EC2 instance public IP address in a web browser
* Verified that the custom website was successfully displayed

Example:

```text
http://<your-public-ip>
```

---

## Commands Used

```bash
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl status nginx
cd /usr/share/nginx/html
sudo nano index.html
sudo systemctl restart nginx
```

---

## Output

The website was successfully hosted on an AWS EC2 instance using Nginx.

Users can access the website using the EC2 public IP address through a web browser.

---

## Learning Outcome

Through this project, the following concepts were learned:

* Launching and configuring EC2 instances
* Managing security groups
* Installing and managing Nginx
* Hosting static websites on AWS
* Using Linux commands for server administration
* Accessing hosted websites through public IP
