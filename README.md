# ☁️ AWS EC2 Static Website Deployment using Nginx & Docker

<p align="center">

<img src="https://img.shields.io/badge/AWS-EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white"/>
<img src="https://img.shields.io/badge/Ubuntu-26.04-E95420?style=for-the-badge&logo=ubuntu&logoColor=white"/>
<img src="https://img.shields.io/badge/Nginx-Web%20Server-009639?style=for-the-badge&logo=nginx&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Linux-Ubuntu-FCC624?style=for-the-badge&logo=linux&logoColor=black"/>
<img src="https://img.shields.io/badge/HTML5-Website-E34F26?style=for-the-badge&logo=html5&logoColor=white"/>

</p>

<p align="center">

A complete cloud deployment project demonstrating how to deploy a static website on an AWS EC2 instance using Ubuntu, Nginx, Linux, and Docker while following basic DevOps practices.

</p>

---

# 📚 Table of Contents

* About the Project
* Project Objectives
* Project Architecture
* Features
* Tech Stack
* Project Structure
* Deployment Workflow
* Linux Commands Used
* Docker Bonus Task
* Screenshots
* Challenges Faced
* Learning Outcomes
* Future Improvements
* Author

---

# 📖 About the Project

This project demonstrates the complete process of deploying a static website on an **Amazon EC2 Ubuntu Server**.

The deployment includes creating and configuring an EC2 instance, setting up Security Groups, connecting securely using SSH, installing the Nginx web server, replacing the default Nginx page with a custom HTML dashboard, and verifying the deployment through both the browser and Linux commands.

As an additional task, Docker was installed on the EC2 instance and the official **hello-world** container was executed successfully.

This project helped me gain practical experience with AWS cloud infrastructure, Linux server administration, Docker, GitHub documentation, and the overall deployment workflow followed in DevOps.

---

# 🎯 Project Objectives

* Launch an Amazon EC2 Ubuntu instance.
* Configure AWS Security Groups.
* Connect securely using SSH.
* Install and configure Nginx.
* Deploy a custom HTML website.
* Verify successful deployment.
* Perform Linux server administration tasks.
* Install Docker on the EC2 instance.
* Execute the Docker hello-world container.
* Organize the project using GitHub.

---

# 🏗 Project Architecture

<p align="center">

<img src="architecture.png" width="900">

</p>

---

# ✨ Features

* 🚀 AWS EC2 Instance Deployment
* 🔐 Secure SSH Authentication using PEM Key
* 🌐 Nginx Web Server Installation
* 🎨 Custom Responsive HTML Dashboard
* 📡 Website Accessible through Public IP
* 💻 Linux Server Administration
* 🐳 Docker Installation on EC2
* ✅ Docker Hello-World Container Execution
* 📂 Well Organized Project Structure
* 📸 Complete Documentation with Screenshots

---

# 🛠 Tech Stack

| Technology                                                           | Purpose              |
| -------------------------------------------------------------------- | -------------------- |
| <img src="https://skillicons.dev/icons?i=aws" width="30"/> AWS EC2   | Cloud Infrastructure |
| <img src="https://skillicons.dev/icons?i=ubuntu" width="30"/> Ubuntu | Operating System     |
| <img src="https://skillicons.dev/icons?i=nginx" width="30"/> Nginx   | Web Server           |
| <img src="https://skillicons.dev/icons?i=docker" width="30"/> Docker | Container Platform   |
| <img src="https://skillicons.dev/icons?i=git" width="30"/> Git       | Version Control      |
| <img src="https://skillicons.dev/icons?i=github" width="30"/> GitHub | Repository Hosting   |
| <img src="https://skillicons.dev/icons?i=html" width="30"/> HTML5    | Static Website       |

---

# 📂 Project Structure

```text
aws-devops-nginx-deployment/
│
├── README.md
├── architecture.png
├── report.pdf
│
├── website/
│   └── index.html
│
├── commands/
│   └── linux-commands.txt
│
└── screenshots/
    ├── 01-ec2-instance.png
    ├── 02-security-group.png
    ├── 03-ssh-login.png
    ├── 04-nginx-installation.png
    ├── 05-nginx-status.png
    ├── 06-custom-dashboard.png
    ├── 07-linux-commands.png
    ├── 08-browser-output.png
    └── 09-docker-bonus.png
```

