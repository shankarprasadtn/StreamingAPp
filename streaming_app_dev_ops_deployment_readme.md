# StreamingApp DevOps Deployment Project

# Project Overview

This project demonstrates end-to-end orchestration, CI/CD automation, containerization, and scalable deployment of a MERN-based microservices application using AWS and DevOps tools.

The application was containerized, integrated with Jenkins CI/CD, stored in Amazon ECR, and deployed to Amazon EKS using Kubernetes.

---

# Tech Stack

- Frontend: React.js
- Backend: Node.js / Express.js
- Architecture: Microservices
- Containerization: Docker
- CI/CD: Jenkins
- Container Registry: Amazon ECR
- Orchestration: Kubernetes (Amazon EKS)
- Package Manager: Helm
- Monitoring: Amazon CloudWatch
- Cloud Provider: AWS

---

# Microservices Used

- auth-service
- chat-service
- admin-service
- streaming-service
- streaming-frontend

---

# Implementation Steps

## Step 1: Source Code Management
- Forked / cloned the project repository from GitHub.
- Managed project source code using Git.

## Step 2: Dockerization
Created Docker images for all services.

## Step 3: Amazon ECR Setup
Created repositories in Amazon ECR and pushed images.

## Step 4: Jenkins CI/CD Pipeline
Pipeline stages:
- Clone Source Code
- Build Docker Images
- Authenticate with ECR
- Push Images to ECR

## Step 5: Kubernetes Deployment using Amazon EKS
Created EKS cluster and verified worker nodes.

## Step 6: Application Exposure
Frontend exposed using LoadBalancer and validated in browser.

---

# Validation Completed

- Jenkins pipeline executed successfully
- Docker images built successfully
- Images pushed to ECR
- EKS cluster created successfully
- Pods running successfully
- Services exposed successfully
- Application accessible in browser

---

# Conclusion

This project demonstrates practical DevOps implementation using Docker, Jenkins, Amazon ECR, Kubernetes, and Amazon EKS for scalable cloud-native deployment.