# 🚀 AWS EC2 Static Website Deployment  
### *Complete Cloud Infrastructure Documentation*

---

## 📖 About This Project
This repository contains **complete end-to-end documentation** for deploying a
**static website on AWS EC2** using a **custom VPC, subnets, security groups, and
Apache web server**.

> 🎯 **Focus:** Cloud infrastructure setup + server deployment + documentation  
> 🧠 **Purpose:** Learning, reference, and interview-ready AWS project

---

## 🏆 Project Objective
- Design AWS infrastructure **from scratch**
- Configure **secure networking**
- Deploy a **Linux web server**
- Document **each step clearly in one place**

---

## ☁️ AWS Services Used
| Service | Purpose |
|------|--------|
| Amazon EC2 | Host the web server |
| Amazon VPC | Custom cloud network |
| Subnets | Public & Private isolation |
| Internet Gateway | Internet access |
| Route Tables | Traffic routing |
| Security Groups | Firewall rules |
| Apache (httpd) | Web server |

---

## 🏗️ Architecture Summary
- **VPC CIDR:** `10.1.0.0/16`
- **Public Subnet:** `10.1.1.0/24` (Internet facing)
- **Private Subnet:** `10.1.2.0/24` (Internal use)
- **Internet Gateway:** Attached to VPC
- **Public Route Table:** `0.0.0.0/0 → IGW`
- **EC2 Instance:** Amazon Linux 2 (t2.micro)

---

## 📘 📌 MAIN DOCUMENTATION (IMPORTANT)
👉 **All steps, commands, and explanations are written in ONE place here:**

### 🔗 [Deployment Guide – Full Step-by-Step Documentation](documents/deployment-guide.md)

This guide includes:
- AWS Console steps (VPC, Subnets, Routes)
- Security Group configuration
- EC2 provisioning
- SSH connection
- `sudo` terminal commands
- Website deployment
- Validation & testing

---

## 💻 Server Commands Reference
All EC2 terminal commands executed on the server:
👉 [Apache Setup Commands](commands/setup-commands.md)

---

## 🌐 Website Content
Static website deployed on EC2:
👉 [index.html](website/index.html)

---

## 📸 Validation Proof
Screenshots showing:
- EC2 running
- Security group rules
- Website output

👉 [View Screenshots](screenshots/)

---

## 🔐 Best Practices Implemented
- 🔒 SSH access restricted to admin IP
- 🌐 Public subnet only where required
- 🧱 Security groups used as firewall
- 💰 Cost-efficient instance selection
- 📄 Documentation-first approach

---

## 🎓 Learning Outcomes
- AWS VPC & networking fundamentals
- EC2 server deployment
- Linux web server configuration
- Cloud security basics
- Professional cloud documentation

---

## 🏁 Conclusion
This repository serves as a **complete AWS EC2 deployment documentation**
showing how a static website can be securely hosted on the cloud using
properly designed infrastructure components.

> ✅ Beginner friendly  
> ✅ Interview ready  
> ✅ Resume worthy  
> ✅ Real-world AWS project

---

### 📌 Final Note
📄 **Full documentation:** `documents/deployment-guide.md`  
🖥️ **Server work:** Performed on EC2 (not local machine)  
📦 **Version control:** Managed using Git & GitHub

---
