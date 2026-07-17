# Day 8 – AWS CLI Fundamentals

## Objective

The objective of this lab was to verify the AWS CLI installation, confirm my AWS identity, inspect CLI configuration profiles, and interact with Amazon EC2 using AWS CLI commands.

---

## Skills Practiced

- Verify AWS CLI installation
- Validate IAM credentials
- Inspect configured AWS CLI profiles
- Retrieve AWS account identity
- Describe EC2 instances using AWS CLI
- Interpret CLI error messages

---

## Commands Executed

### 1. Verify AWS CLI Installation

```bash
aws --version
```

Verified that AWS CLI was correctly installed and available from the command line.

---

### 2. Verify Current IAM Identity

```bash
aws sts get-caller-identity
```

Retrieved:

- UserId
- AWS Account ID
- IAM User ARN

This confirmed that the CLI was authenticated successfully.

---

### 3. View Configured Profiles

```bash
aws configure list-profiles
```

Observed two configured profiles:

- default
- dev-user

---

### 4. Describe EC2 Instances

```bash
aws ec2 describe-instances
```

Initially received the following error:

```
Could not connect to the endpoint URL
```

After retrying, the command successfully returned the EC2 instance information in JSON format, including:

- Reservation ID
- Owner ID
- Architecture
- Block Device Mapping
- Attached EBS Volume
- Instance Metadata

---

## Screenshots

Include screenshots of:

- AWS CLI Version
- get-caller-identity
- list-profiles
- Failed describe-instances command
- Successful describe-instances output

---

## Key Takeaways

During this lab I learned:

- How to verify AWS CLI installation.
- How to verify the currently authenticated IAM identity.
- How AWS CLI profiles work.
- How to retrieve EC2 information from the command line.
- How to recognize and investigate endpoint connectivity errors.

---

## Cloud Support Relevance

Cloud Support Engineers frequently use the AWS CLI to:

- Validate IAM authentication
- Troubleshoot CLI connectivity issues
- Inspect EC2 resources
- Collect infrastructure information for customers