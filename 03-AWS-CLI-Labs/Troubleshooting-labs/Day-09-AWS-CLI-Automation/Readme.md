# Day 9 – Troubleshooting AWS CLI Authentication

## Scenario

### Problem

While attempting to access Amazon S3 using the AWS CLI, the following command failed:

```bash
aws s3 ls
```

The AWS CLI returned:

```
Unable to locate credentials.
You can configure credentials by running "aws login".
```

---

## Investigation

To determine the cause of the error, I inspected the current AWS CLI configuration.

```bash
aws configure list
```

Output:

```
profile    : <not set>
access_key : <not set>
secret_key : <not set>
region     : eu-north-1
```

From the output, I confirmed that:

- No AWS CLI profile was configured.
- No Access Key was configured.
- No Secret Access Key was configured.
- The Region was detected automatically from the EC2 Instance Metadata Service (IMDS).

Since the AWS CLI had no credentials available, it could not authenticate requests to AWS services.

---

## Root Cause

The AWS CLI was not configured with valid AWS credentials.

Without an Access Key ID and Secret Access Key, authenticated AWS CLI commands cannot communicate with AWS services.

---

## Resolution

Configured the AWS CLI with valid credentials.

```bash
aws configure
```

After providing:

- AWS Access Key ID
- AWS Secret Access Key
- Default Region
- Output Format

the AWS CLI was able to authenticate successfully.

---

## Verification

After configuring the credentials, rerunning the AWS CLI commands completed successfully without the authentication error.

---

## Lessons Learned

This troubleshooting exercise reinforced the importance of verifying AWS CLI configuration before assuming there is an IAM permission or service issue.

Useful commands for diagnosing AWS CLI authentication problems:

```bash
aws configure list
```

```bash
aws sts get-caller-identity
```

These commands quickly confirm whether valid credentials are available and whether the CLI is authenticated correctly.

---

## Evidence

**Screenshot:**

`day8-troubleshooting-unable-to-locate-credentials.png`