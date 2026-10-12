# Phase 1: Platform Engineering

# Milestone 1: Platform Bootstrap

## Objective

Build a production-ready AWS Kubernetes platform that will serve as the foundation for all upcoming MLOps, LLMOps, and AIOps workloads.

Final Target:

```text
AWS
 |
VPC
 |
EKS
 |
----------------------------------
|                                |
ALB                         ECR
|                                |
Applications              Container Images
|
Kubernetes
|
Metrics Server
|
Karpenter
```

---

# Lab 1: AWS Account Setup

## Goal

Prepare AWS account for platform engineering activities.

### Tasks

- Create AWS Account
- Configure MFA
- Create Billing Alerts
- Create Budget
- Enable CloudTrail
- Verify Region Selection

### Deliverables

```text
AWS Account Ready
Budget Configured
CloudTrail Enabled
```

### Validation

```bash
aws sts get-caller-identity
```

Expected:

```json
{
  "Account": "xxxxxxxxxxxx"
}
```

---

# Lab 2: IAM Setup

## Goal

Create identities and permissions.

### Topics

- IAM Users
- IAM Groups
- IAM Roles
- Policies
- Least Privilege

### Tasks

Create:

```text
terraform-admin
eks-admin
github-actions-role (future)
```

Create Groups:

```text
platform-admins
developers
readonly
```

### Deliverables

```text
IAM Structure Created
Access Keys Generated
Permissions Defined
```

### Validation

```bash
aws iam list-users
```

---

# Lab 3: AWS CLI Setup

## Goal

Configure local machine access.

### Tasks

Install:

```bash
awscli
```

Configure:

```bash
aws configure
```

Verify:

```bash
aws sts get-caller-identity
```

### Deliverables

```text
CLI Configured
Credentials Working
```

---

# Lab 4: Repository Structure

## Goal

Create project repository.

### Repository

```text
aws-ai-platform-engineering
```

### Structure

```text
aws-ai-platform-engineering/
|
├── 01-platform-bootstrap/
│
├── terraform/
│   ├── backend/
│   ├── network/
│   ├── eks/
│   ├── iam/
│   └── ecr/
│
├── kubernetes/
│
├── docs/
│
├── diagrams/
│
└── README.md
```

### Deliverables

```text
Git Repository Ready
Folder Structure Created
```

---

# Lab 5: Terraform Installation

## Goal

Install Infrastructure as Code tooling.

### Topics

- Terraform Basics
- Providers
- State Files
- Modules

### Tasks

Install:

```bash
terraform
```

Validate:

```bash
terraform version
```

### Deliverables

```text
Terraform Installed
```

---

# Lab 6: Terraform Remote Backend

## Goal

Create centralized state management.

### Topics

- Remote State
- Team Collaboration
- State Locking

### AWS Services

- S3
- DynamoDB

### Tasks

Create:

```text
terraform-state-bucket
```

Create:

```text
terraform-lock-table
```

### Architecture

```text
Terraform
    |
    +----> S3 State File
    |
    +----> DynamoDB Lock
```

### Deliverables

```text
Remote State Configured
State Locking Enabled
```

### Validation

```bash
terraform init
```

---

# Lab 7: VPC Deployment

## Goal

Build production networking.

### Topics

- CIDR
- Subnets
- Internet Gateway
- NAT Gateway
- Routing

### Components

Create:

```text
VPC
```

CIDR:

```text
10.0.0.0/16
```

Subnets:

```text
Public-A
Public-B

Private-A
Private-B
```

### Architecture

```text
VPC
 |
 +---- Public Subnets
 |
 +---- Private Subnets
 |
 +---- Internet Gateway
 |
 +---- NAT Gateway
```

### Deliverables

```text
Production VPC
High Availability Networking
```

### Validation

```bash
aws ec2 describe-vpcs
```

---

# Lab 8: ECR Deployment

## Goal

Create container registry.

### Topics

- Container Registries
- Image Storage
- Image Versioning

### Tasks

Create:

```text
ai-platform
```

Repository.

### Architecture

```text
Developer
    |
Docker Build
    |
ECR
```

### Deliverables

```text
Private Registry Ready
```

### Validation

