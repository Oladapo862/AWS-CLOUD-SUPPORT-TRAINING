# Day 1 – AWS Account Security (Hands-on)

## Overview

The goal of today's lab was to secure my AWS account by implementing AWS security best practices before deploying any cloud resources. I protected the Root User with Multi-Factor Authentication (MFA), configured billing alerts, created an IAM Administrator account, and switched from the Root User to the IAM Administrator for daily account management.

---

# Task 1 – Enable MFA on the Root User

## Objective

Protect the Root User by enabling Multi-Factor Authentication (MFA).

## What I Did

* Opened the AWS Security Credentials page.
* Selected the option to assign an MFA device.
* Chose an authenticator application.
* Completed the MFA setup process.
* Verified that MFA was successfully enabled.

## Result

The Root User is now protected with Multi-Factor Authentication.

---

# Task 2 – Configure Billing Alerts

## Objective

Configure billing notifications to monitor AWS spending.

## What I Did

* Opened the AWS Billing and Cost Management console.
* Created a new budget.
* Configured a spending threshold.
* Added an email notification.
* Saved the budget configuration.

## Result

Billing alerts were successfully configured to monitor AWS costs.

---

# Task 3 – Create an IAM Administrator Account

## Objective

Create a dedicated administrator account for daily AWS management.

## What I Did

* Opened the IAM service.
* Created a new IAM user.
* Granted Administrator permissions.
* Completed the user creation process.

## Result

The IAM Administrator account was created successfully.

---

# Task 4 – Stop Using the Root User

## Objective

Use the IAM Administrator account for daily AWS administration.

## What I Did

* Signed out of the Root User.
* Opened the IAM sign-in page.
* Logged in using the IAM Administrator account.
* Verified successful access to the AWS Management Console.

## Result

The IAM Administrator account is now used for daily administration, while the Root User is reserved for account-level tasks only.

---

# Conclusion

Today's lab established a secure AWS environment by implementing the recommended account security practices. The account is now ready for future AWS hands-on labs.
