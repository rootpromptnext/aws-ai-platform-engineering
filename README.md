# AWS AI Platform Engineering

## From DevOps Engineer → MLOps Engineer → LLMOps Engineer → AI Platform Engineer → AIOps Engineer

---

# 🎯 Objective

Build a complete Enterprise AI Platform on AWS using:

- Terraform
- EKS
- Docker
- GitHub Actions
- Amazon Bedrock
- OpenSearch
- RAG
- MCP
- Bedrock Agents
- MLflow
- SageMaker
- CloudWatch
- Prometheus
- Grafana
- OpenTelemetry
- Lambda
- EventBridge

---

# 🏗 Final Architecture

```text
GitHub
   |
GitHub Actions
   |
Terraform
   |
AWS
   |
EKS
   |
-----------------------------------------------------
|                                                   |
|                   AI Platform                     |
|                                                   |
|  MLOps       LLMOps               AIOps           |
|                                                   |
| SageMaker   Bedrock          CloudWatch           |
| MLflow      RAG              Prometheus           |
| Registry    OpenSearch       Grafana              |
| Endpoint    MCP              OpenTelemetry        |
|             Agents           Auto Remediation     |
-----------------------------------------------------
```

---

# Phase 1: Platform Engineering

## Milestone 1: Platform Bootstrap

### Topics

- AWS Account Setup
- IAM
- AWS CLI
- Terraform
- Remote State Management
- VPC
- EKS
- ECR
- Kubernetes Foundations

### AWS Services

- IAM
- S3
- DynamoDB
- VPC
- EKS
- ECR

### Labs

- Create Terraform Backend
- Configure S3 State Storage
- Configure DynamoDB Locking
- Deploy VPC
- Deploy EKS
- Create ECR Repository
- Install ALB Controller
- Install Metrics Server
- Install Karpenter
- Deploy Test Application

### Outcome

✅ Production Kubernetes Platform

---

# Phase 2: Building AI Applications

## Milestone 2: Bedrock Chat Application

### Topics

- Python
- FastAPI
- Bedrock Runtime API
- Claude Models

### Services

- Amazon Bedrock
- IAM

### Labs

Build:

```text
User
 |
FastAPI
 |
Claude
```

### Outcome

✅ ChatGPT-style application

---

## Milestone 3: Deploy Application on EKS

### Topics

- Docker
- Kubernetes
- Deployments
- Services
- ALB Ingress

### Services

- EKS
- ECR
- ALB

### Labs

- Containerize Application
- Push Image to ECR
- Deploy to EKS
- Configure Ingress
- Test Public Access

### Outcome

✅ AI Application Running on Kubernetes

---

## Milestone 4: CI/CD Platform

### Topics

- GitHub Actions
- CI/CD
- Container Automation

### Services

- GitHub Actions
- ECR
- EKS

### Labs

Pipeline:

```text
Git Push
    |
Build
    |
Scan
    |
Push ECR
    |
Deploy EKS
```

### Outcome

✅ Automated Deployments

---

# Phase 3: LLMOps

## Milestone 5: Custom RAG Platform

### Topics

- Embeddings
- Chunking
- Similarity Search
- Semantic Search
- Retrieval

### Services

- Bedrock
- OpenSearch
- S3

### Labs

```text
PDF
 |
Chunking
 |
Embedding
 |
OpenSearch
 |
Claude
```

### Outcome

✅ Enterprise RAG Chatbot

---

## Milestone 6: Bedrock Knowledge Bases

### Topics

- Knowledge Bases
- Data Sources
- Sync Jobs
- Managed Retrieval

### Services

- Bedrock Knowledge Bases
- S3

### Labs

- Create Knowledge Base
- Configure Data Source
- Sync Documents
- Query Data

### Outcome

✅ Managed RAG Platform

---

## Milestone 7: MCP Platform

### Topics

- MCP Basics
- MCP Architecture
- MCP Client
- MCP Server
- Tool Discovery
- Tool Execution

### Labs

Build MCP Servers for:

- AWS CLI
- EKS
- CloudWatch
- Cost Explorer

### Outcome

✅ Tool-Enabled LLM

---

## Milestone 8: CloudOps Agent

### Topics

- Bedrock Agents
- Tool Calling
- Multi-Step Reasoning
- Agent Workflows

### Services

- Bedrock Agents
- MCP
- CloudWatch
- EKS

### Labs

Agent Use Cases:

```text
Show failed pods

Show EKS node usage

Show deployment status

Show CloudWatch errors

Show AWS cost
```

### Outcome

✅ AI-Powered Cloud Operations Assistant

---

# Phase 4: AIOps

## Milestone 9: Observability Platform

### Topics

- Metrics
- Logs
- Traces
- Distributed Observability

### Tools

