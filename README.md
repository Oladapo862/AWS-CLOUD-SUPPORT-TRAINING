# 🚀 AWS Cloud Support Engineer Production Project

> **End-to-end deployment of a production-style Flask web application on AWS using core cloud infrastructure, containerization, orchestration, automation, monitoring, logging, and Infrastructure as Code.**

---

## 📖 Project Overview

This project documents my end-to-end implementation of a production-style cloud environment by deploying a simple HTML website served by a Flask application on AWS. Rather than focusing only on application development, the primary objective was to demonstrate practical Cloud Support Engineer skills by designing, deploying, troubleshooting, monitoring, and automating a complete cloud infrastructure similar to what is used in production environments.

The project began with building a secure network architecture using Amazon VPC and gradually progressed through compute, storage, containerization, orchestration, networking, monitoring, automation, and Infrastructure as Code. At every stage, I validated the deployment, documented my configuration, and resolved issues encountered during implementation to simulate the responsibilities of a Cloud Support Engineer.

---

# Architecture

```
Users
   │
Route 53
   │
Application Load Balancer
   │
Target Group
   │
Amazon ECS Service
   │
Docker Container
   │
Flask Application
   │
Amazon ECR
   │
CI/CD Pipeline
   │
GitHub
   │
CloudWatch
   │
SNS Notifications
   │
CloudTrail Logs
```

Infrastructure was provisioned inside a custom VPC with public and private subnets, secured with Security Groups, Route Tables, and Network ACLs.

---

# Technologies Used

* AWS VPC
* Amazon EC2
* AWS Systems Manager (SSM)
* Amazon EBS
* Amazon EFS
* Amazon S3
* Docker
* Python Flask
* Git
* GitHub
* Amazon ECR
* Amazon ECS
* Target Groups
* Application Load Balancer
* Route 53
* Auto Scaling
* CI/CD
* Amazon CloudWatch
* Amazon SNS
* AWS CloudTrail
* Amazon RDS
* Terraform
* Linux
* AWS CLI

---

# Project Implementation

## 1. VPC

I created a custom VPC instead of using the default AWS network. Public and private subnets were configured with dedicated route tables, an Internet Gateway, and a NAT Gateway to provide secure communication between internet-facing resources and backend services. Security Groups and Network ACLs were configured to control inbound and outbound traffic while validating connectivity between all network components.

**Troubleshooting:** Route table misconfigurations, incorrect CIDR blocks, internet connectivity issues, Security Group rules, NAT Gateway routing, and Network ACL conflicts.

---

## 2. EC2 (SSH & SSM)

I launched Amazon EC2 instances to host the application and perform administration tasks. Secure Shell (SSH) and AWS Systems Manager Session Manager were configured to enable secure remote access without exposing unnecessary ports. IAM roles were attached to allow Systems Manager communication.

**Troubleshooting:** SSH failures, missing key pairs, SSM agent connectivity issues, IAM permission errors, security group restrictions, and instance reachability.

---

## 3. Storage (EBS, EFS & S3)

Persistent storage was implemented using Amazon EBS volumes attached to EC2 instances. Amazon EFS was configured for shared file storage, while Amazon S3 was used to store application assets, backups, and deployment artifacts with versioning enabled.

**Troubleshooting:** Mount failures, storage permission errors, bucket policies, incorrect filesystem configuration, and disk utilization issues.

---

## 4. Docker on EC2

Docker was installed and configured on EC2 to containerize the application. Images were created, containers were managed, networking was configured, and persistent volumes were tested to ensure application consistency.

**Troubleshooting:** Container crashes, Docker daemon failures, port conflicts, missing images, and volume mapping issues.

---

## 5. Flask Application

A lightweight Flask application serving a simple HTML website was developed and deployed inside Docker containers. Environment variables were configured and the application was tested locally before deployment to AWS.

**Troubleshooting:** Dependency conflicts, incorrect application ports, Flask startup errors, Python package issues, and container runtime failures.

---

## 6. Git

Git was used for version control throughout the project. Feature branches, commits, merges, and repository history were maintained to track project progress and support collaborative development practices.

**Troubleshooting:** Merge conflicts, accidental commits, branch synchronization, and repository recovery.

---

## 7. GitHub

The project was hosted on GitHub with a structured repository, documentation, and version history. GitHub served as the central source code repository for the CI/CD pipeline.

**Troubleshooting:** Authentication failures, repository permissions, remote configuration issues, and push conflicts.

---

## 8. Docker Build

Production-ready Docker images were built using optimized Dockerfiles. Images were tested locally before deployment and unnecessary layers were removed to reduce image size.

**Troubleshooting:** Build failures, missing dependencies, Docker cache issues, incorrect working directories, and startup command errors.

---

## 9. Amazon ECR

Docker images were securely stored in Amazon Elastic Container Registry (ECR). Authentication, repository management, image tagging, and version control were implemented to support deployments.

**Troubleshooting:** Authentication failures, image push errors, repository permissions, and image version mismatches.

