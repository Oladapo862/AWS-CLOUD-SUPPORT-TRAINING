# Troubleshooting

## Issue 1 – Unable to List S3 Buckets

### Problem

After adding my IAM user to a group and attaching an S3 managed policy, I was unable to list S3 buckets even though I expected to have full access.

### Cause

I mistakenly attached the **AmazonS3FilesFullAccess** managed policy instead of a policy that granted full bucket-level permissions. The policy did not provide the permissions required to list S3 buckets.

### Resolution

I reviewed the attached policy, identified that the wrong managed policy had been assigned, and replaced it with the appropriate S3 policy. After updating the permissions, I was able to access the required S3 resources successfully.

---

## Issue 2 – Unable to Attach a New IAM Role to an Existing EC2 Instance

### Problem

After creating a new IAM role, I attempted to attach it to an existing EC2 instance. AWS would not allow the new role to be attached because the instance already had an IAM role associated with it.

### Cause

The existing EC2 instance still had an IAM role attached. AWS requires the current IAM role association to be removed before another role can be attached.

### Resolution

I selected the EC2 instance and navigated to:

**Actions → Security → Modify IAM Role**

I changed the IAM role to **No IAM Role** and saved the changes. After removing the existing role, I repeated the process and selected the newly created IAM role. The new role was attached successfully, and the EC2 instance was able to use the updated permissions.

---

# Lessons Learned

* Always verify that the correct managed policy is attached before testing permissions.
* Similar policy names can grant different levels of access, so it is important to review the permissions included in each policy.
* An EC2 instance can only have one IAM role attached at a time.
* Before attaching a different IAM role to an EC2 instance, the existing role should be removed by selecting **No IAM Role** through the **Modify IAM Role** option.
* Understanding AWS error messages and reviewing service configurations helps identify permission-related issues more efficiently.

---

# Conclusion

The issues encountered during this lab helped reinforce my understanding of IAM policies, IAM roles, and EC2 role associations. By identifying the incorrect S3 policy and learning how to replace an IAM role on an existing EC2 instance, I gained practical troubleshooting experience that will be valuable when managing AWS identities and permissions in real-world environments.
