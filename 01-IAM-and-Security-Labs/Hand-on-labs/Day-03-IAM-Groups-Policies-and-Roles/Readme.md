# Day 3 – IAM Groups, Policies & Roles

## Overview

Today's lab focused on managing AWS Identity and Access Management (IAM) resources by working with groups, managed policies, custom policies, and IAM roles. I learned how permissions are assigned through IAM groups, how custom policies can be created, and how IAM roles allow AWS services such as Amazon EC2 and AWS Lambda to securely access other AWS resources without using long-term credentials.

---

# Objectives

* Create IAM groups.
* Add users to IAM groups.
* Attach AWS managed policies.
* Create a custom IAM policy.
* Test IAM permissions.
* Create an EC2 IAM role with S3 permissions.
* Attach the IAM role to an EC2 instance.
* Verify EC2 access to Amazon S3.
* Create a Lambda execution role.

---

# Hands-on Tasks

## Task 1 – Create IAM Groups

### Objective

Create IAM groups to simplify permission management for multiple users.

### What I Did

* Opened the IAM service.
* Created a new IAM group.
* Configured the group for future permission assignments.

### Result

The IAM group was created successfully.

---

## Task 2 – Add Users to IAM Groups

### Objective

Assign permissions through IAM groups instead of attaching permissions directly to individual users.

### What I Did

* Selected the IAM user.
* Added the user to the newly created IAM group.
* Verified that the user became a member of the group.

### Result

The IAM user successfully inherited permissions from the group.

---

## Task 3 – Attach Managed Policies

### Objective

Grant AWS service permissions using AWS managed policies.

### What I Did

* Attached an AWS managed policy to the IAM group.
* Verified that the policy was successfully assigned.

### Result

The IAM group received the managed policy permissions.

---

## Task 4 – Create a Custom IAM Policy

### Objective

Create a custom IAM policy to better understand permission management using JSON policy documents.

### What I Did

* Opened the IAM Policy editor.
* Created a custom IAM policy.
* Reviewed and saved the policy.

### Result

The custom IAM policy was created successfully.

---

## Task 5 – Test IAM Permissions

### Objective

Verify that the assigned permissions work as expected.

### What I Did

* Logged in using the IAM user.
* Tested access to AWS services based on the assigned permissions.
* Confirmed that the expected permissions were applied.

### Result

The IAM permissions worked as expected after the correct policies were assigned.

---

## Task 6 – Create an EC2 IAM Role with S3 Permissions

### Objective

Create an IAM role that allows an EC2 instance to securely access Amazon S3.

### What I Did

* Created a new IAM role for Amazon EC2.
* Selected Amazon EC2 as the trusted AWS service.
* Attached the required Amazon S3 permissions while creating the role.
* Completed the role creation.

### Result

The EC2 IAM role was successfully created with the required S3 permissions.

---

## Task 7 – Attach the IAM Role to an EC2 Instance

### Objective

Assign the IAM role to an EC2 instance.

### What I Did

* Selected my EC2 instance.
* Attached the newly created IAM role.
* Verified that the role was successfully associated with the instance.

### Result

The EC2 instance successfully assumed the IAM role.

---

## Task 8 – Test EC2 Access to Amazon S3

### Objective

Verify that the EC2 instance could access Amazon S3 using its IAM role.

### What I Did

* Connected to the EC2 instance.
* Used the AWS CLI to access Amazon S3.
* Confirmed that the IAM role provided the required permissions without using access keys.

### Result

The EC2 instance successfully accessed Amazon S3 using its IAM role.

---

## Task 9 – Create a Lambda Execution Role

### Objective

Create an IAM role that allows AWS Lambda to interact with other AWS services securely.

### What I Did

* Created a Lambda execution role.
* Selected AWS Lambda as the trusted service.
* Attached the required execution permissions.
* Completed the role creation.

### Result

The Lambda execution role was created successfully.

---

# Key Takeaways

* IAM groups make permission management easier by assigning permissions to groups instead of individual users.
* AWS managed policies provide predefined permissions that simplify IAM administration.
* Custom IAM policies allow permissions to be tailored to specific requirements.
* IAM roles provide temporary credentials that allow AWS services to access other AWS resources securely.
* Amazon EC2 and AWS Lambda should use IAM roles instead of storing long-term access keys.
* Testing permissions after making IAM changes helps confirm that resources have the expected level of access.

---

# Conclusion

Today's lab expanded my understanding of AWS Identity and Access Management by exploring groups, policies, and roles. I successfully assigned permissions through IAM groups, created both managed and custom policies, configured IAM roles for Amazon EC2 and AWS Lambda, and verified secure access to Amazon S3 without using long-term credentials. This lab reinforced the importance of using IAM roles to provide secure and scalable access between AWS services.
