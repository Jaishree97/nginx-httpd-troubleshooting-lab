# AWS Security Group Concepts

## What is a Security Group?

A Security Group is a virtual firewall in AWS used to control inbound and outbound traffic for EC2 instances.

---

# Security Group Rules Used

| Protocol | Port | Purpose |
|---|---|---|
| SSH | 22 | Remote access |
| HTTP | 80 | NGINX access |
| Custom TCP | 83 | Apache access |

---

# Why Port 83 Was Added

Apache HTTP Server was configured on custom port:

```text
83
```

Without allowing port 83:
- Apache webpage would not be accessible
- Browser requests would fail

---

# Advantages of Security Groups

- Traffic filtering
- Improved AWS security
- Controlled access management
- Instance-level firewall protection

---

# Practical Learning

In this lab:
- Configured Security Group rules
- Allowed HTTP traffic
- Allowed custom Apache port
- Verified browser connectivity
