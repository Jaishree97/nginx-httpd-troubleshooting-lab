# NGINX + HTTPD Troubleshooting Lab - Project Flow

# 📌 Project Workflow

This document explains the complete implementation flow of the NGINX + HTTPD Troubleshooting Lab project.

---

# Step 1 — Launch EC2 Instance

Created a Red Hat Linux EC2 instance in AWS.

### Configuration

- Instance Type: t3.micro
- Region: us-east-2 (Ohio)
- Operating System: Red Hat Enterprise Linux
- Default VPC used

---

# Step 2 — Configure Security Groups

Created security group rules to allow:

| Port | Protocol | Purpose |
|------|-----------|----------|
| 22 | SSH | Remote access |
| 80 | HTTP | NGINX access |
| 83 | Custom TCP | Apache access |

---

# Step 3 — Connect EC2 via SSH

Connected to the server using PEM key authentication.

```bash
ssh -i "key.pem" ec2-user@PUBLIC-IP
```

Switched to root user:

```bash
sudo su
```

Successfully logged into the Linux server.

---

# Step 4 — Install NGINX & Apache

Installed required web server packages.

```bash
yum install nginx httpd -y
```

Successfully installed:
- NGINX
- Apache HTTP Server

---

# Step 5 — Start NGINX Service

Started and enabled nginx service.

```bash
systemctl start nginx
systemctl enable nginx
```

Verified nginx service:

```bash
systemctl status nginx
```

---

# Step 6 — Configure NGINX Web Page

Edited nginx default web page.

```bash
vi /usr/share/nginx/html/index.html
```

Added custom content:

```html
<h1>nginx</h1>
```

Saved configuration successfully.

---

# Step 7 — Configure Apache HTTPD

Edited Apache configuration file.

```bash
vi /etc/httpd/conf/httpd.conf
```

Modified Apache listening port:

```apache
Listen 80
```

Changed to:

```apache
Listen 83
```

This was required because nginx was already using port 80.

---

# Step 8 — Verify Apache Configuration

Validated Apache configuration syntax.

```bash
httpd -t
```

Output:

```text
Syntax OK
```

---

# Step 9 — Configure Apache Web Page

Edited Apache default web page.

```bash
vi /var/www/html/index.html
```

Added custom content:

```html
<h1>apache</h1>
```

Saved configuration successfully.

---

# Step 10 — Restart Services

Restarted web server services.

```bash
systemctl restart nginx
systemctl restart httpd
```

Initially Apache failed to start.

---

# Step 11 — Troubleshoot Apache Failure

Verified Apache service status.

```bash
systemctl status httpd
```

Observed service startup failure.

Checked detailed logs:

```bash
journalctl -xeu httpd
```

Identified:
- Port conflict
- SELinux restriction issue

---

# Step 12 — Validate Listening Ports

Checked active listening ports.

```bash
ss -tulnp
```

Verified:
- nginx running on port 80
- Apache expected on port 83

---

# Step 13 — SELinux Troubleshooting

Temporarily disabled SELinux enforcement.

```bash
setenforce 0
```

Restarted Apache service.

```bash
systemctl restart httpd
```

Apache started successfully.

---

# Step 14 — Configure Permanent SELinux Rule

Installed SELinux management utilities.

```bash
yum install policycoreutils-python-utils -y
```

Allowed Apache to use custom port 83 permanently.

```bash
semanage port -a -t http_port_t -p tcp 83
```

Verified allowed HTTP ports.

```bash
semanage port -l | grep http
```

---

# Step 15 — Validate Services

Verified nginx service:

```bash
systemctl status nginx
```

Verified Apache service:

```bash
systemctl status httpd
```

Both services successfully running.

---

# Step 16 — Validate Browser Access

Verified nginx browser access:

```text
http://PUBLIC-IP
```

Output:

```text
nginx
```

---

Verified Apache browser access:

```text
http://PUBLIC-IP:83
```

Output:

```text
apache
```

---

# Step 17 — Validate Networking

Verified active listening ports again.

```bash
ss -tulnp
```

Confirmed:

| Service | Port |
|---|---|
| nginx | 80 |
| httpd | 83 |

---

# 📚 Skills Practiced

- AWS EC2
- Linux Administration
- NGINX Configuration
- Apache HTTP Server
- SELinux Troubleshooting
- Security Groups
- Linux Networking
- Port Management
- Service Troubleshooting
- SSH Connectivity
- Git & GitHub Documentation

---

# ✅ Project Outcome

Successfully implemented and validated:

- NGINX web server on port 80
- Apache HTTP Server on port 83
- SELinux troubleshooting
- Port conflict troubleshooting
- Linux networking validation
- AWS Security Group configuration
- Multi-service web hosting on a single EC2 instance

This project improved practical understanding of Linux troubleshooting, web server administration, AWS networking, and DevOps troubleshooting workflows.