# 26. DevOps Concepts ⭐⭐⭐⭐⭐

## Introduction

**DevOps** is a combination of **Development (Dev)** and **Operations (Ops)**.

The main goal of DevOps is to improve the way software is:

- Developed
- Tested
- Built
- Released
- Deployed
- Monitored
- Maintained

DevOps uses **collaboration, automation, CI/CD, Infrastructure as Code, containers, monitoring, and reliable infrastructure practices** to deliver software faster and more consistently.

A simple DevOps lifecycle is:

```text
Plan
  ↓
Code
  ↓
Build
  ↓
Test
  ↓
Release
  ↓
Deploy
  ↓
Operate
  ↓
Monitor
  ↓
Feedback
  ↓
Plan
```

---

# Table of Contents

1. [What is DevOps?](#1-what-is-devops)
2. [Dev vs Ops](#2-dev-vs-ops)
3. [Continuous Integration](#3-continuous-integration)
4. [Continuous Delivery](#4-continuous-delivery)
5. [Continuous Delivery vs Continuous Deployment](#5-continuous-delivery-vs-continuous-deployment)
6. [Infrastructure as Code](#6-infrastructure-as-code)
7. [Automation](#7-automation)
8. [Configuration Management](#8-configuration-management)
9. [Containerization](#9-containerization)
10. [Orchestration](#10-orchestration)
11. [Monitoring](#11-monitoring)
12. [Logging](#12-logging)
13. [Observability](#13-observability)
14. [Infrastructure Provisioning](#14-infrastructure-provisioning)
15. [Immutable Infrastructure](#15-immutable-infrastructure)
16. [Blue-Green Deployment](#16-blue-green-deployment)
17. [Rolling Deployment](#17-rolling-deployment)
18. [Canary Deployment](#18-canary-deployment)
19. [Disaster Recovery](#19-disaster-recovery)
20. [High Availability](#20-high-availability)
21. [Scalability](#21-scalability)
22. [Fault Tolerance](#22-fault-tolerance)
23. [How These Concepts Work Together](#23-how-these-concepts-work-together)
24. [DevOps Example](#24-devops-example)
25. [Important Interview Questions](#25-important-interview-questions)
26. [Quick Revision](#26-quick-revision)
27. [Final Summary](#27-final-summary)

---

# 1. What is DevOps?

## Definition

**DevOps** is a set of practices, processes, and tools that brings Development and Operations teams together to build, test, deploy, operate, and improve software efficiently.

In simple words:

> **DevOps means developing and operating software together using collaboration, automation, monitoring, and continuous delivery practices.**

---

## Traditional Approach

In a traditional environment:

```text
Developers
    ↓
Write Code
    ↓
Operations
    ↓
Deploy Application
```

Development and Operations may work separately.

This can create:

- Communication problems
- Manual processes
- Deployment delays
- Environment differences
- Difficult troubleshooting

---

## DevOps Approach

DevOps brings the teams and processes closer together:

```text
Develop
   ↓
Build
   ↓
Test
   ↓
Deploy
   ↓
Operate
   ↓
Monitor
   ↓
Feedback
   ↓
Develop
```

The process becomes continuous.

---

## Main Goals of DevOps

DevOps aims to improve:

- Collaboration
- Automation
- Deployment speed
- Software quality
- Reliability
- Monitoring
- Recovery
- Infrastructure management

---

# 2. Dev vs Ops

## Dev

**Development** is mainly responsible for building the application.

Developers typically work on:

- Writing code
- Developing features
- Fixing application bugs
- Unit testing
- Application design

Example:

```text
Developer
   ↓
Writes Python/Java/Node.js Code
   ↓
Git Repository
```

---

## Ops

**Operations** focuses on running and maintaining applications and infrastructure.

Operations commonly handles:

- Servers
- Networking
- Infrastructure
- Deployments
- Monitoring
- Availability
- Security
- Troubleshooting

Example:

```text
Operations
    ↓
AWS Infrastructure
    ↓
EC2 / VPC / Load Balancer
    ↓
Application
```

---

## DevOps

DevOps connects these responsibilities.

```text
Development
     +
Operations
     ↓
    DevOps
```

The goal is not simply to merge two job titles.

It is to create a collaborative process where software can move from development to production reliably and repeatedly.

---

# 3. Continuous Integration

## What is CI?

**CI stands for Continuous Integration.**

Continuous Integration means developers frequently integrate their code changes into a shared repository and automatically build and test those changes.

Example:

```text
Developer writes code
        ↓
Git Push
        ↓
CI Pipeline
        ↓
Build
        ↓
Automated Tests
        ↓
Result
```

---

## Example

Suppose three developers are working on an application.

```text
Developer A → Code
Developer B → Code
Developer C → Code
```

They frequently push their changes to Git.

A CI system automatically:

```text
Pulls Code
    ↓
Builds Application
    ↓
Runs Tests
    ↓
Reports Result
```

---

## Common CI Tools

Examples include:

- GitHub Actions
- Jenkins
- GitLab CI/CD
- Azure Pipelines

---

## Why CI?

CI helps detect problems early.

For example:

```text
Developer pushes code
        ↓
Automated test fails
        ↓
Developer receives feedback
        ↓
Bug is fixed
```

---

# 4. Continuous Delivery

## What is Continuous Delivery?

**Continuous Delivery** means keeping software in a deployable state through an automated process.

The application is automatically:

```text
Built
 ↓
Tested
 ↓
Packaged
 ↓
Prepared for Deployment
```

The final production deployment may require a manual approval.

---

## Example

```text
Developer
    ↓
Git Push
    ↓
Build
    ↓
Test
    ↓
Package
    ↓
Ready for Production
    ↓
Manual Approval
    ↓
Production
```

The important idea is:

> The software is always ready to be deployed.

---

# 5. Continuous Delivery vs Continuous Deployment

These two terms are commonly confused.

## Continuous Delivery

The application automatically reaches a deployable state.

Production deployment may require approval.

```text
Code
 ↓
Build
 ↓
Test
 ↓
Ready
 ↓
Manual Approval
 ↓
Production
```

---

## Continuous Deployment

Production deployment happens automatically after the required pipeline checks pass.

```text
Code
 ↓
Build
 ↓
Test
 ↓
Automatic Deployment
 ↓
Production
```

---

## Simple Difference

| Continuous Delivery | Continuous Deployment |
|---|---|
| Software is always deployable | Software is automatically deployed |
| Production may require approval | Production deployment is automated |
| More manual control | More automation |

---

# 6. Infrastructure as Code

## What is IaC?

**Infrastructure as Code (IaC)** means managing and creating infrastructure using code or configuration files instead of manually creating everything through a graphical console.

For example, instead of manually creating an EC2 instance:

```text
AWS Console
   ↓
Click
   ↓
Configure EC2
   ↓
Launch
```

you can define infrastructure using Terraform:

```text
Terraform Code
      ↓
terraform plan
      ↓
terraform apply
      ↓
AWS Infrastructure
```

---

## Example

Terraform can define:

- EC2
- VPC
- Subnets
- Security Groups
- Load Balancers
- S3
- IAM resources

---

## Benefits of IaC

IaC provides:

- Repeatability
- Automation
- Version control
- Consistency
- Easier recovery
- Easier infrastructure changes

---

## Common IaC Tools

- Terraform
- AWS CloudFormation
- Ansible for configuration/automation use cases

For your Cloud + DevOps learning path, **Terraform is an important IaC tool to prioritize.**

---

# 7. Automation

## What is Automation?

**Automation** means using tools or scripts to perform tasks automatically instead of performing them manually every time.

Example:

Manual:

```text
Build
 ↓
Test
 ↓
Deploy
```

Someone performs each step manually.

Automated:

```text
Git Push
   ↓
Build Automatically
   ↓
Test Automatically
   ↓
Deploy Automatically
```

---

## Examples of DevOps Automation

- Automated testing
- Automated builds
- Automated deployments
- Infrastructure provisioning
- Configuration
- Monitoring alerts
- Scaling

---

## Why Automation?

Automation helps reduce:

- Manual errors
- Repetitive work
- Deployment time
- Inconsistency

---

# 8. Configuration Management

## What is Configuration Management?

**Configuration Management** means maintaining systems and software configurations in a consistent and controlled way.

For example, suppose you have 10 servers.

You want all of them to have:

```text
Nginx
Python
Security settings
Application configuration
Required packages
```

Instead of configuring every server manually, configuration management tools can automate the process.

---

## Example

```text
Configuration File
       ↓
Automation Tool
       ↓
Server 1
Server 2
Server 3
Server 4
```

---

## Common Tool

**Ansible** is commonly used for configuration management and automation.

---

## Simple Example

You can define:

```text
Install Nginx
Start Nginx
Enable Nginx
Copy Configuration
```

and automate those actions across multiple servers.

---

# 9. Containerization

## What is Containerization?

**Containerization** is the process of packaging an application together with its dependencies into a container.

A container can include:

```text
Application
Dependencies
Libraries
Configuration
Runtime
```

---

## Why Containers?

Imagine an application works on the developer's computer but fails on another machine.

Containers help create a more consistent runtime environment.

```text
Application
    +
Dependencies
    +
Runtime
    ↓
Container
```

---

## Docker

**Docker** is one of the most commonly used container technologies.

Example:

```text
Dockerfile
    ↓
Docker Image
    ↓
Docker Container
    ↓
Application
```

---

## Container vs Virtual Machine

### Virtual Machine

```text
Hardware
   ↓
Hypervisor
   ↓
Guest OS
   ↓
Application
```

### Container

```text
Operating System
       ↓
Container Runtime
       ↓
Container
       ↓
Application
```

Containers generally share the host operating system kernel, whereas VMs include a guest operating system.

---

# 10. Orchestration

## What is Orchestration?

When you have many containers, managing them manually becomes difficult.

**Container orchestration** means automatically managing containers and their workloads.

It can involve:

- Deployment
- Scaling
- Networking
- Service discovery
- Health checking
- Restarting failed workloads

---

## Kubernetes

**Kubernetes** is a widely used container orchestration platform.

Example:

```text
Kubernetes
     ↓
Container 1
Container 2
Container 3
Container 4
```

If a container fails, Kubernetes can detect the problem and take corrective action according to the configured desired state.

---

## Simple Example

Without orchestration:

```text
100 Containers
     ↓
Manual Management
```

With orchestration:

```text
100 Containers
     ↓
Kubernetes
     ↓
Automated Management
```

---

# 11. Monitoring

## What is Monitoring?

**Monitoring** means continuously collecting and checking metrics and system information to understand the health and performance of systems.

Examples of things to monitor:

- CPU usage
- Memory usage
- Disk usage
- Network traffic
- Application latency
- Request count
- Error rate
- Availability

---

## Example

Suppose an EC2 instance has high CPU usage.

Monitoring can detect:

```text
CPU = 95%
```

An alert can then be generated.

```text
High CPU
   ↓
Monitoring System
   ↓
Alert
   ↓
DevOps Engineer
```

---

## AWS Monitoring Example

**Amazon CloudWatch** can be used to monitor AWS resources and applications.

---

# 12. Logging

## What is Logging?

**Logging** means recording events and information generated by applications and infrastructure.

Example application log:

```text
2026-10-02 10:30:15
User login successful
```

Another example:

```text
2026-10-02 10:31:22
Database connection failed
```

---

## Why Logging?

Logs help with:

- Troubleshooting
- Debugging
- Security investigations
- Understanding application behavior
- Finding errors

---

## Example

```text
Application
    ↓
Logs
    ↓
Log Storage
    ↓
DevOps Engineer
```

---

# 13. Observability

## What is Observability?

**Observability** is the ability to understand the internal state and behavior of a system by examining the data it produces.

The commonly discussed three pillars are:

```text
Observability
     |
     +---- Metrics
     |
     +---- Logs
     |
     +---- Traces
```

---

## Metrics

Metrics are numerical measurements.

Examples:

```text
CPU = 75%
Memory = 60%
Requests = 1,000/min
Error Rate = 2%
```

---

## Logs

Logs are recorded events.

Example:

```text
Database connection failed
```

---

## Traces

A trace helps follow a request through multiple components.

Example:

```text
User Request
    ↓
API Gateway
    ↓
Service A
    ↓
Service B
    ↓
Database
```

A distributed trace can help identify where time was spent or where a request failed.

---

## Monitoring vs Observability

### Monitoring

Monitoring asks:

> "Is the system healthy?"

### Observability

Observability helps answer:

> "Why is the system behaving this way?"

---

# 14. Infrastructure Provisioning

## What is Infrastructure Provisioning?

**Infrastructure provisioning** means creating and configuring infrastructure resources required to run an application.

Examples:

```text
VPC
Subnets
EC2
Security Groups
Load Balancer
S3
Database
```

---

## Manual Provisioning

```text
AWS Console
   ↓
Create VPC
   ↓
Create Subnet
   ↓
Create EC2
   ↓
Create Security Group
```

---

## Automated Provisioning

Using Terraform:

```text
Terraform Code
      ↓
Plan
      ↓
Apply
      ↓
Infrastructure
```

---

## Provisioning vs Configuration

These concepts are related but different.

### Provisioning

Creates infrastructure.

```text
Create EC2
Create VPC
Create S3
```

### Configuration Management

Configures systems after they exist.

```text
Install Nginx
Configure Nginx
Install Packages
```

---

# 15. Immutable Infrastructure

## What is Immutable Infrastructure?

**Immutable infrastructure** means that once infrastructure is deployed, you generally do not modify the existing server in place.

Instead, when a change is required, you create a new version and replace the old infrastructure.

---

## Traditional Mutable Approach

```text
Server
  ↓
Change Configuration
  ↓
Same Server
```

---

## Immutable Approach

```text
Old Server
    ↓
Create New Version
    ↓
New Server
    ↓
Replace Old Server
```

---

## Example

Suppose you have:

```text
EC2 Version 1
```

You need to update the application.

Instead of changing it manually:

```text
EC2 Version 1
     ↓
Manual Changes
```

you create:

```text
EC2 Version 2
```

and replace Version 1.

---

## Benefits

Immutable infrastructure can provide:

- Consistency
- Predictable deployments
- Easier rollback
- Reduced configuration drift

---

# 16. Blue-Green Deployment

## What is Blue-Green Deployment?

**Blue-Green Deployment** uses two environments.

```text
Blue  → Current Production
Green → New Version
```

For example:

```text
             Load Balancer
                  |
          ┌───────┴───────┐
          ↓               ↓
        BLUE            GREEN
       Version 1        Version 2
```

Initially:

```text
Users
  ↓
Blue
```

You deploy and test Version 2 in Green.

After validation:

```text
Users
  ↓
Green
```

Traffic is switched to Green.

---

## Main Advantage

If something goes wrong, traffic can potentially be switched back to Blue.

```text
Green Problem
     ↓
Switch Traffic
     ↓
Blue
```

---

# 17. Rolling Deployment

## What is Rolling Deployment?

A **rolling deployment** gradually replaces old application instances with new ones instead of replacing everything at once.

Suppose you have four instances:

```text
Instance 1 → Old
Instance 2 → Old
Instance 3 → Old
Instance 4 → Old
```

Deploy the new version gradually:

```text
Instance 1 → New
Instance 2 → Old
Instance 3 → Old
Instance 4 → Old
```

Then:

```text
Instance 1 → New
Instance 2 → New
Instance 3 → Old
Instance 4 → Old
```

Then:

```text
Instance 1 → New
Instance 2 → New
Instance 3 → New
Instance 4 → Old
```

Finally:

```text
Instance 1 → New
Instance 2 → New
Instance 3 → New
Instance 4 → New
```

---

## Advantage

The application can continue serving traffic while the deployment progresses, depending on the architecture and deployment configuration.

---

# 18. Canary Deployment

## What is Canary Deployment?

A **Canary deployment** releases a new version to a small percentage of users or traffic first.

Example:

```text
100% Traffic
     ↓
95% → Old Version
5%  → New Version
```

You monitor the new version.

If everything works correctly:

```text
90% → Old
10% → New
```

Then:

```text
50% → Old
50% → New
```

Eventually:

```text
100% → New Version
```

---

## Why Use Canary Deployment?

It reduces the initial exposure of a new release.

If the new version has a problem, only a smaller portion of traffic may be affected.

---

# 19. Disaster Recovery

## What is Disaster Recovery?

**Disaster Recovery (DR)** is the process and strategy used to restore systems and data after a major failure or disaster.

Possible disasters include:

- Hardware failure
- Region-level disruption
- Data corruption
- Accidental deletion
- Cybersecurity incidents
- Infrastructure failure

---

## Example

Suppose an application is running in one environment and that environment becomes unavailable.

A disaster recovery strategy may use:

```text
Backup
   ↓
Recovery Environment
   ↓
Restore Application
   ↓
Resume Service
```

---

## Important DR Concepts

### Backup

Copies of data are stored so they can be restored later.

### Recovery Time Objective (RTO)

**RTO** is the target amount of time within which a service should be restored after a disruption.

Example:

```text
RTO = 1 hour
```

The recovery target is to restore the service within that timeframe.

### Recovery Point Objective (RPO)

**RPO** describes the maximum acceptable amount of data loss measured in time.

Example:

```text
RPO = 15 minutes
```

This means the recovery strategy aims to limit data loss to roughly the most recent 15 minutes of data, depending on implementation.

---

# 20. High Availability

## What is High Availability?

**High Availability (HA)** means designing a system to remain available with minimal interruption when individual components fail.

Instead of depending on one server:

```text
User
 ↓
Single Server
```

use multiple components:

```text
             Load Balancer
              /         \
             ↓           ↓
          Server 1    Server 2
```

If one server fails:

```text
Server 1 → Failed

Server 2 → Continues serving traffic
```

---

## AWS Example

You can improve availability by distributing resources across multiple Availability Zones.

```text
              Load Balancer
                 /     \
                ↓       ↓
              AZ-A     AZ-B
                |       |
              EC2     EC2
```

---

# 21. Scalability

## What is Scalability?

**Scalability** is the ability of a system to handle increasing workload by adding resources or changing resource capacity.

There are two major approaches.

---

## Vertical Scaling

Vertical scaling means increasing the capacity of an existing resource.

For example:

```text
Small EC2
   ↓
Larger EC2
```

You increase:

- CPU
- Memory
- Other resource capacity

---

## Horizontal Scaling

Horizontal scaling means adding more instances or resources.

Example:

```text
1 EC2
  ↓
3 EC2
  ↓
10 EC2
```

A load balancer can distribute traffic across them.

```text
             Load Balancer
            /      |      \
           ↓       ↓       ↓
         EC2     EC2     EC2
```

---

# 22. Fault Tolerance

## What is Fault Tolerance?

**Fault tolerance** is the ability of a system to continue operating even when one or more components fail.

Example:

```text
Application
    |
    +---- Server A
    |
    +---- Server B
```

If Server A fails:

```text
Server A → Failed

Server B → Continues
```

The application can continue operating.

---

## High Availability vs Fault Tolerance

These concepts are related but not identical.

### High Availability

Focuses on minimizing downtime and maintaining service availability.

### Fault Tolerance

Focuses on continuing operation despite component failures.

A highly fault-tolerant system generally requires redundancy and careful architecture.

---

# 23. How These Concepts Work Together

DevOps concepts are connected.

A typical workflow can look like:

```text
Developer
    ↓
Git
    ↓
Continuous Integration
    ↓
Build
    ↓
Test
    ↓
Container
    ↓
Deployment
    ↓
Infrastructure as Code
    ↓
Cloud Infrastructure
    ↓
Monitoring
    ↓
Logging
    ↓
Observability
    ↓
Feedback
```

---

## Infrastructure Side

```text
Terraform
    ↓
Infrastructure Provisioning
    ↓
AWS
    ↓
EC2 / VPC / Load Balancer
```

---

## Application Side

```text
Developer
    ↓
Git
    ↓
CI/CD
    ↓
Docker
    ↓
Kubernetes
    ↓
Application
```

---

## Operations Side

```text
Application
    ↓
Metrics
Logs
Traces
    ↓
Monitoring / Observability
    ↓
Alerts
    ↓
Troubleshooting
```

---

# 24. DevOps Example

Let's imagine a company has a web application.

## Step 1 — Developer Writes Code

```text
Developer
   ↓
Application Code
```

---

## Step 2 — Push to Git

```text
Developer
   ↓
GitHub
```

---

## Step 3 — CI Pipeline

```text
GitHub
   ↓
CI Pipeline
   ↓
Build
   ↓
Tests
```

---

## Step 4 — Build Container

```text
Application
   ↓
Dockerfile
   ↓
Docker Image
```

---

## Step 5 — Deploy

The application can be deployed to an environment such as:

```text
AWS
   ↓
Kubernetes / ECS / EC2
```

---

## Step 6 — Infrastructure

Infrastructure can be created using Terraform:

```text
Terraform
    ↓
VPC
EC2
Load Balancer
Security Groups
```

---

## Step 7 — Monitoring

After deployment:

```text
Application
     ↓
Metrics
     ↓
Logs
     ↓
Monitoring
```

---

## Step 8 — Continuous Improvement

If a problem is detected:

```text
Monitoring
    ↓
Alert
    ↓
DevOps Engineer
    ↓
Fix
    ↓
Git
    ↓
CI/CD
    ↓
New Deployment
```

This creates a continuous feedback loop.

---

# 25. Important Interview Questions

## 1. What is DevOps?

**Answer:**

DevOps is a set of practices and cultural approaches that brings development and operations closer together to improve software delivery, automation, reliability, and continuous improvement.

---

## 2. What is the difference between Dev and Ops?

**Answer:**

Development focuses mainly on building and testing software, while Operations focuses on deploying, running, monitoring, and maintaining applications and infrastructure. DevOps encourages collaboration between both areas.

---

## 3. What is CI?

**Answer:**

CI, or Continuous Integration, is the practice of frequently integrating code changes into a shared repository and automatically building and testing those changes.

---

## 4. What is Continuous Delivery?

**Answer:**

Continuous Delivery is the practice of keeping software in a deployable state through automated build, test, and release processes. Production deployment may require approval.

---

## 5. What is Continuous Deployment?

**Answer:**

Continuous Deployment automatically deploys validated changes to production without requiring a manual production approval step.

---

## 6. What is Infrastructure as Code?

**Answer:**

Infrastructure as Code is the practice of defining and managing infrastructure using code or configuration files instead of manually creating infrastructure.

---

## 7. What is automation in DevOps?

**Answer:**

Automation means using tools and scripts to perform repetitive tasks such as building, testing, deploying, provisioning infrastructure, and configuration automatically.

---

## 8. What is configuration management?

**Answer:**

Configuration management is the process of maintaining system and application configurations consistently and in a controlled way. Tools such as Ansible can automate configuration tasks.

---

## 9. What is containerization?

**Answer:**

Containerization packages an application and its dependencies into a container so that it can run consistently across environments.

---

## 10. What is orchestration?

**Answer:**

Orchestration is the automated management of containers and their workloads, including deployment, scaling, networking, and health management. Kubernetes is a common orchestration platform.

---

## 11. What is monitoring?

**Answer:**

Monitoring is the process of collecting and analyzing system and application metrics to understand health, performance, and availability.

---

## 12. What is logging?

**Answer:**

Logging is the process of recording application and infrastructure events to help with troubleshooting, debugging, auditing, and analysis.

---

## 13. What is observability?

**Answer:**

Observability is the ability to understand the internal behavior of a system using telemetry such as metrics, logs, and traces.

---

## 14. What is infrastructure provisioning?

**Answer:**

Infrastructure provisioning is the process of creating and configuring infrastructure resources such as VPCs, EC2 instances, databases, and load balancers.

---

## 15. What is immutable infrastructure?

**Answer:**

Immutable infrastructure is an approach where deployed infrastructure is generally not modified in place. Instead, a new version is created and the old version is replaced.

---

## 16. What is Blue-Green deployment?

**Answer:**

Blue-Green deployment uses two environments. One runs the current version while the other runs the new version. Traffic can be switched between them after validation.

---

## 17. What is Rolling deployment?

**Answer:**

Rolling deployment gradually replaces instances running the old application version with instances running the new version.

---

## 18. What is Canary deployment?

**Answer:**

Canary deployment releases a new application version to a small portion of traffic or users first, allowing the new version to be monitored before increasing its traffic.

---

## 19. What is Disaster Recovery?

**Answer:**

Disaster Recovery is the strategy and process for restoring applications, infrastructure, and data after a major failure or disruption.

---

## 20. What is High Availability?

**Answer:**

High Availability is the design of systems to remain available with minimal interruption by using redundancy and eliminating single points of failure where practical.

---

## 21. What is scalability?

**Answer:**

Scalability is the ability of a system to handle increasing workload by increasing the capacity of existing resources or adding additional resources.

---

## 22. What is fault tolerance?

**Answer:**

Fault tolerance is the ability of a system to continue operating when one or more components fail.

---

# 26. Quick Revision

## DevOps

```text
Development + Operations
          ↓
        DevOps
```

---

## CI

```text
Code
 ↓
Build
 ↓
Test
```

---

## Continuous Delivery

```text
Code
 ↓
Build
 ↓
Test
 ↓
Ready for Production
 ↓
Approval
 ↓
Deploy
```

---

## Continuous Deployment

```text
Code
 ↓
Build
 ↓
Test
 ↓
Automatic Deployment
 ↓
Production
```

---

## Infrastructure as Code

```text
Code
 ↓
Terraform
 ↓
Infrastructure
```

---

## Automation

```text
Manual Tasks
     ↓
Automation
     ↓
Repeatable Process
```

---

## Configuration Management

```text
Configuration
      ↓
Automation Tool
      ↓
Servers
```

---

## Containerization

```text
Application
+
Dependencies
     ↓
Container
```

---

## Orchestration

```text
Containers
     ↓
Kubernetes
     ↓
Automated Management
```

---

## Monitoring

```text
System
  ↓
Metrics
  ↓
Monitoring
  ↓
Alert
```

---

## Logging

```text
Application
    ↓
Logs
    ↓
Analysis
```

---

## Observability

```text
Observability
     |
     +---- Metrics
     |
     +---- Logs
     |
     +---- Traces
```

---

## Infrastructure Provisioning

```text
Terraform
    ↓
Create Infrastructure
```

---

## Immutable Infrastructure

```text
Old Version
    ↓
New Version
    ↓
Replace Old
```

---

## Blue-Green

```text
Blue  → Old Version
Green → New Version

Switch Traffic
     ↓
Green
```

---

## Rolling Deployment

```text
Old → New
Old → New
Old → New
Old → New
```

Gradual replacement.

---

## Canary Deployment

```text
95% → Old
5%  → New

Monitor

90% → Old
10% → New

Monitor

100% → New
```

---

## Disaster Recovery

```text
Failure
   ↓
Recovery Plan
   ↓
Restore
   ↓
Service Recovery
```

---

## High Availability

```text
Load Balancer
   /      \
Server 1  Server 2
```

If one fails, another can continue serving traffic.

---

## Scalability

### Vertical

```text
Small Server
     ↓
Large Server
```

### Horizontal

```text
1 Server
   ↓
3 Servers
   ↓
10 Servers
```

---

## Fault Tolerance

```text
Component A → Failed
Component B → Continues
```

---

# 27. Final Summary

The most important DevOps concepts to remember are:

```text
DevOps
  ↓
Collaboration
  ↓
Automation
  ↓
CI/CD
  ↓
Infrastructure as Code
  ↓
Containers
  ↓
Orchestration
  ↓
Monitoring
  ↓
Logging
  ↓
Observability
  ↓
Reliable Deployments
  ↓
High Availability
  ↓
Scalability
  ↓
Fault Tolerance
```

### One-line definitions for quick interview revision

| Concept | Simple Meaning |
|---|---|
| **DevOps** | Collaboration between development and operations with automation and continuous delivery practices |
| **Dev** | Builds and tests applications |
| **Ops** | Deploys, operates, and maintains applications and infrastructure |
| **CI** | Frequently integrate code and automatically build/test it |
| **Continuous Delivery** | Keep software ready for production deployment |
| **Continuous Deployment** | Automatically deploy validated changes to production |
| **IaC** | Manage infrastructure using code |
| **Automation** | Automatically perform repetitive tasks |
| **Configuration Management** | Maintain system configurations consistently |
| **Containerization** | Package applications and dependencies into containers |
| **Orchestration** | Automatically manage containers and workloads |
| **Monitoring** | Track system health and performance |
| **Logging** | Record system and application events |
| **Observability** | Understand system behavior using metrics, logs, and traces |
| **Infrastructure Provisioning** | Create infrastructure resources |
| **Immutable Infrastructure** | Replace infrastructure instead of modifying it in place |
| **Blue-Green** | Run old and new environments and switch traffic |
| **Rolling Deployment** | Gradually replace old instances with new ones |
| **Canary Deployment** | Release the new version to a small percentage first |
| **Disaster Recovery** | Restore systems after major failures |
| **High Availability** | Minimize downtime using redundancy |
| **Scalability** | Handle increasing workload by adding capacity |
| **Fault Tolerance** | Continue operating despite component failures |

## Most Important DevOps Flow

```text
Developer
    ↓
Git
    ↓
CI
    ↓
Build
    ↓
Test
    ↓
Docker
    ↓
CD
    ↓
Deployment
    ↓
Infrastructure
    ↓
Monitoring
    ↓
Logging
    ↓
Observability
    ↓
Feedback
    ↓
Continuous Improvement
```

> **Interview-ready definition:**  
> **DevOps is a set of practices that brings development and operations together through collaboration, automation, CI/CD, Infrastructure as Code, containerization, monitoring, and reliable deployment practices to deliver and operate software efficiently.**

