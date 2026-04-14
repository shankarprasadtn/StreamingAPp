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

# Commands Used

## Git Commands
```bash
git clone https://github.com/UnpredictablePrashant/StreamingApp.git
cd StreamingApp
git status
git add .
git commit -m "Project updates"
git push origin main
```

## Docker Commands
```bash
docker build -t auth-service ./backend/authService
docker build -t chat-service ./backend/chatService
docker build -t admin-service ./backend/adminService
docker build -t streaming-service ./backend/streamingService
docker build -t streaming-frontend ./frontend
docker images
docker ps
```

## AWS / ECR Commands
```bash
aws configure
aws sts get-caller-identity
aws ecr create-repository --repository-name auth-service
aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin <account-id>.dkr.ecr.ap-south-1.amazonaws.com
```

## Kubernetes / EKS Commands
```bash
eksctl create cluster --name streaming-cluster-v2 --region ap-south-1 --nodes 2 --node-type t3.medium
kubectl get nodes
kubectl get pods
kubectl get svc
kubectl create deployment streaming-frontend --image=<account-id>.dkr.ecr.ap-south-1.amazonaws.com/streaming-frontend:latest
kubectl expose deployment streaming-frontend --type=LoadBalancer --port=80 --target-port=80
```

## Jenkins Commands
```bash
sudo apt update
sudo apt install openjdk-17-jdk -y
sudo apt install jenkins -y
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

## Cleanup Commands
```bash
eksctl delete cluster --region ap-south-1 --name streaming-cluster-v2
```

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

# Screenshots

## Application UI
**Application Home**
<img width="1916" height="1130" alt="Screenshot 2026-04-14 212030" src="https://github.com/user-attachments/assets/b30e933c-0986-4844-a52f-4da3eddf0e03" />

**Application Features** <img width="1919" height="1139" alt="Screenshot 2026-04-14 212040" src="https://github.com/user-attachments/assets/2cd5efb9-bf55-42ab-961c-5501aa1a210d" />

**Create Account** <img width="1910" height="1135" alt="Screenshot 2026-04-14 212050" src="https://github.com/user-attachments/assets/430d837a-860a-4896-99a5-81bd022ac425" />

**Streaming Steps** <img width="1919" height="1140" alt="Screenshot 2026-04-14 212104" src="https://github.com/user-attachments/assets/b2852ca8-6643-4995-9628-9e9706cdfbcf" />


## AWS EKS
**EKS Clusters** <img width="1819" height="922" alt="Screenshot 2026-04-14 212140" src="https://github.com/user-attachments/assets/66d0e381-9be8-49eb-8065-103d92053129" />

**EKS Cluster Details** <img width="1822" height="918" alt="Screenshot 2026-04-14 212204" src="https://github.com/user-attachments/assets/26c0bb50-f529-422a-932d-3e650ba85576" />


## AWS IAM / ECR
**IAM Users** <img width="1830" height="914" alt="Screenshot 2026-04-14 213055" src="https://github.com/user-attachments/assets/5cca5b67-6d77-4d91-a6da-1fcf0c013619" />

**IAM Permissions** <img width="1829" height="944" alt="Screenshot 2026-04-14 213119" src="https://github.com/user-attachments/assets/a5f2ddca-ffe3-4588-bc0b-ce76ab895951" />

**ECR Repositories** <img width="1832" height="1000" alt="Screenshot 2026-04-14 211725" src="https://github.com/user-attachments/assets/4fe6fc68-9b10-4c87-bc26-6ab60953da6c" />


## Jenkins CI/CD
**![Jenkins Unlock](Screenshot 2026-04-14 200922.png)
![Jenkins Job Status](Screenshot 2026-04-14 211556.png)
![Jenkins Build Details](Screenshot 2026-04-14 211620.png)
![Jenkins Console Output](Screenshot 2026-04-14 211640.png)
![Jenkins Build Success](Screenshot 2026-04-14 211649.png)**

## Kubernetes Validation
![kubectl get nodes](Screenshot 2026-04-14 211725.png)
![kubectl get pods](Screenshot 2026-04-14 211801.png)
![kubectl get svc](Screenshot 2026-04-14 211824.png)

---

# Conclusion

This project demonstrates practical DevOps implementation using Docker, Jenkins, Amazon ECR, Kubernetes, and Amazon EKS for scalable cloud-native deployment.

