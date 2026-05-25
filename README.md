# 🚀 NGINX + HTTPD Troubleshooting Lab on AWS EC2

![AWS](https://img.shields.io/badge/AWS-EC2-orange)
![Linux](https://img.shields.io/badge/Linux-RedHat-blue)
![NGINX](https://img.shields.io/badge/WebServer-NGINX-green)
![Apache](https://img.shields.io/badge/WebServer-Apache-red)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

# 📌 Project Overview

This project demonstrates real-world Linux web server troubleshooting using NGINX and Apache HTTP Server on a single AWS EC2 instance.

The lab includes:

- NGINX configuration on port 80
- Apache HTTP Server configuration on custom port 83
- Linux troubleshooting
- Port conflict troubleshooting
- SELinux troubleshooting
- Security Group configuration
- Service validation
- Networking verification
- Git & GitHub documentation

This project helped build practical understanding of Linux administration, web server troubleshooting, and AWS networking concepts.

---

# 🎯 Project Objective

The objective of this project is to configure and troubleshoot multiple web servers running simultaneously on a single Linux EC2 instance.

## Key Objectives

- Configure NGINX on port 80
- Configure Apache on custom port 83
- Resolve port conflicts
- Troubleshoot SELinux issues
- Configure AWS Security Groups
- Validate Linux networking
- Practice Linux administration
- Build professional GitHub documentation

---

# 🏗️ Architecture Diagram

```text
AWS Cloud (us-east-2)
│
├── VPC
│
├── EC2 Instance (linux-server)
│   │
│   ├── NGINX
│   │    └── Port 80
│   │
│   └── Apache HTTPD
│        └── Port 83
│
├── Security Group
│    ├── SSH → 22
│    ├── HTTP → 80
│    └── Custom TCP → 83
│
└── Browser Access
      ├── http://PUBLIC-IP
      └── http://PUBLIC-IP:83
```

---

# 📂 Repository Structure

```text
nginx-httpd-troubleshooting-lab/
│
├── README.md
│
├── screenshots/
│   ├── 01-ec2-instance-running.png
│   ├── 02-security-group-rules.png
│   ├── 03-nginx-browser-output.png
│   ├── 04-apache-browser-output-port83.png
│   ├── 05-package-installation-and-verification.png
│   ├── 06-port-verification-ss-command.png
│   └── 07-journalctl-httpd-troubleshooting.png
│
├── commands/
│   ├── nginx-httpd-commands.md
│   ├── selinux-commands.md
│   ├── ss-commands.md
│   ├── journalctl-commands.md
│   └── troubleshooting-commands.md
│
├── notes/
│   ├── nginx-notes.md
│   ├── apache-notes.md
│   ├── selinux-notes.md
│   ├── journalctl-notes.md
│   └── troubleshooting-notes.md
│
└── docs/
    └── project-flow.md
```

---

# 🌍 AWS Region

```text
us-east-2 (Ohio)
```

---

# 🧰 Technologies Used

| Technology | Purpose |
|---|---|
| AWS EC2 | Linux Server |
| NGINX | Web Server |
| Apache HTTPD | Web Server |
| Linux | Server Administration |
| Security Groups | Traffic Control |
| SELinux | Linux Security |
| Git & GitHub | Version Control |

---

# ✅ Prerequisites

- AWS Account
- EC2 Key Pair
- Basic Linux Knowledge
- Networking Fundamentals
- Git & GitHub
- SSH Client

---

# 🚀 Implementation Steps

1. Launched Red Hat Linux EC2 instance
2. Configured Security Group rules for ports 22, 80, and 83
3. Connected EC2 instance using SSH
4. Installed NGINX and Apache HTTP Server
5. Started web server services
6. Configured Apache to listen on port 83
7. Verified listening ports using ss command
8. Troubleshooted service issues using journalctl
9. Configured SELinux for custom Apache port
10. Verified browser access for:
   - NGINX on port 80
   - Apache on port 83

---

# 🐧 Linux Commands Documentation

Detailed command documentation available here:

- [NGINX + HTTPD Commands](commands/nginx-httpd-commands.md)
- [SELinux Commands](commands/selinux-commands.md)
- [SS Networking Commands](commands/ss-commands.md)
- [journalctl Commands](commands/journalctl-commands.md)
- [Troubleshooting Commands](commands/troubleshooting-commands.md)

---

# 📝 Additional Notes

Detailed conceptual and troubleshooting notes available here:

- [NGINX Notes](notes/nginx-notes.md)
- [Apache Notes](notes/apache-notes.md)
- [SELinux Notes](notes/selinux-notes.md)
- [journalctl Notes](notes/journalctl-notes.md)
- [Troubleshooting Notes](notes/troubleshooting-notes.md)

---

# 📄 Project Workflow Documentation

Complete project workflow available here:

- [Project Flow](docs/project-flow.md)

---

# 📸 Screenshots

## EC2 Instance Running

![EC2](./screenshots/01-ec2-instance-running.png)

---

## Security Group Rules

![Security Group](./screenshots/02-security-group-rules.png)

---

## NGINX Browser Output

![NGINX Output](./screenshots/03-nginx-browser-output.png)

---

## Apache Browser Output on Port 83

![Apache Output](./screenshots/04-apache-browser-output-port83.png)

---

# 🔐 Security Concepts Learned

- SELinux
- Linux port security
- AWS Security Groups
- Service isolation
- Custom port management

---

# ⚠️ Challenges Faced

- Apache port conflict
- SELinux blocking custom ports
- Security Group configuration
- Service troubleshooting
- Port validation

---

# 🧠 Key Learning Outcomes

After completing this project, I learned:

- Linux troubleshooting
- NGINX configuration
- Apache configuration
- SELinux troubleshooting
- AWS Security Groups
- Linux networking
- Service management
- Log analysis
- Port troubleshooting
- Real-world DevOps troubleshooting workflow

---

# 🧹 Cleanup

All AWS resources created during this lab were deleted after testing to avoid unnecessary AWS billing charges.

---

# 🚀 Future Improvements

- Configure Reverse Proxy
- Add HTTPS with SSL
- Configure Load Balancer
- Automate using Terraform
- Add Monitoring
- Configure Docker Containers

---

# 👩‍💻 Author

**Jaishree Chaure**

Passionate about AWS, Linux, Networking, and DevOps Engineering.  
Currently building hands-on cloud and infrastructure projects to strengthen practical skills in AWS and DevOps.

🔗 GitHub: https://github.com/Jaishree97