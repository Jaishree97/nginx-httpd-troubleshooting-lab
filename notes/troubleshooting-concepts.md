# Linux Troubleshooting Concepts

## What is Troubleshooting?

Troubleshooting is the process of identifying, analyzing, and resolving system issues.

---

# Issues Faced in Lab

- Apache service failure
- Port conflict
- SELinux restriction
- Browser access issue

---

# Root Cause Analysis

## Port Conflict

NGINX was already using:

```text
80
```

Apache could not start on the same port.

---

## SELinux Restriction

SELinux blocked Apache from using custom port:

```text
83
```

---

# Troubleshooting Workflow

1. Verified service status
2. Checked service logs
3. Verified listening ports
4. Identified SELinux issue
5. Configured custom port access
6. Restarted services

---

# Practical Learning

In this lab:
- Performed Linux troubleshooting
- Analyzed Apache logs
- Verified port conflicts
- Resolved SELinux restrictions
- Validated successful service access
