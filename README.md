# NGINX + HTTPD Troubleshooting Lab

## Objective

Configure:
- nginx on port 80
- Apache/httpd on port 83

Perform troubleshooting using:
- systemctl
- journalctl
- ss
- semanage
- SELinux

---

# Architecture

| Service | Port |
|---|---|
| nginx | 80 |
| Apache | 83 |

---

# Commands Used

```bash
systemctl status httpd
journalctl -xeu httpd
ss -tulnp
httpd -t
setenforce 0
```

---

# Troubleshooting Performed

- Port conflict troubleshooting
- SELinux troubleshooting
- Security Group troubleshooting
- Apache startup troubleshooting

---

# Verification

## NGINX

http://PUBLIC-IP

## APACHE

http://PUBLIC-IP:83

---

# Learning Outcome

- Linux troubleshooting
- Web server configuration
- AWS Security Groups
- SELinux troubleshooting
- Service troubleshooting