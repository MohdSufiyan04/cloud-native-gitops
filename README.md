🚀 Cloud Native GitOps Platform

This repository contains Kubernetes deployment configurations used to deploy the Spring Boot application into a Kubernetes cluster using Argo CD.

This repository follows GitOps principles where Kubernetes manifests are stored in Git and Argo CD continuously manages the desired application state.

🏗️ GitOps Deployment Flow
CI/CD Repository
        |
        |
        v
 Docker Image (Docker Hub)
        |
        |
        v
 GitOps Repository
        |
        |
        v
      Argo CD
        |
        |
        v
 Kubernetes Cluster
        |
        |
        v
 Spring Boot Application Pods
 
🛠️ Technologies Used
Technology	Purpose
Kubernetes	Container orchestration
Argo CD	GitOps continuous deployment
Docker Hub	Container image registry
YAML	Kubernetes configuration
📂 Repository Structure
cloud-native-gitops

│
└── spring-boot-app
    │
    ├── deployment.yml
    └── service.yml
    
☸️ Kubernetes Configuration
Deployment (deployment.yml)

Defines how the Spring Boot application runs inside Kubernetes.

It manages:
Application pods
Container image configuration
Replica count
Pod lifecycle
Service (service.yml)

Provides networking for the application inside Kubernetes.

It manages:
Stable application endpoint
Pod communication
Service exposure

🔄 Argo CD Workflow
Git Push
   |
   v
GitOps Repository
   |
   v
Argo CD Detects Changes
   |
   v
Application Sync
   |
   v
Kubernetes Updated State

📊 Monitoring

The deployed application is monitored using:
Prometheus
Grafana
Alertmanager

Monitoring provides visibility into:
Kubernetes resources
Pod health
CPU and memory usage
