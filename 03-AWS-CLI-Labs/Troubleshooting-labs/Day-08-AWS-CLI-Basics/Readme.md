# Day 8 – Troubleshooting AWS CLI EC2 Endpoint Connectivity

## Scenario

While retrieving Amazon EC2 instance information using the AWS CLI, the request failed because the CLI could not connect to the EC2 service endpoint.

---

## Problem

Command executed:

```bash
aws ec2 describe-instances
```

Error received:

```text
Could not connect to the endpoint URL:
"https://ec2.us-east-1.amazonaws.com/"
```

---

## Investigation

To determine the cause of the issue, I performed several verification steps.

### 1. Verified AWS Identity

```bash
aws sts get-caller-identity
```

The command successfully returned my AWS account information, confirming that my IAM credentials were valid.

---

### 2. Verified Available AWS CLI Profiles

```bash
aws configure list-profiles
```

The configured CLI profiles were successfully displayed, confirming that the expected AWS CLI profiles were available.

---

### 3. Retried the EC2 Command

```bash
aws ec2 describe-instances
```

The command completed successfully and returned the EC2 instance information in JSON format.

---

## Root Cause

The issue was caused by a temporary endpoint connectivity problem rather than invalid IAM credentials or missing AWS CLI profiles.

---

## Resolution

After confirming that authentication and CLI configuration were correct, I retried the command. The AWS CLI successfully connected to the EC2 endpoint and returned the requested instance information.

---

## Verification

The successful response included EC2 instance details such as:

- Reservation ID
- Instance ID
- Availability Zone
- Instance State
- Block Device Mapping
- Network Interfaces

This confirmed that connectivity to the EC2 endpoint had been restored.

---

## Lessons Learned

This troubleshooting exercise reinforced the importance of verifying authentication and AWS CLI configuration before assuming an IAM permission issue.

Useful diagnostic commands include:

```bash
aws sts get-caller-identity
```

```bash
aws configure list-profiles
```

These commands help confirm that the AWS CLI is authenticated correctly before investigating endpoint connectivity or service availability.

---

## Evidence

### Troubleshooting Workflow

`day8-troubleshooting-ec2-endpoint-connectivity.png`

The screenshot captures the complete troubleshooting process, including:

- Initial endpoint connectivity error
- Verification of AWS identity
- Verification of configured AWS CLI profiles
- Successful execution of the EC2 describe command after retrying

---

## Cloud Support Relevance

Endpoint connectivity issues are common when working with the AWS CLI. This exercise demonstrates a structured troubleshooting approach by validating authentication, checking CLI configuration, and confirming successful communication with the AWS service after the issue was resolved.