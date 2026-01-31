# 🌐 AWS EC2 Static Website – Deployment Guide 🚀

This document provides the complete end-to-end deployment process for hosting  
a static website on Amazon EC2 using a custom VPC, secure networking, and an  
Apache web server. All resources are created manually in the AWS Console  
following AWS best practices. ✅

---

## ☁️ AWS Environment

- **AWS Region:** us-east-1 🌎  
- **AMI:** Amazon Linux 2023 🐧  
- **Instance Type:** t2.micro 💻  
- **Web Server:** Apache (httpd) 🌐  
- **Public IP Used for Testing:** 54.82.232.14 🔢  

---

## 🛜 VPC Configuration

A custom Virtual Private Cloud (VPC) was created to isolate the network  
environment.

- **VPC Name:** my-vpc-01  
- **IPv4 CIDR Block:** 10.1.0.0/16  

📸 **Screenshot Reference:**  
screenshots/02_VPC_structure.jpeg

---

## 📡 Subnet Configuration

Two subnets were created inside the VPC.

### 🌍 Public Subnet
- **CIDR Block:** 10.1.1.0/24  
- **Availability Zone:** us-east-1a  
- **Purpose:** Internet-facing resources  

### 🔒 Private Subnet
- **CIDR Block:** 10.1.2.0/24  
- **Availability Zone:** us-east-1b  
- **Purpose:** Internal and isolated resources  

---

## 🌐 Internet Gateway

An Internet Gateway was created and attached to the VPC.

- **Internet Gateway Name:** my-igw  
- **Attached VPC:** my-vpc-01  

---

## 🧭 Route Table Configuration

A public route table was created to enable internet access.

### 📤 Public Route Table
- **Route:** 0.0.0.0/0 → Internet Gateway  
- **Associated Subnet:** Public Subnet  

The private subnet uses the default local route and does not have direct  
internet access. 🚫🌍

---

## 🔐 Security Group Configuration

- **Security Group Name:** web-sg  
- **VPC:** my-vpc-01  

### 📥 Inbound Rules
- **HTTP (Port 80):** 0.0.0.0/0  
- **SSH (Port 22):** Administrator Public IP  

### 📤 Outbound Rules
- **All traffic allowed**  

📸 **Screenshot Reference:**  
screenshots/03_server_connect_IP.jpeg

---

## 🖥️ EC2 Instance Deployment

An EC2 instance was launched with the following configuration:

- **AMI:** Amazon Linux 2023  
- **Instance Type:** t2.micro  
- **Subnet:** Public Subnet  
- **Auto-assign Public IP:** Enabled  
- **Security Group:** web-sg  

🏷️ **Tag:**  
Name = static-web-server  

---

## 🔑 SSH Access to EC2

The instance was accessed using SSH from the local machine.

ssh -i key.pem ec2-user@54.82.232.14  

📸 **Screenshot Reference:**  
screenshots/03_server_connect_IP.jpeg

---

## 🌐 Apache Web Server Installation

Apache was installed and configured using the following commands:

sudo yum install httpd -y  
sudo systemctl start httpd  
sudo systemctl enable httpd  

📸 **Screenshot Reference:**  
screenshots/06_server_run.jpeg

---

## 📁 Website Deployment

The static website file was created in the Apache document root.

cd /var/www/html  
sudo nano index.html  

### 📝 Website Content

Welcome to My Static Website hosted on EC2  

📂 **File Location:**  
website/index.html  

---

## ✅ Validation and Testing

The deployment was validated by accessing the EC2 public IP address in a web  
browser.

http://54.82.232.14  

The website loaded successfully and displayed the expected output. 🎉

📸 **Screenshot Reference:**  
screenshots/06_server_run.jpeg

---

## 🧩 Architecture Diagrams

- **High-Level Architecture:**  
  architecture/01_architecture_high_level.png  

- **VPC and Networking Architecture:**  
  architecture/02_architecture_vpc_network.png  

- **EC2 and Apache Request Flow:**  
  architecture/03_architecture_ec2_apache_flow.png  

---

## ⭐ Best Practices Followed

✔️ Custom VPC for network isolation  
✔️ Public and private subnet separation  
✔️ Least privilege SSH access  
✔️ Security groups used as a firewall  
✔️ Apache configured for auto-start  
✔️ Clear and structured documentation  

---

## 🏁 Conclusion

This project demonstrates a complete real-world implementation of hosting a  
static website on AWS EC2 using secure networking and proper infrastructure  
design. The deployment follows AWS best practices and provides hands-on  
experience with core AWS services. 🚀