```bash
aws ecr describe-repositories
```

---

# Lab 9: EKS Deployment

## Goal

Deploy managed Kubernetes cluster.

### Topics

- EKS
- Node Groups
- Worker Nodes
- Autoscaling

### Components

Cluster:

```text
platform-eks
```

Node Group:

```text
platform-ng
```

Nodes:

```text
2
```

Instance Type:

```text
t3.medium
```

### Architecture

```text
EKS
 |
 +---- Control Plane
 |
 +---- Managed Nodes
```

### Deliverables

```text
Production EKS Cluster
```

### Validation

```bash
aws eks list-clusters
```

---

# Lab 10: Kubectl Access

## Goal

Connect workstation to Kubernetes.

### Tasks

Update kubeconfig:

```bash
aws eks update-kubeconfig \
--region ap-south-1 \
--name platform-eks
```

Verify:

```bash
kubectl get nodes
```

Expected:

```text
Ready
Ready
```

### Deliverables

```text
Kubectl Connected
```

---

# Lab 11: Kubernetes Foundations

## Goal

Understand cluster objects.

### Topics

- Namespaces
- Pods
- Deployments
- Services
- Ingress

### Labs

Create:

```yaml
Namespace
Deployment
Service
```

Commands:

```bash
kubectl get pods

kubectl get svc

kubectl get deploy
```

### Deliverables

```text
Basic Kubernetes Knowledge
```

---

# Lab 12: Install AWS Load Balancer Controller

## Goal

Enable ALB-based ingress.

### Topics

- OIDC
- IAM Roles for Service Accounts
- ALB Ingress

### Tasks

Install:

```text
AWS Load Balancer Controller
```

### Architecture

```text
Internet
   |
ALB
   |
Ingress
   |
Service
   |
Pods
```

### Validation

```bash
kubectl get pods -n kube-system
```

---

# Lab 13: Install Metrics Server

## Goal

Enable Kubernetes metrics.

### Topics

- CPU Metrics
- Memory Metrics
- HPA

### Tasks

Install:

```text
Metrics Server
```

### Validation

```bash
kubectl top nodes
```

### Deliverables

```text
Cluster Metrics Available
```

---

# Lab 14: Install Karpenter

## Goal

Enable intelligent autoscaling.

### Topics

- Node Provisioning
- Spot Instances
- Cost Optimization

### Tasks

Install:

```text
Karpenter
```

### Architecture

```text
Pods
 |
Karpenter
 |
New Nodes
```

### Validation

```bash
kubectl get pods -n karpenter
```

### Deliverables

```text
Dynamic Node Scaling Enabled
```

---

# Lab 15: Deploy Test Application

## Goal

Verify complete platform functionality.

### Application

```text
nginx
```

### Tasks

Deploy:

```yaml
Deployment
Service
Ingress
```

### Flow

```text
User
 |
ALB
 |
Ingress
 |
Service
 |
Nginx Pods
```

### Validation

```bash
kubectl get pods

kubectl get svc

kubectl get ingress
```

Open ALB URL.

Expected:

```text
NGINX Welcome Page
```

### Deliverables

```text
Application Successfully Running
```

---

# Milestone 1 Completion Checklist

## AWS

- [ ] AWS Account Ready
- [ ] IAM Configured
- [ ] AWS CLI Configured

## Terraform

- [ ] Terraform Installed
- [ ] S3 Backend Configured
- [ ] DynamoDB Locking Enabled

## Networking

- [ ] VPC Created
- [ ] Public Subnets Created
- [ ] Private Subnets Created
- [ ] NAT Gateway Created

## Container Platform

- [ ] ECR Created
- [ ] EKS Cluster Running
- [ ] Kubectl Connected

## Kubernetes

- [ ] ALB Controller Installed
- [ ] Metrics Server Installed
- [ ] Karpenter Installed
- [ ] Sample Application Deployed

## Outcome

✅ Production Kubernetes Platform

✅ Ready for Bedrock Applications

✅ Ready for RAG Workloads

✅ Ready for MCP Servers

✅ Ready for Agents

✅ Ready for MLOps Workloads

✅ Foundation for Entire AWS AI Platform Engineering Journey
