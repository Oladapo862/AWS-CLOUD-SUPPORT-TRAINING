# Day 2 – Troubleshooting

## Issue – SignatureDoesNotMatch While Verifying AWS CLI Credentials

### Problem

After creating a new access key for my IAM user, I configured the AWS CLI profile and attempted to verify the credentials using the AWS STS GetCallerIdentity command. Instead of returning my account information, the AWS CLI returned a **SignatureDoesNotMatch** error.

---

### Cause

I assumed that only the **Secret Access Key** needed to be updated after creating a new access key. I forgot to update the **Access Key ID**, leaving the previous Access Key ID paired with the new Secret Access Key.

Since both values must belong to the same access key pair, AWS could not validate the request signature and rejected the authentication request.

---

### Resolution

I reconfigured the **dev-user** AWS CLI profile using both the new **Access Key ID** and the matching **Secret Access Key**. After updating both values, I ran the AWS STS GetCallerIdentity command again and successfully verified my identity.

---

### Lesson Learned

This troubleshooting exercise taught me that an AWS access key consists of two matching components:

* Access Key ID
* Secret Access Key

Whenever a new access key is created, both values must be updated together. Mixing credentials from different access key pairs will result in authentication errors such as **SignatureDoesNotMatch**.

It also reinforced the importance of carefully reading AWS error messages, as they often provide valuable clues that help identify the root cause of a problem.

---

# Conclusion

Although I encountered an authentication error while configuring the AWS CLI, I was able to identify the cause, correct the configuration, and successfully verify the IAM user credentials. This experience improved my understanding of AWS CLI authentication and access key management.
