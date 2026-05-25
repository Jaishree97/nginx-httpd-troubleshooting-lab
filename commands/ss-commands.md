# SS Commands

This document contains socket statistics commands used during troubleshooting.

---

# Verify Listening Ports

## Command

```bash
ss -tulnp
```

## Purpose

Displays:
- Listening TCP ports
- Listening UDP ports
- Process IDs
- Running services

Used to verify:
- NGINX on port 80
- Apache on port 83
