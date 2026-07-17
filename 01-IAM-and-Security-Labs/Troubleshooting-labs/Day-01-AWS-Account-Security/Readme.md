# Day 1 – AWS Account Security (Troubleshooting)

## Issue 1 – Invalid MFA Code

### Problem

While configuring Multi-Factor Authentication (MFA), I entered an invalid authentication code from my authenticator application.

### Cause

The authentication code entered was incorrect.

### Resolution

I generated a new valid code from the authenticator application and completed the MFA setup successfully.

---

## Issue 2 – Billing Alert Threshold Not Configured

### Problem

While creating my AWS Budget, I forgot to configure the alert threshold.

### Cause

The threshold value was skipped during the budget configuration process.

### Resolution

I returned to the budget settings, configured the desired spending threshold, and verified the notification settings before saving the budget.

---

## Issue 3 – Incorrect AWS Account ID During IAM User Login

### Problem

While signing in with the IAM Administrator account, I entered an incorrect AWS Account ID.

### Cause

The wrong account identifier was entered on the IAM sign-in page.

### Resolution

I confirmed the correct AWS Account ID and signed in successfully using the correct information.

---

# Lessons Learned

* Always verify authentication codes before submitting them during MFA setup.
* Review budget settings carefully to ensure spending thresholds and notifications are configured correctly.
* Double-check the AWS Account ID before signing in as an IAM user.
* Reading AWS error messages carefully helps identify mistakes and speeds up troubleshooting.

---

# Conclusion

The issues encountered during today's lab were resolved by carefully reviewing the AWS configuration steps and error messages. These troubleshooting exercises improved my understanding of AWS account security and reinforced the importance of verifying configuration details before completing administrative tasks.
