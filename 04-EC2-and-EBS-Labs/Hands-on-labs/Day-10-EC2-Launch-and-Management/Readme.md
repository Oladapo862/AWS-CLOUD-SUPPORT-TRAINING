# EC2 Security Group SSH Access Control

## Objective

Practice managing EC2 Security Group inbound rules by blocking and restoring SSH access to an EC2 instance.

---

## Services Used

- Amazon EC2
- Amazon VPC
- Security Groups

---

## Tasks Performed

### 1. Located the EC2 Security Group

Navigated to:

```
EC2 → Instances → Select EC2 Instance → Security → Security Groups
```

Identified the Security Group attached to the EC2 instance.

---

### 2. Verified Existing SSH Rule

Opened:

```
Inbound Rules
```

Confirmed an existing SSH rule allowing inbound traffic on TCP port 22 from my public IP.

---

### 3. Blocked SSH Access

Edited the inbound rules and removed the SSH rule.

Saved the Security Group configuration.

Result:

- SSH traffic on port 22 was blocked.
- New SSH connections to the instance were no longer allowed.

---

### 4. Tested SSH Connectivity

Attempted to connect to the EC2 instance using SSH.

Confirmed that the connection failed after removing the SSH rule.

---

### 5. Restored SSH Access

Edited the Security Group inbound rules.

Added a new rule:

- Type: SSH
- Protocol: TCP
- Port: 22
- Source: My IP

Saved the changes.

---

### 6. Verified SSH Access

Attempted to connect to the EC2 instance again.

Confirmed that SSH access was successfully restored.

---

## Outcome

Successfully practiced controlling EC2 access by modifying Security Group inbound rules and verified how Security Groups directly affect SSH connectivity.

---

## Screenshots

| Screenshot | Description |
|------------|-------------|
| 01-ec2-security-group-ssh-rule-before-change.png | SSH rule configured before modification |
| 02-ec2-security-group-ssh-rule-removed-blocked.png | SSH rule removed from Security Group |
| 03-ec2-ssh-connection-failed-after-block.png | SSH connection failed after removing the rule |
| 04-ec2-security-group-ssh-rule-restored.png | SSH rule added back to the Security Group |
| 05-ec2-ssh-access-restored-successfully.png | Successful SSH connection after restoring access |