---

## 10. Amazon ECS

Amazon Elastic Container Service (ECS) was used to orchestrate container deployment. Task Definitions, Services, and Cluster configurations were created to ensure application availability and scalability.

**Troubleshooting:** Task failures, unhealthy containers, insufficient resources, deployment failures, and IAM permission issues.

---

## 11. Target Group

A Target Group was configured to register ECS tasks and perform continuous health checks. This ensured only healthy application instances received traffic.

**Troubleshooting:** Failed health checks, incorrect ports, unhealthy targets, and networking configuration errors.

---

## 12. Application Load Balancer

An Application Load Balancer (ALB) was deployed to distribute incoming traffic across ECS tasks. Listener rules and routing behavior were configured to improve availability.

**Troubleshooting:** HTTP 502/503 errors, listener configuration, backend communication failures, SSL issues, and target registration problems.

---

## 13. Route 53

Amazon Route 53 was configured to provide DNS resolution for the deployed application using hosted zones and alias records pointing to the Application Load Balancer.

**Troubleshooting:** DNS propagation delays, incorrect record configuration, alias resolution failures, and domain verification.

---

## 14. Auto Scaling

Auto Scaling policies were implemented to automatically increase or decrease application capacity based on workload demand, improving both availability and cost optimization.

**Troubleshooting:** Scaling policies not triggering, launch failures, unhealthy instances, and insufficient capacity.

---

## 15. CI/CD

A Continuous Integration and Continuous Deployment (CI/CD) pipeline was implemented to automate application deployment from GitHub to AWS. Code changes triggered automated build and deployment processes, reducing manual intervention.

**Troubleshooting:** Pipeline execution failures, deployment rollbacks, build errors, missing environment variables, and authentication issues.

---

## 16. CloudWatch

Amazon CloudWatch was configured to collect metrics, application logs, dashboards, and alarms. Resource utilization and application performance were continuously monitored to detect operational issues before they affected users.

**Troubleshooting:** Missing logs, alarm configuration errors, metric collection failures, CloudWatch Agent issues, and delayed log delivery.

---

## 17. Amazon SNS

Amazon Simple Notification Service (SNS) was integrated with CloudWatch alarms to deliver email notifications whenever critical thresholds or failures occurred.

**Troubleshooting:** Subscription confirmation failures, notification delivery issues, permission errors, and alarm integration problems.

---

## 18. AWS CloudTrail

AWS CloudTrail was enabled to record all API activity across the environment. Logs were reviewed to audit infrastructure changes, investigate incidents, and identify unauthorized actions.

**Troubleshooting:** Missing events, disabled trails, logging configuration issues, and S3 delivery failures.

---

## 19. Database

A relational database was provisioned to support the application. Connectivity, authentication, backups, storage management, and performance monitoring were validated throughout deployment.

**Troubleshooting:** Connection failures, authentication errors, storage limitations, high CPU utilization, and slow query performance.

---

## 20. Terraform

Infrastructure provisioning was automated using Terraform. Networking, compute resources, storage, and supporting services were defined as code to enable consistent, repeatable deployments.

**Troubleshooting:** State conflicts, provider authentication issues, dependency ordering, resource drift, and failed apply operations.

---

## 21. Production Incident Simulation

To reinforce operational readiness, I simulated numerous production incidents across networking, compute, storage, containers, load balancing, monitoring, security, and deployments. Each scenario followed a structured troubleshooting methodology:

* Identify symptoms
* Collect evidence
* Review logs and metrics
* Determine root cause
* Implement recovery
* Validate system health
* Document Root Cause Analysis (RCA)

This exercise strengthened my ability to respond systematically to production issues while minimizing downtime.

---

# Skills Demonstrated

* AWS Infrastructure Deployment
* Cloud Networking
* Linux Administration
* EC2 Management
* Docker Containerization
* Container Orchestration with ECS
* Load Balancing
* DNS Management
* Storage Administration
* CI/CD Implementation
* Infrastructure as Code
* Monitoring and Alerting
* Log Analysis
* Security Best Practices
* Production Troubleshooting
* Incident Response
* Root Cause Analysis
* Cloud Automation
* Version Control
* Technical Documentation

---

# Key Takeaways

Through this project, I developed practical experience deploying and supporting a cloud-native application using AWS services commonly found in production environments. Beyond deploying infrastructure, I focused on validating configurations, monitoring system health, troubleshooting failures, documenting implementation steps, and automating deployments. This project reflects the day-to-day responsibilities of a Cloud Support Engineer, including infrastructure management, operational support, incident investigation, and continuous improvement of cloud-based systems.

---

## Future Improvements

Future enhancements include implementing HTTPS with AWS Certificate Manager, AWS WAF for application protection, ECS blue/green deployments, centralized log aggregation, container vulnerability scanning, CloudWatch dashboards for business metrics, automated backups, disaster recovery strategies, and advanced security monitoring to further align the environment with enterprise production standards.
