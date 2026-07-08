# 🚀 Deploy Three-Tier DevSecOps Kubernetes Project on AWS EKS

## 📖 Project Overview

This project demonstrates an end-to-end **Three-Tier DevSecOps CI/CD pipeline** deployed on **AWS EKS (Elastic Kubernetes Service)**. It automates the build, security scanning, containerization, deployment, monitoring, and GitOps workflow using industry-standard DevOps tools.

The application follows a **three-tier architecture** consisting of a frontend, backend, and database. The complete deployment pipeline is automated using **Jenkins**, while **Argo CD** continuously synchronizes Kubernetes manifests from GitHub to the EKS cluster. Security is integrated into the pipeline using vulnerability scanning, and application monitoring is implemented with **Prometheus** and **Grafana** for real-time metrics and visualization.

## 🎯 Project Objectives

- Build an automated DevSecOps CI/CD pipeline.
- Deploy a Three-Tier application on AWS EKS.
- Implement GitOps using Argo CD.
- Automate Docker image build and deployment.
- Monitor application and cluster health with Prometheus and Grafana.
- Improve deployment reliability, scalability, and security.

## 🛠️ Technologies Used

- AWS EC2
- AWS EKS
- Docker
- Kubernetes
- Jenkins
- Argo CD
- Prometheus
- Grafana
- Git & GitHub
- Helm
- Python / Node.js (Application)
- Trivy (Security Scanning)

## 🔄 CI/CD & GitOps Workflow

1. Developer pushes code to GitHub.
2. Jenkins automatically triggers the CI/CD pipeline.
3. Source code is built and tested.
4. Docker image is created.
5. Trivy scans the Docker image for vulnerabilities.
6. Docker image is pushed to Docker Hub.
7. Kubernetes manifests are updated.
8. Argo CD detects changes from GitHub and syncs them to AWS EKS.
9. The application is deployed to the Kubernetes cluster.
10. Prometheus collects application and cluster metrics.
11. Grafana visualizes dashboards for monitoring and alerting.

## 📂 Project Components

- Frontend
- Backend
- Database
- Jenkins Pipeline
- Dockerfile
- Kubernetes Manifests
- Helm Charts
- Argo CD Configuration
- Prometheus Monitoring
- Grafana Dashboards

## ✨ Key Features

- End-to-End DevSecOps Pipeline
- Three-Tier Architecture
- AWS EKS Deployment
- Automated CI/CD with Jenkins
- GitOps Deployment with Argo CD
- Container Security Scanning using Trivy
- Real-Time Monitoring with Prometheus
- Interactive Dashboards using Grafana
- Scalable and Highly Available Kubernetes Deployment

## 🏗️ Architecture

Developer
     │
     ▼
GitHub Repository
     │
     ▼
Jenkins CI Pipeline
     │
     ├── Build
     ├── Test
     ├── Trivy Scan
     ├── Docker Build
     └── Push to Docker Hub
                 │
                 ▼
      Update Kubernetes Manifests
                 │
                 ▼
             Argo CD
                 │
                 ▼
            AWS EKS Cluster
                 │
      ┌──────────┼──────────┐
      ▼          ▼          ▼
 Frontend    Backend    Database
                 │
                 ▼
        Prometheus Monitoring
                 │
                 ▼
        Grafana Dashboards

## 📈 Benefits

- Fully Automated CI/CD Pipeline
- GitOps-Based Continuous Deployment
- Secure Container Image Scanning
- High Availability with Kubernetes
- Scalable Cloud-Native Architecture
- Centralized Monitoring and Observability
- Faster and Reliable Software Delivery

## 👨‍💻 Author

**Vishnu Saratthi**

**DevOps Engineer | AWS | Kubernetes | Jenkins | Docker | Argo CD | Prometheus | Grafana | Terraform**
