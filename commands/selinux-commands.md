# SELinux Commands

This document contains SELinux troubleshooting commands used during the lab.

---

# Disable SELinux Temporarily

## Command

```bash
setenforce 0
```

## Purpose

Temporarily disables SELinux enforcement for troubleshooting.

---

# Install SELinux Utilities

## Command

```bash
yum install policycoreutils-python-utils -y
```

## Purpose

Installs SELinux management utilities.

---

# Allow Apache on Port 83

## Command

```bash
semanage port -a -t http_port_t -p tcp 83
```

## Purpose

Allows Apache HTTP Server to use custom TCP port 83.
