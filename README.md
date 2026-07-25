# AWS Production Cloud Support Engineer Training

> A hands-on, production-focused AWS Cloud Support Engineer training repository built around real-world operations, troubleshooting, incident response, reliability engineering, and production support.

---

# Overview

This repository documents my end-to-end journey toward becoming a **Production Cloud Support Engineer**.

Unlike traditional AWS courses that focus on creating resources, this training focuses on **operating, monitoring, troubleshooting, recovering, and improving production systems** using real-world scenarios.

Throughout this training, I worked with three applications:

* **Flask Application** – Traditional web application running on AWS infrastructure
* **Google Online Boutique** – Kubernetes-based microservices application
* **Astronomy Shop** – Cloud-native application used for observability and distributed tracing

The emphasis has been on thinking and operating like a **Cloud Support Engineer**, **Cloud Operations Engineer**, or **Site Reliability Engineer (SRE)** rather than an application developer.

---

# Training Philosophy

The objective of this repository is to answer questions such as:

* What happens when production breaks?
* How do you investigate incidents?
* How do you restore services safely?
* How do you determine the root cause?
* How do you prevent incidents from happening again?

Every module follows a production support mindset.

Each module includes:

* Real Production Introduction
* Module Goal
* What It Is
* Why Companies Use It
* Where It Fits in Production Architecture
* Internal Working
* Production Workflow
* Commands Used by Cloud Support Engineers
* Common Production Failures
* Incident Tickets
* Troubleshooting Methodology

  * Symptoms
  * Evidence
  * Investigation
  * Root Cause
  * Recovery
  * Verification
  * RCA
* Hands-on Labs
* Production Exercises
* Interview Questions

---

# Technologies Covered

## Linux

* Linux administration
* Users and permissions
* Services
* SSH
* Networking
* Log analysis
* Process management
* Disk management
* Performance troubleshooting

---

## Python & Web Application Operations

* Python virtual environments
* Flask production deployment
* Gunicorn
* Nginx
* systemd

---

## AWS Infrastructure

* AWS CLI
* IAM
* EC2
* EBS
* VPC
* Security Groups
* Network ACLs
* Route Tables
* Internet Gateway
* NAT Gateway
* Route 53
* AWS Certificate Manager (ACM)
* AWS Systems Manager (SSM)

---

## Data Services

* Amazon RDS
* Redis
* Amazon S3

---

## Containers & Orchestration

* Docker
* Amazon ECR
* Amazon ECS
* Amazon EKS

---

## Infrastructure as Code & Deployment

* Git
* CI/CD
* Terraform

---

## Monitoring & Observability

* Amazon CloudWatch
* CloudWatch Agent
* CloudWatch Alarms
* SNS
* AWS X-Ray
* OpenTelemetry

---

## Serverless

* AWS Lambda

---

## Production Operations

* Incident Response
* Troubleshooting
* Root Cause Analysis (RCA)
* Post-Incident Review
* Reliability Engineering

---

# Applications Used

## Flask Application

Used to practice:

* Linux administration
* EC2 operations
* Nginx
* Gunicorn
* systemd
* RDS
* Redis
* S3
* Docker
* ECS
* CloudWatch
* IAM
* Networking
* Incident response
* Root Cause Analysis

Typical production scenarios:

* HTTP 500 errors
* 502 Bad Gateway
* 504 Gateway Timeout
* Database connectivity failures
* Disk full
* High CPU
* Memory exhaustion
* Deployment failures
* SSL certificate issues
* Application recovery

---

## Google Online Boutique

Used to practice Kubernetes and microservices operations.

Topics covered:

* Amazon EKS
* Pod lifecycle
* CrashLoopBackOff
* ImagePullBackOff
* Kubernetes networking
* Service-to-service communication
* Redis failures
* Rolling deployments
* Kubernetes troubleshooting
* Production incidents
* Distributed application failures

---

## Astronomy Shop

Used to practice cloud-native observability.

Topics covered:

* OpenTelemetry
* AWS X-Ray
* Distributed tracing
* Dependency analysis
* Performance bottlenecks
* Latency investigation
* Root Cause Analysis
* Post-Incident Reviews
* Reliability improvements

---

# Production Skills Developed

This repository focuses on the day-to-day responsibilities of a Cloud Support Engineer.

Examples include:

* Production monitoring
* Incident response
* Infrastructure troubleshooting
* Application troubleshooting
* Database troubleshooting
* Network troubleshooting
* Container troubleshooting
* Kubernetes troubleshooting
* Performance analysis
* Root Cause Analysis
* Reliability improvement
* Documentation
* Production communication

---

# Troubleshooting Workflow

Every production issue is approached using the same structured methodology.

Symptoms

↓

Customer Impact

↓

Evidence Collection

↓

Metrics

↓

Logs

↓

Distributed Traces

↓

Investigation

↓

Root Cause

↓

Recovery

↓

Verification

↓

Root Cause Analysis

↓

Post-Incident Review

---

# Common Production Scenarios Practiced

## Linux

* SSH failures
* Disk full
* High CPU
* High memory
* Service failures
* Permission issues

## AWS

* EC2 unavailable
* EBS storage issues
* IAM AccessDenied
* S3 permission issues
* Security Group misconfiguration
* Route Table problems
* NAT Gateway failures
* Route 53 DNS issues

## Application

* HTTP 500
* HTTP 502
* HTTP 503
* HTTP 504
* Gunicorn failures
* Nginx failures
* Flask startup failures

## Database

* Connection timeouts
* Connection exhaustion
* Slow queries
* Storage issues

## Containers

* ECS task failures
* Docker container crashes
* Image pull failures

## Kubernetes

* CrashLoopBackOff
* ImagePullBackOff
* Pending Pods
* Failed readiness probes
* Failed liveness probes
* Service connectivity failures

## Monitoring

* CloudWatch alarm investigations
* CloudWatch Agent troubleshooting
* X-Ray trace analysis
* OpenTelemetry latency investigations

---

# Production Incident Lifecycle Practiced

* Detect incidents
* Assess customer impact
* Collect evidence
* Investigate production systems
* Restore services
* Verify recovery
* Write Root Cause Analysis
* Conduct Post-Incident Reviews
* Improve production reliability

---

# Cloud Support Engineer Mindset

This repository is built around the operational mindset expected in production environments.

Rather than focusing only on deploying AWS resources, the training emphasizes:

* Understanding customer impact
* Making evidence-based decisions
* Following structured troubleshooting workflows
* Restoring services safely
* Preventing recurring incidents
* Improving operational reliability

---

# Current Outcome

Through this training I have built practical experience operating production-style AWS environments using:

* Flask
* Google Online Boutique
* Astronomy Shop

The focus has been on:

* AWS infrastructure operations
* Linux administration
* Cloud monitoring
* Production troubleshooting
* Incident management
* Root Cause Analysis
* Reliability engineering

This repository represents my progression toward Cloud Support Engineer, Cloud Operations Engineer, AWS Support Engineer, and Site Reliability Engineer (SRE) roles.

---

# Repository Status

**Status:** In Progress

I continue to expand this repository with additional production scenarios, automation, monitoring improvements, and hands-on operational exercises to strengthen my production support skills.
