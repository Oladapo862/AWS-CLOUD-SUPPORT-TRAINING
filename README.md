# 🚀 AWS Cloud Engineer Learning Journey

## Overview

Welcome to the **AWS Cloud Engineer Learning Journey**.

This repository is designed to help you learn AWS and Cloud Engineering by building a **single production-ready application** from scratch instead of learning AWS services in isolation.

Throughout this journey, every technology you learn is immediately applied to the same project:

> **Employee Management System**

By the end of the roadmap, you will have built, deployed, monitored, secured, automated, and continuously delivered a production-grade application using modern AWS services and DevOps practices.

---

# Learning Philosophy

This roadmap follows one simple principle:

> **Learn → Practice → Build → Troubleshoot**

Every phase introduces a new technology.

For each technology, you will:

1. Learn the concepts.
2. Perform hands-on exercises.
3. Integrate that technology into the Employee Management System.
4. Practice real production troubleshooting scenarios.

Rather than creating many unrelated mini-projects, you continuously improve **one application** until it becomes production ready.

---

# The Project

Throughout this roadmap, you will build a complete **Employee Management System**.

As the project grows, new AWS services and DevOps tools will be integrated into it.

The application will eventually include:

* Employee registration
* Employee listing
* Employee profile images
* MySQL database
* Secure file uploads
* HTTPS
* High availability
* Auto Scaling
* Monitoring
* Logging
* Notifications
* Infrastructure as Code
* Automated deployments

By the final phase, the application will be running in a production-style AWS environment.

---

# Learning Order

The roadmap follows the same order a real production environment is built.

1. Linux Fundamentals
2. Git & GitHub (used throughout the journey)
3. Amazon EC2
4. Amazon EBS
5. Nginx
6. Python & Virtual Environment
7. Flask
8. Running Flask
9. Gunicorn
10. Reverse Proxy with Nginx
11. Amazon RDS
12. Amazon S3
13. IAM Roles
14. CloudWatch
15. AWS Systems Manager (SSM)
16. CloudWatch Alarms
17. Amazon SNS
18. CloudTrail
19. VPC, Networking & Security
20. Application Load Balancer
21. Target Group
22. Amazon Route 53
23. AWS Certificate Manager (ACM)
24. Auto Scaling Group
25. Docker
26. Amazon ECS
27. AWS Lambda
28. Terraform
29. CI/CD with GitHub Actions

Each phase builds on everything completed before it.

Nothing is learned without being applied to the project.

---

# Repository Structure

The repository is organized into learning phases.

Each phase represents one technology.

Example:

```text
01-linux-fundamentals/

02-ec2/

03-ebs/

04-nginx/

05-python/

...

29-ci-cd/
```

Every phase contains two main folders.

```text
01-linux-fundamentals/

├── hands-on/

└── troubleshooting/
```

---

# Hands-on Folder

The **hands-on** folder contains everything required to learn and practice the technology.

Examples include:

* Step-by-step labs
* Commands
* Configuration files
* Practice exercises
* Sample code
* Deployment instructions
* Mini challenges

The goal of the hands-on folder is to master the technology before integrating it into the project.

---

# Troubleshooting Folder

The **troubleshooting** folder contains real production incident scenarios.

Each technology includes multiple production-style troubleshooting exercises using a structured incident playbook.

Example format:

| Production Layer | Customer Complaint | Information to Gather | Check First | Check Next | Deep Investigation | Possible Root Causes | Resolution | Validate | Escalate If |
| ---------------- | ------------------ | --------------------- | ----------- | ---------- | ------------------ | -------------------- | ---------- | -------- | ----------- |

These scenarios simulate the types of incidents handled by Cloud Support Engineers, Site Reliability Engineers (SREs), and DevOps Engineers in production environments.

---

# Learning Format

Every phase follows the exact same structure.

## Goal

Understand what the technology is used for.

---

## Hands-on

Learn and practice the technology.

Example:

* Install
* Configure
* Test
* Verify
* Practice commands
* Explore features

---

## Build

Immediately integrate that technology into the Employee Management System.

Examples:

* Deploy the application
* Add a database
* Store images
* Enable HTTPS
* Configure monitoring
* Deploy containers
* Automate infrastructure

The project evolves after every phase.

---

## Troubleshoot

Practice solving real production incidents.

Examples:

* Website unavailable
* High CPU
* Access denied
* Database connection failure
* Docker container crash
* ECS deployment failure
* DNS issues
* SSL certificate problems

The objective is not only to build the application but also to understand how to diagnose and resolve issues when things go wrong.

---

## Checkpoint

Every phase ends with a checkpoint to confirm mastery before moving to the next technology.

---

# Continuous Git Workflow

Git and GitHub are used throughout the entire project.

After every completed task:

1. Check repository status.
2. Review changes.
3. Commit with a meaningful message.
4. Push to GitHub.
5. Update project documentation.
6. Continue building.

By the final phase, GitHub also powers the CI/CD pipeline.

---

# Final Production Architecture

By the end of the roadmap, the Employee Management System will include:

* Linux Administration
* Git & GitHub
* Amazon EC2
* Amazon EBS
* Nginx
* Python
* Flask
* Gunicorn
* Amazon RDS
* Amazon S3
* IAM Roles
* CloudWatch
* CloudWatch Alarms
* Amazon SNS
* CloudTrail
* AWS Systems Manager (SSM)
* Custom VPC
* Security Groups
* Network ACLs
* Application Load Balancer
* Target Group
* Route 53
* AWS Certificate Manager (HTTPS)
* Auto Scaling Group
* Docker
* Amazon ECS
* AWS Lambda
* Terraform
* GitHub Actions CI/CD

Everything is connected into a single production-ready application.

---

# Goal of This Repository

This repository is more than a collection of AWS labs.

It is a complete, project-based learning journey that combines:

* Cloud Engineering
* Linux Administration
* AWS
* DevOps
* Infrastructure as Code
* Monitoring
* Security
* Automation
* Production Troubleshooting

By completing every phase, you will have built a production-style Employee Management System while developing the practical skills used by Cloud Engineers, Cloud Support Engineers, DevOps Engineers, and Site Reliability Engineers.
