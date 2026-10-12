AWS AI Platform Engineering
From DevOps Engineer → MLOps Engineer → LLMOps Engineer → AI Platform Engineer → AIOps Engineer

This is the roadmap we decided for your repository:

aws-ai-platform-engineering


The repository will not contain separate disconnected labs.

It will contain 10 progressive milestone projects that build a single enterprise platform.

Final Platform We Will Build
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
------------------------------------------------
|                                              |
|                   AI Platform                |
|                                              |
|  MLOps       LLMOps          AIOps           |
|                                              |
| SageMaker   Bedrock      CloudWatch          |
| MLflow      RAG          Prometheus          |
| Registry    Agents       Grafana             |
| Endpoint    MCP          OpenTelemetry       |
|             OpenSearch   Auto Remediation    |
------------------------------------------------

Milestone 1
Platform Bootstrap
Goal

Build the AWS foundation.

Topics
AWS Account Setup
AWS CLI
Terraform Basics
Remote State Management
Networking
Kubernetes Foundations
AWS Services
IAM
S3
DynamoDB
VPC
EKS
ECR
Labs
Create Terraform Backend
Create Remote State
Deploy VPC
Deploy EKS Cluster
Deploy ECR Repository
Install ALB Controller
Install Metrics Server
Install Karpenter
Deploy Sample Application
Outcome

✅ Production-ready Kubernetes platform

Milestone 2
AI Chat Application
Goal

Build first AI application.

Topics
Python
FastAPI
Bedrock Runtime API
Claude Models
AWS Services
Bedrock
IAM
Labs

Build:

User
 |
FastAPI
 |
Claude

Outcome

✅ Working ChatGPT-style application

Milestone 3
Platform Deployment
Goal

Run chatbot on Kubernetes.

Topics
Docker
Kubernetes
ALB Ingress
Service Exposure
AWS Services
ECR
EKS
ALB
Labs
Build Docker Image
Push Image to ECR
Deploy to EKS
Configure Ingress
Access Application via ALB
Outcome

✅ AI application running on EKS

Milestone 4
CI/CD Platform
Goal

Automate deployments.

Topics
GitHub Actions
GitOps
Image Versioning
AWS Services
ECR
EKS
Labs

Pipeline:

Git Push
    |
Build
    |
Security Scan
    |
Push ECR
    |
Deploy EKS

Outcome

✅ Automated AI platform deployment

Milestone 5
Custom RAG Platform
Goal

Build RAG from scratch.

Topics
Embeddings
Chunking
Semantic Search
Retrieval
AWS Services
Bedrock
S3
OpenSearch
Labs
PDF
 |
Chunk
 |
Embedding
 |
OpenSearch
 |
Claude

Outcome

✅ Enterprise document assistant

Milestone 6
Managed RAG
Goal

Learn AWS-native RAG.

Topics
Bedrock Knowledge Bases
Data Sources
Sync Jobs
AWS Services
Bedrock Knowledge Bases
S3
Labs
Create Knowledge Base
Connect S3
Sync Documents
Query Data
Outcome

✅ Managed RAG solution

Milestone 7
MCP Platform
Goal

Allow LLMs to use tools.

Topics
MCP Architecture
MCP Server
Tool Discovery
Tool Execution
Labs

Create MCP Servers:

AWS CLI
EKS
CloudWatch
Cost Explorer
Outcome

✅ Working MCP environment

Milestone 8
CloudOps Agent
Goal

Build AI Operations Engineer.

Topics
Bedrock Agents
Tool Calling
Multi-Step Reasoning
Labs

Agent Capabilities:

Show failing pods

Show EKS node usage

Show CloudWatch errors

Show AWS spending

Services
Bedrock Agent
MCP
EKS
CloudWatch
Outcome

✅ AI-powered DevOps Assistant

Milestone 9
Observability Platform
Goal

Monitor whole AI platform.

Topics
Metrics
Logs
Traces
Telemetry
Tools
CloudWatch
Prometheus
Grafana
OpenTelemetry
Labs

Monitor:

FastAPI

Bedrock

RAG

OpenSearch

MCP

Agent

Outcome

✅ Full observability stack

Milestone 10
AIOps & Auto Remediation
Goal

Self-healing AI platform.

Topics
Alerting
Incident Management
EventBridge
Lambda Automation
Services
CloudWatch
EventBridge
SNS
Lambda
Systems Manager
Labs

Automate:

Restart Failed Pods

Scale Workloads

Rollback Releases

Generate Incidents

Outcome

✅ Self-healing AI platform

MLOps Track (Added After Milestone 10)

Because your primary goal is Bedrock/RAG/MCP first.

Module M1

ML Fundamentals

Topics

Classification
Regression
Feature Engineering
Model Lifecycle
Module M2

MLflow

Topics

Experiment Tracking
Artifacts
Metrics

Labs

Deploy MLflow
Track Experiments
Module M3

SageMaker Training

Topics

Training Jobs
Containers

Labs

Train XGBoost
Train RandomForest
Module M4

Hyperparameter Tuning

Labs

SageMaker HPO
Module M5

Model Registry

Labs

Version Models
Promote Models
Module M6

Inference Endpoints

Labs

Deploy Model
Batch Inference
Module M7

Model Monitoring

Labs

Data Drift
Model Drift
MLOps Outcome

✅ SageMaker Engineer
 ✅ MLOps Engineer

Repository Structure
aws-ai-platform-engineering
│
├── 01-platform-bootstrap
│
├── 02-bedrock-chatbot
│
├── 03-eks-deployment
│
├── 04-cicd-platform
│
├── 05-custom-rag
│
├── 06-bedrock-knowledge-bases
│
├── 07-mcp-platform
│
├── 08-cloudops-agent
│
├── 09-observability-platform
│
├── 10-aiops-remediation
│
├── 11-mlflow
│
├── 12-sagemaker-training
│
├── 13-model-registry
│
├── 14-model-serving
│
├── 15-model-monitoring
│
├── docs
│
├── diagrams
│
└── README.md

Final Skills Gained

✅ AWS Platform Engineering
 ✅ Terraform
 ✅ Docker
 ✅ ECR
 ✅ EKS
 ✅ GitHub Actions
 ✅ Bedrock
 ✅ Claude
 ✅ OpenSearch
 ✅ RAG
 ✅ Knowledge Bases
 ✅ MCP
 ✅ Bedrock Agents
 ✅ CloudOps Agents
 ✅ CloudWatch
 ✅ Prometheus
 ✅ Grafana
 ✅ OpenTelemetry
 ✅ EventBridge
 ✅ Lambda Automation
 ✅ MLflow
 ✅ SageMaker
 ✅ Model Registry
 ✅ Model Monitoring
 ✅ AIOps
 ✅ MLOps
 ✅ LLMOps

This sequence is optimized for your background as a Kubernetes/Terraform engineer: Platform → Bedrock → RAG → MCP → Agents → Observability → AIOps → MLOps, so you get a working enterprise AI product very early and learn the theory while building.
