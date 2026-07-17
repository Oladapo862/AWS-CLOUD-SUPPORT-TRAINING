# Day 2 – IAM Users & Access Keys

## Overview

Today's lab focused on managing IAM users and securing programmatic access to AWS. I created a new IAM user with console access, logged in using the new account, generated access keys for AWS CLI authentication, configured a named CLI profile, and rotated the access keys following AWS security best practices.

---

# Objectives

* Create an IAM user with console access.
* Sign in as the new IAM user.
* Generate access keys for programmatic access.
* Configure the AWS CLI using a named profile.
* Rotate access keys to improve security.

---

# Hands-on Tasks

## Task 1 – Create an IAM User with Console Access

### Objective

Create a dedicated IAM user that can access the AWS Management Console.

### What I Did

* Created a new IAM user named **dev-user**.
* Enabled AWS Management Console access during user creation.
* Assigned a temporary password.
* Completed the user creation process.

### Result

The IAM user was successfully created with console access.

---

## Task 2 – First Console Login

### Objective

Sign in using the newly created IAM user.

### What I Did

* Logged in using the IAM user credentials.
* Changed the temporary password when prompted.
* Successfully accessed the AWS Management Console.

### Result

The IAM user account was activated and ready for daily use.

---

## Task 3 – Create Access Keys

### Objective

Generate access keys for AWS CLI authentication.

### What I Did

* Navigated to the Security Credentials section for the IAM user.
* Created a new access key for AWS CLI usage.
* Stored the access key securely.

### Result

A new access key pair was successfully generated for the IAM user.

---

## Task 4 – Configure AWS CLI

### Objective

Configure the AWS CLI to use the IAM user's credentials.

### What I Did

* Configured a named AWS CLI profile called **dev-user**.
* Entered the Access Key ID and Secret Access Key.
* Configured the default region and output format.
* Verified the configuration using the AWS STS GetCallerIdentity command.

### Result

The AWS CLI was successfully configured and authenticated using the **dev-user** profile.

---

## Task 5 – Rotate Access Keys

### Objective

Practice rotating IAM access keys following AWS security best practices.

### What I Did

* Created a new access key.
* Updated the AWS CLI profile with the new credentials.
* Verified the new credentials were working correctly.
* Deactivated the old access key.
* Deleted the old access key after confirming the new key was functioning properly.

### Result

The old access key was successfully replaced with a new one without affecting future AWS CLI access.

---

# Key Takeaways

* IAM users should be used instead of the Root User for everyday AWS administration.
* Console access and programmatic access are configured separately for IAM users.
* AWS CLI profiles make it easy to manage multiple AWS identities on the same computer.
* Access keys should be rotated regularly to improve account security.
* Verifying credentials before deleting old access keys helps prevent authentication issues.

---

# Conclusion

Today's lab strengthened my understanding of IAM user management and AWS CLI authentication. I successfully created a new IAM user, configured console and CLI access, and practiced rotating access keys while following AWS security best practices.
