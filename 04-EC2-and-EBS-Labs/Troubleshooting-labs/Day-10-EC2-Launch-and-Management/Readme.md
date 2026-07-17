# Troubleshooting EC2 SSH Access Using Security Groups

## Issue

After modifying the EC2 Security Group, SSH access to the instance failed.

---

## Error Observed

```
ssh: connect to host <public-ip> port 22: Connection timed out
```

---

## Investigation

### Step 1 — Confirm EC2 Instance Status

Verified that the EC2 instance was running.

Result:

- Instance was healthy and running.

---

### Step 2 — Review Security Group

Navigated to:

```
EC2 → Security Groups → Inbound Rules
```

Observed that the SSH inbound rule had been removed.

---

### Root Cause

The Security Group was no longer allowing inbound TCP traffic on port 22.

Since Security Groups act as virtual firewalls, all SSH traffic was blocked before reaching the EC2 instance.

---

## Resolution

Edited the Security Group and added a new inbound rule:

- Type: SSH
- Protocol: TCP
- Port: 22
- Source: My IP

Saved the changes.

---

## Verification

Attempted to connect using SSH again.

Result:

- Connection succeeded.
- EC2 instance became accessible over SSH.

---

## Lesson Learned

A running EC2 instance can still be unreachable if its Security Group blocks the required inbound traffic.

When troubleshooting SSH connectivity, one of the first checks should always be the Security Group inbound rules.