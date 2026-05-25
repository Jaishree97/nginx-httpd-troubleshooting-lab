# NGINX + HTTPD Commands

This document contains the NGINX and Apache HTTP Server installation and configuration steps performed on the AWS EC2 instance.

---

# Install NGINX and Apache

## Command

```bash
yum install nginx httpd -y
```

## Purpose

Installs:
- NGINX web server
- Apache HTTP Server

---

# Start NGINX Service

## Command

```bash
systemctl start nginx
```

## Purpose

Starts NGINX web server.

---

# Enable NGINX Service

## Command

```bash
systemctl enable nginx
```

## Purpose

Enables NGINX service during system boot.

---

# Start Apache HTTPD Service

## Command

```bash
systemctl start httpd
```

## Purpose

Starts Apache HTTP Server.

---

# Enable Apache HTTPD Service

## Command

```bash
systemctl enable httpd
```

## Purpose

Enables Apache service during system boot.

---

# Edit Apache Configuration File

## Command

```bash
vi /etc/httpd/conf/httpd.conf
```

## Purpose

Used to modify Apache configuration settings.

---

# Change Apache Port

## Configuration

```apache
Listen 80
```

Changed to:

```apache
Listen 83
```

## Purpose

Changes Apache listening port from 80 to 83.

---

# Verify Apache Syntax

## Command

```bash
httpd -t
```

## Purpose

Checks Apache configuration syntax.

---

# Verify NGINX Syntax

## Command

```bash
nginx -t
```

## Purpose

Checks NGINX configuration syntax.

---

# Restart NGINX Service

## Command

```bash
systemctl restart nginx
```

## Purpose

Restarts NGINX after configuration changes.

---

# Restart Apache HTTPD Service

## Command

```bash
systemctl restart httpd
```

## Purpose

Restarts Apache after configuration changes.
