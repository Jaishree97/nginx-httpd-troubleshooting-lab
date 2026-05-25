# SELinux Concepts

## What is SELinux?

SELinux (Security-Enhanced Linux) is a Linux security module used to enforce access control policies.

It improves Linux system security by restricting unauthorized access.

---

# SELinux Modes

| Mode | Description |
|---|---|
| Enforcing | SELinux actively blocks violations |
| Permissive | Violations are logged only |
| Disabled | SELinux disabled completely |

---

# Why SELinux Blocked Apache

Apache was configured on custom port:

```text
83
```

SELinux allows HTTP services only on default ports:
- 80
- 443

Therefore Apache was blocked until custom port access was configured.

---

# Advantages of SELinux

- Improved Linux security
- Access control enforcement
- Protection against unauthorized access
- Service isolation

---

# Practical Learning

In this lab:
- Identified SELinux issue
- Disabled SELinux temporarily
- Allowed Apache on custom port 83
- Verified Apache startup successfully
