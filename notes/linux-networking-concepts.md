# Linux Networking Concepts

## What is Linux Networking?

Linux networking manages communication between services, ports, and systems.

---

# Networking Command Used

```text
ss -tulnp
```

Used to verify:
- Listening ports
- Running services
- Active network sockets

---

# Ports Used in Lab

| Port | Purpose |
|---|---|
| 22 | SSH Access |
| 80 | NGINX Web Server |
| 83 | Apache HTTP Server |

---

# Port Conflict

Two services cannot use the same port simultaneously.

In this lab:
- NGINX was already using port 80
- Apache was moved to port 83

---

# Practical Learning

In this lab:
- Verified active listening ports
- Identified port conflicts
- Tested network accessibility
- Validated web server communication