---

#  Deployment Workflow

## Step 1 — Launch EC2 Instance

Created an Ubuntu 26.04 LTS EC2 instance in the **Mumbai (ap-south-1)** AWS Region.

Configured Security Group rules:

* SSH (Port 22)
* HTTP (Port 80)

---

## Step 2 — Connect to EC2

Connected securely using the generated PEM key.

```bash
ssh -i aws-devops-key.pem ubuntu@<Public-IP>
```

---

## Step 3 — Update Ubuntu Packages

```bash
sudo apt update
```

Updating packages ensures the latest software versions and security updates are available before installation.

---

## Step 4 — Install Nginx

```bash
sudo apt install nginx -y
```

Nginx was installed as the web server responsible for serving the HTML website.

---

## Step 5 — Verify Nginx

```bash
sudo systemctl status nginx
```

Verified that the Nginx service was active and running.

---

## Step 6 — Deploy Custom Website

The default Nginx landing page was replaced with a custom-designed HTML dashboard.

The website became accessible using the EC2 Public IPv4 Address.

---

## Step 7 — Verify Website

```bash
curl http://localhost
```

The command successfully returned the HTML page, confirming that the web server was working correctly.

---

## Step 8 — Linux Administration

The following Linux commands were used during the deployment process.

| Command               | Purpose                   |
| --------------------- | ------------------------- |
| hostname              | Display server hostname   |
| whoami                | Show logged-in user       |
| pwd                   | Display current directory |
| df -h                 | Check disk usage          |
| free -h               | Check memory usage        |
| ps aux                | Display running processes |
| curl http://localhost | Verify local website      |

---

# 🐳 Docker Bonus Task

Docker was installed successfully on the EC2 instance.

Installation:

```bash
sudo apt install docker.io -y
```

Start Docker:

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

Verify Docker:

```bash
docker --version
```

Run Docker Test Container:

```bash
sudo docker run hello-world
```

The successful execution of the **hello-world** container confirmed that Docker was installed and functioning correctly.

---

# 📸 Screenshots

The repository contains screenshots of every major step performed during the project.

* EC2 Instance Creation
* Security Group Configuration
* SSH Login
* Nginx Installation
* Nginx Service Status
* Custom Dashboard Deployment
* Linux Commands
* Browser Output
* Docker Bonus Task

---

# ⚡ Challenges Faced

During the project, I encountered and resolved several practical issues:

* Fixed SSH private key permission issues while connecting from WSL.
* Configured Security Group rules to make the website publicly accessible.
* Replaced the default Nginx landing page with a custom HTML dashboard.
* Verified the web server using browser access and Linux commands.
* Installed Docker and confirmed successful container execution.

These troubleshooting steps provided valuable hands-on experience with Linux server administration.

---

# 📚 Learning Outcomes

This project helped me develop practical knowledge of:

* AWS EC2
* Ubuntu Linux
* SSH Authentication
* Nginx Configuration
* Static Website Hosting
* Docker Installation
* Linux System Administration
* Git and GitHub
* Cloud Deployment Workflow
* Basic DevOps Practices

---

# 🚀 Future Improvements

Possible enhancements for this project include:

* Deploy using Docker Compose
* Configure HTTPS using SSL/TLS
* Register a custom domain with Route 53
* Automate deployment using GitHub Actions
* Monitor the server using Amazon CloudWatch
* Provision infrastructure using AWS CloudFormation
* Configure reverse proxy and load balancing
* Deploy a dynamic web application

---

# 👩‍💻 Author

## Priyamvada

**B.Tech – Information Technology**

KIET Group of Institutions

📧 **Email:** [priyamvadachaudhary7078@gmail.com](mailto:priyamvadachaudhary7078@gmail.com)

🔗 **GitHub:** https://github.com/priyamvada7078

🔗 **LinkedIn:** https://www.linkedin.com/in/priyamvada7078

---

## 🌐 Live Demo

The website is hosted on AWS EC2.

**Public URL**

http://35.154.253.141

> The server was active at the time of assignment submission.

# ⭐ Acknowledgement

This project was completed as part of an AWS DevOps internship assessment to demonstrate practical knowledge of cloud infrastructure, Linux administration, web server deployment, Docker basics, and project documentation.

Thank you for taking the time to review this project.
