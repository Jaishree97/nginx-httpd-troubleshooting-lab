# Journalctl Commands

This document contains Linux log troubleshooting commands.

---

# View Apache Logs

## Command

```bash
journalctl -xeu httpd
```

## Purpose

Displays detailed Apache HTTP Server logs.

Used for:
- Service failure troubleshooting
- Port conflict errors
- SELinux errors

---

# View NGINX Logs

## Command

```bash
journalctl -xeu nginx
```

## Purpose

Displays NGINX service logs and troubleshooting information.
