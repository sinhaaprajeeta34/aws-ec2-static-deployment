# AWS EC2 Static Website Deployment

This project demonstrates the complete deployment of a static website on
Amazon EC2 using a custom VPC, public and private subnets, security groups,
and Apache web server. The project follows AWS best practices for networking,
security, and instance management.

## 🚀 Project Objective
The objective of this project is to design and deploy a secure and scalable
AWS infrastructure from scratch and host a static website on an EC2 instance.

## 🧰 AWS Services Used
- Amazon EC2
- Amazon VPC
- Internet Gateway
- Route Tables
- Security Groups
- Apache Web Server (httpd)

## 🏗️ Architecture Overview
- Custom VPC (10.1.0.0/16)
- Public Subnet (10.1.1.0/24) in us-east-1a
- Private Subnet (10.1.2.0/24) in us-east-1b
- Internet Gateway attached to VPC
- Public Route Table with internet access
- EC2 instance deployed in public subnet

## 📘 Detailed Documentation
Complete step-by-step deployment details are available here:
[Deployment Guide](documents/deployment-guide.md)

## ✅ Final Output
The static website is accessible using the public IP address of the EC2
instance and displays the following message:

> Welcome to My Static Website hosted on EC2

## 🏆 Key Learning Outcomes
- Understanding of AWS VPC networking
- Hands-on experience with EC2 provisioning
- Security group configuration for real-world scenarios
- Web server deployment and validation on AWS cloud
