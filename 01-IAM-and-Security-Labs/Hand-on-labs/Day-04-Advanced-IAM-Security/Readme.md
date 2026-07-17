# Day 4 – Advanced IAM Security

## Overview

Today's lab focused on strengthening IAM security by working with AWS Security Token Service (STS), IAM roles, CloudTrail, Multi-Factor Authentication (MFA), least privilege, and IAM Access Analyzer. I also practiced assuming an IAM role from the AWS CLI using a named profile and learned how AWS trust policies and IAM permissions work together to grant temporary access.

---

# Objectives

* Generate temporary credentials using AWS STS.
* Assume an IAM role using the AWS CLI.
* Review role usage with CloudTrail.
* Enable MFA for an IAM user.
* Remove an unused IAM user.
* Apply the principle of least privilege using a custom IAM policy.
* Review IAM Access Analyzer findings.

---

# Hands-on Tasks

## Task 1 – Generate Temporary Credentials and Assume an IAM Role

### Objective

Learn how AWS Security Token Service (STS) provides temporary credentials by allowing an IAM user to assume an IAM role.

### What I Did

* Edited the trust policy of the **STS-Lab-Role** and added the ARN of my **dev-user** IAM user.
* Created an inline IAM policy for **dev-user** that granted permission to perform the `sts:AssumeRole` action on the target role.
* Verified that I was using the **dev-user** AWS CLI profile.
* Successfully assumed the IAM role using the AWS CLI and received temporary security credentials.

### Result

I successfully configured the required trust relationship and permissions, then generated temporary credentials using AWS STS.

---

## Task 2 – Audit IAM Role Usage

### Objective

Review IAM role activity using AWS CloudTrail.

### What I Did

* Opened AWS CloudTrail.
* Reviewed events related to IAM role usage.
* Verified that role activity was being recorded.

### Result

I confirmed that CloudTrail can be used to audit IAM role activity for security and compliance purposes.

---

## Task 3 – Enable MFA for an IAM User

### Objective

Improve account security by enabling Multi-Factor Authentication for an IAM user.

### What I Did

* Opened the IAM user security settings.
* Configured an MFA device.
* Verified that MFA was successfully enabled.

### Result

The IAM user now requires MFA during authentication, providing an additional layer of security.

---

## Task 4 – Remove an Unused IAM User

### Objective

Practice identity management by removing an IAM user that was no longer required.

### What I Did

* Identified an unused IAM user.
* Deleted the user from the AWS account.
* Confirmed the user was successfully removed.

### Result

The unused IAM user was permanently removed, following IAM security best practices.

---

## Task 5 – Apply the Principle of Least Privilege

### Objective

Create a custom IAM policy that grants only the permissions required to perform a specific task.

### What I Did

* Created a custom IAM policy using the JSON editor.
* Configured the policy to allow read-only access to Amazon S3 bucket information.
* Reviewed the policy after creation.

### Result

A custom least-privilege policy was successfully created, limiting access to only the required S3 actions.

---

## Task 6 – Review IAM Access Analyzer

### Objective

Use IAM Access Analyzer to identify resources that may be accessible outside the AWS account.

### What I Did

* Created an IAM Access Analyzer.
* Reviewed the findings for my AWS account.
* Confirmed that no unexpected external access findings were present.

### Result

IAM Access Analyzer was successfully configured and used to review the security posture of the account.

---

# Key Takeaways

* AWS STS provides temporary credentials that improve security compared to long-term access keys.
* Successfully assuming an IAM role requires both a trust policy on the role and permission for the IAM user to call `sts:AssumeRole`.
* CloudTrail records IAM role activity, making it valuable for auditing and troubleshooting.
* Enabling MFA strengthens IAM user security.
* Removing unused IAM users reduces unnecessary security risks.
* Applying least privilege minimizes the impact of accidental or unauthorized actions.
* IAM Access Analyzer helps identify resources that may be publicly or externally accessible.

---

# Conclusion

Today's lab expanded my understanding of advanced IAM security by focusing on temporary credentials, role assumption, auditing, identity management, and permission control. Through hands-on practice, I learned how AWS services work together to provide secure access while following security best practices such as least privilege and Multi-Factor Authentication.
