# Day 6 – Linux User & Permission Management

## Overview

Today's lab focused on Linux user administration and permission management. I learned how Linux manages users and groups, how file ownership affects access, and how permissions determine what users can do with files. These are essential Linux administration skills that are commonly used when managing cloud servers.

---

# Objectives

* View existing Linux users.
* Create a new Linux user.
* Set a password for the new user.
* Create a Linux group.
* Add a user to a group.
* Change file ownership.
* Modify file permissions.

---

# Hands-on Tasks

## Task 1 – View Existing Users and Create a New User

### Objective

Learn how Linux stores user accounts and create a new local user.

### What I Did

* Viewed all user accounts stored in the `/etc/passwd` file.
* Listed only the usernames using the `cut` command.
* Created a new user named **clouduser**.
* Verified the new user's details using the `id` command.
* Assigned a password to the new user.

### Result

I successfully created a new Linux user and confirmed that the account was created correctly.

---

## Task 2 – Create a Group and Add a User

### Objective

Manage user access by creating a Linux group and assigning users to it.

### What I Did

* Created a new group named **developers**.
* Added **clouduser** to the **developers** group.
* Verified the user's group membership.

### Result

The new user became a member of the **developers** group, allowing permissions to be managed through group membership.

---

## Task 3 – Change File Ownership and Permissions

### Objective

Understand how ownership and permissions control access to files.

### What I Did

* Created a test file for the lab.
* Changed the ownership of the file from the default owner to **clouduser**.
* Verified the ownership change using `ls -l`.
* Modified the file permissions and confirmed the changes.

### Result

The file ownership and permissions were successfully updated, demonstrating how Linux controls access to files through ownership and permission settings.

---

# Key Takeaways

* Linux stores user account information in the `/etc/passwd` file.
* Users can be organized into groups to simplify permission management.
* File ownership determines who has primary control over a file.
* Permissions define who can read, write, or execute a file.
* Proper ownership and permission management are essential for maintaining secure Linux systems.

---

# Conclusion

Today's lab strengthened my understanding of Linux user and permission management. Through hands-on practice, I learned how to create users and groups, manage group membership, change file ownership, and modify file permissions. These are fundamental skills that are frequently used when administering Linux servers in cloud environments.
