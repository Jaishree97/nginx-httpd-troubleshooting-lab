# Apache Troubleshooting Commands

This document contains troubleshooting steps performed during Apache HTTP Server failure.

---

# Apache Service Failure

## Error

```bash
Job for httpd.service failed
```

## Purpose

Apache service failed to start because:
- Port 80 was already used by NGINX
- SELinux blocked custom port 83

---

# Check Apache Logs

## Command

```bash
journalctl -xeu httpd
```

## Purpose

Displays detailed Apache troubleshooting logs.

---

# Verify Apache Configuration

## Command

```bash
httpd -t
```

## Purpose

Checks Apache configuration syntax.

---

# Verify Listening Ports

## Command

```bash
ss -tulnp
```

## Purpose

Verifies:
- Active listening ports
- Running services
- Port conflicts

---

# Solution Applied

- Changed Apache port to 83
- Allowed port 83 in Security Group
- Configured SELinux custom port access
- Restarted Apache service successfully
