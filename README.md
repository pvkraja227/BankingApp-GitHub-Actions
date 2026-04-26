# BankingApp-GitHub-Actions

# 🏦 Secure Banking Microservices Platform on AWS

## 📌 Overview

This project demonstrates a **production-grade banking application** built using a **microservices architecture** and deployed on AWS with end-to-end DevOps automation.

It showcases real-world DevOps practices including **CI/CD, Infrastructure as Code, containerization, Kubernetes orchestration, monitoring, and security (DevSecOps)**.

---

## 🚀 Key Features

* 🔐 Secure user authentication & secrets management
* 💸 Fund transfer & transaction processing (simulated)
* 📊 Real-time monitoring and logging
* 🔄 Fully automated CI/CD pipeline
* 🌍 Scalable and highly available architecture
* 🔁 Zero-downtime deployments

---

## 🏗️ Architecture

```
User → Load Balancer (ALB) → Kubernetes (EKS)
                                 ↓
        -----------------------------------------
        |        |         |         |           |
   User Service Payment Service Transaction Service Notification Service
                                 ↓
                             RDS (PostgreSQL)

CI/CD → GitHub Actions → Docker → ECR → EKS (Helm Deployments)
Monitoring → Prometheus + Grafana
Logging → CloudWatch
Security → IAM + Secrets Manager + Trivy
```

---

## 🛠️ Tech Stack

### ☁️ Cloud & Infrastructure

* AWS (EKS, EC2, S3, RDS, IAM, ALB, CloudWatch, ECR)

### ⚙️ DevOps Tools

* CI/CD: GitHub Actions
* Containerization: Docker
* Orchestration: Kubernetes (EKS)
* IaC: Terraform
* Config Management: Ansible

### 📊 Monitoring & Logging

* Prometheus
* Grafana
* AWS CloudWatch

### 🔐 Security (DevSecOps)

* IAM Roles (Least Privilege)
* AWS Secrets Manager
* Trivy (Image Scanning)

---

## 🔁 CI/CD Pipeline Flow

1. Developer pushes code to GitHub
2. GitHub Actions pipeline is triggered
3. Build Docker image
4. Scan image using Trivy
5. Push image to Amazon ECR
6. Deploy to EKS using Helm
7. Verify deployment (health checks)

---

## 📦 Project Structure

```
banking-app/
│
├── microservices/
│   ├── user-service/
│   ├── payment-service/
│   ├── transaction-service/
│   └── notification-service/
│
├── terraform/
│   ├── vpc/
│   ├── eks/
│   ├── rds/
│   └── iam/
│
├── k8s/
│   ├── deployments/
│   ├── services/
│   └── ingress/
│
├── helm-charts/
│
├── .github/workflows/
│
└── README.md
```

---

## 🔐 Security Implementation

* No hardcoded credentials (used AWS Secrets Manager)
* IAM roles with least privilege access
* Container image vulnerability scanning using Trivy
* Secure communication via HTTPS (ALB)

---

## 📊 Monitoring & Logging

* Application and infrastructure metrics using Prometheus
* Visualization dashboards using Grafana
* Logs centralized using AWS CloudWatch

---

## 🚀 Deployment Strategy

* Rolling updates for zero downtime
* Multi-environment setup (Dev, QA, Prod)
* Auto-scaling using Kubernetes

---

## 📈 Key Achievements

* Improved deployment reliability with automated CI/CD pipelines
* Enabled zero-downtime deployments using Kubernetes strategies
* Enhanced security posture with DevSecOps practices
* Built scalable infrastructure capable of handling high traffic

---

## 🧠 Learnings

* Hands-on experience with Kubernetes (EKS) in production-like setup
* Deep understanding of CI/CD automation using GitHub Actions
* Implemented Infrastructure as Code using Terraform
* Strengthened knowledge of monitoring, logging, and security

---
