# Day 6 – Troubleshooting

## Issue – Unable to Change File Permissions After Changing Ownership

### Problem

After changing the ownership of `project.txt` to **clouduser**, I attempted to modify the file permissions while logged in as **ec2-user**. The command failed with the following error:

```text
chmod: changing permissions of 'project.txt': Operation not permitted
```

### Cause

I had already transferred ownership of the file to **clouduser** using the `chown` command. Since I was still logged in as **ec2-user**, I was no longer the owner of the file. In Linux, only the file owner or a user with administrative privileges can change a file's permissions.

### Resolution

I used `sudo` to run the `chmod` command with administrative privileges. This allowed the permission change to complete successfully even though the file was owned by another user.

### Lesson Learned

* Changing file ownership affects who can manage a file.
* The `chown` command changes the owner of a file, while `chmod` changes its permissions.
* After transferring ownership, the original user may lose the ability to modify permissions unless they use `sudo` or regain ownership.
* Always verify file ownership with `ls -l` before troubleshooting permission-related errors.

---

# Conclusion

This troubleshooting exercise helped me better understand the relationship between file ownership and permissions in Linux. By identifying that the file owner had changed, I was able to use the appropriate administrative privileges to modify the file permissions successfully.
