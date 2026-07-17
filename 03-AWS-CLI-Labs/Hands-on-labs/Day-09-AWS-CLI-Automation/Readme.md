# Day 9 – Amazon S3 Using AWS CLI

## Objective

The objective of this lab was to manage Amazon S3 resources using AWS CLI by creating buckets, uploading files, listing bucket contents, and retrieving bucket information.

---

## Skills Practiced

- Verify configured AWS Region
- Create Amazon S3 buckets
- Upload files to S3
- List S3 buckets
- List objects inside a bucket
- Retrieve bucket information using JSON output

---

## Commands Executed

### 1. Verify Configured Region

```bash
aws configure get region
```

Confirmed the configured region.

---

### 2. Attempt Bucket Creation

```bash
aws s3 mb s3://linux-lab
```

Received an endpoint connection error.

Retried using another bucket name.

---

### 3. List Existing Buckets

```bash
aws s3 ls
```

Verified the existing buckets within the account.

---

### 4. View Current CLI Configuration

```bash
aws configure list
```

Verified:

- Access Key
- Secret Key
- Region

---

### 5. Create Bucket

```bash
aws s3api create-bucket --bucket cyberratel-lab147 --region us-east-1
```

Bucket creation completed successfully.

---

### 6. Create Local Test File

```cmd
echo AWS CLI S3 Automation Lab > testfile.txt
```

---

### 7. Upload File

```bash
aws s3 cp testfile.txt s3://cyberratel-lab147/
```

Successfully uploaded the file.

---

### 8. Verify Uploaded Object

```bash
aws s3 ls s3://cyberratel-lab147/
```

Confirmed that the uploaded file existed inside the bucket.

---

### 9. List Buckets Using JSON

```bash
aws s3api list-buckets --output json
```

Retrieved bucket information in JSON format.

---

## Screenshots

Include screenshots of:

- aws configure get region
- Failed bucket creation
- aws s3 ls
- Successful bucket creation
- Uploading file
- Listing bucket contents
- list-buckets JSON output

---

## Key Takeaways

During this lab I learned:

- The difference between `aws s3` and `aws s3api`.
- How to create S3 buckets.
- How to upload files using AWS CLI.
- How to verify uploaded objects.
- How to retrieve bucket information in JSON format.
- How endpoint errors can affect S3 operations.

---

## Cloud Support Relevance

AWS Cloud Support Engineers regularly use these commands to:

- Validate customer bucket creation
- Upload diagnostic files
- Verify bucket contents
- Troubleshoot AWS CLI connectivity