- CloudWatch
- Prometheus
- Grafana
- OpenTelemetry

### Labs

Monitor:

- FastAPI
- Bedrock
- OpenSearch
- MCP Calls
- Agent Calls
- Kubernetes

### Outcome

✅ Complete Observability Stack

---

## Milestone 10: AIOps & Auto Remediation

### Topics

- Alerting
- Incident Management
- EventBridge
- Lambda
- Systems Manager

### Services

- CloudWatch
- EventBridge
- Lambda
- SNS
- Systems Manager

### Labs

Automate:

```text
Restart Failed Pod

Scale Deployment

Delete Stuck Pod

Rollback Release

Open Incident

Send Alert
```

### Outcome

✅ Self-Healing AI Platform

---

# Phase 5: MLOps

## Module M1: Machine Learning Fundamentals

### Topics

- Regression
- Classification
- Clustering
- Feature Engineering
- Model Lifecycle

### Outcome

✅ Understand Core ML Concepts

---

## Module M2: MLflow

### Topics

- Experiment Tracking
- Metrics Tracking
- Artifact Tracking

### Labs

- Deploy MLflow
- Track Experiments
- Compare Results

### Outcome

✅ Experiment Management

---

## Module M3: SageMaker Training

### Topics

- Training Jobs
- Containers
- Managed Training

### Labs

Train:

- XGBoost
- Random Forest

### Outcome

✅ Managed ML Training

---

## Module M4: Hyperparameter Tuning

### Topics

- HPO Jobs
- Optimization Strategies

### Labs

- Run Multiple Training Jobs
- Compare Accuracy

### Outcome

✅ Automated Optimization

---

## Module M5: Feature Store

### Topics

- Feature Engineering
- Feature Management
- Reuse

### Labs

- Create Feature Store
- Store Training Features

### Outcome

✅ Reusable ML Features

---

## Module M6: Model Registry

### Topics

- Versioning
- Promotion
- Rollback

### Labs

- Register Model V1
- Register Model V2
- Promote Production Model

### Outcome

✅ Model Governance

---

## Module M7: Model Serving

### Topics

- Real-Time Inference
- Batch Inference
- Multi-Model Endpoints

### Labs

Deploy:

```text
Model
 |
Endpoint
 |
Prediction
```

### Outcome

✅ Production Inference

---

## Module M8: Model Monitoring

### Topics

- Data Drift
- Model Drift
- Bias Monitoring
- Data Quality

### Services

- SageMaker Model Monitor

### Labs

- Detect Drift
- Generate Monitoring Reports

### Outcome

✅ Production ML Monitoring

---

# 📁 Repository Structure

```text
aws-ai-platform-engineering/
|
├── 01-platform-bootstrap/
├── 02-bedrock-chatbot/
├── 03-eks-deployment/
├── 04-cicd-platform/
├── 05-custom-rag/
├── 06-bedrock-knowledge-bases/
├── 07-mcp-platform/
├── 08-cloudops-agent/
├── 09-observability-platform/
├── 10-aiops-remediation/
|
├── 11-mlflow/
├── 12-sagemaker-training/
├── 13-feature-store/
├── 14-model-registry/
├── 15-model-serving/
├── 16-model-monitoring/
|
├── architecture/
├── diagrams/
├── docs/
└── README.md
```

---

# 🎓 Skills Gained

## Platform Engineering

- Terraform
- AWS Networking
- EKS
- Docker
- ECR
- GitHub Actions

## LLMOps

- Bedrock
- Claude
- Prompt Engineering
- OpenSearch
- Embeddings
- RAG
- Knowledge Bases
- MCP
- Bedrock Agents

## AIOps

- CloudWatch
- Prometheus
- Grafana
- OpenTelemetry
- Incident Management
- Auto Remediation

## MLOps

- MLflow
- SageMaker
- Feature Store
- Model Registry
- Training Pipelines
- Model Monitoring

---

# 🚀 Final Capstone

```text
User
 |
ALB
 |
FastAPI
 |
Bedrock Agent
 |
------------------------------------------------
|                    MCP                        |
------------------------------------------------
|         |          |            |             |
EKS   CloudWatch   Cost      OpenSearch        ML
                                  |
                                 RAG
                                  |
                                 S3
                                  |
                             Documents
```

### Features

- AI Chat Assistant
- Enterprise RAG
- Bedrock Agents
- MCP Tools
- CloudOps Assistant
- Cost Assistant
- Kubernetes Assistant
- Observability Dashboard
- Auto Remediation
- ML Training Pipeline
- Model Registry
- Model Monitoring

### Final Outcome

✅ AWS Platform Engineer  
✅ MLOps Engineer  
✅ LLMOps Engineer  
✅ AIOps Engineer  
✅ AI Platform Engineer
