# Day 4 – Troubleshooting

## Issue – Incorrect AWS CLI Command Format in Windows Command Prompt

### Problem

While attempting to assume an IAM role using the AWS CLI, the command failed immediately and Windows displayed the following error:

```text
'--profile' is not recognized as an internal or external command,
operable program or batch file.
```

---

### Cause

I copied a command that was written using Linux/macOS syntax with line continuation characters. Since I was using **Windows Command Prompt (CMD)**, the command was interpreted incorrectly and `--profile` was treated as a separate command instead of part of the AWS CLI command.

---

### Resolution

I rewrote the command as a single line using the correct Windows CMD syntax:

```bash
aws sts assume-role --role-arn arn:aws:iam::274703560323:role/STS-Lab-Role --role-session-name day4-lab --profile dev-user
```

The command executed successfully and AWS STS returned temporary security credentials for the assumed role.

---

## Lesson Learned

* AWS CLI commands may differ slightly between operating systems.
* Linux and macOS commonly use line continuation characters that are not supported in Windows Command Prompt.
* When using Windows CMD, multi-line AWS CLI commands should be entered as a single command unless using PowerShell with the appropriate syntax.
* Reading the error message carefully helped identify that the issue was related to the command format rather than IAM permissions.

---

## Conclusion

The issue was resolved by using the correct command syntax for Windows Command Prompt. After correcting the command, I successfully assumed the IAM role and generated temporary credentials using AWS Security Token Service (STS).
