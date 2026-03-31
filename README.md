# 🚀 CI/CD Pipeline Project – Jenkins + SonarQube + Docker + GitHub + Nginx

## 📌 Project Overview

This project showcases an end-to-end CI/CD pipeline leveraging Jenkins and SonarQube deployed in Docker containers. The pipeline automates code integration, quality analysis, containerization, and deployment of an Nginx application to AWS EC2. It uses GitHub webhooks for event-driven execution, ensuring fast, consistent, and automated application delivery.
---

## 🏗️ Architecture

GitHub Repository → Jenkins Pipeline → SonarQube Code Analysis → Docker Image Build → Nginx Container Deployment

---

## 🛠️ Technologies Used

* Jenkins (Docker container)
* SonarQube (Docker container)
* Docker & Docker Compose
* GitHub Webhooks
* Nginx Web Server
* Linux / WSL environment
* AWS EC2

---

## ⚙️ Setup Steps

### 1️⃣ Jenkins & SonarQube Setup

* Used Docker Compose to run Jenkins and SonarQube containers.
* Configured persistent volumes for data storage.
* Installed required Jenkins plugins:

  * SonarQube Scanner
  * Git Plugin
  * Pipeline Plugin

---

### 2️⃣ SonarQube Integration

* Added SonarQube server configuration in Jenkins.
* Generated authentication token.
* Configured scanner tool in Jenkins.

---

### 3️⃣ GitHub Integration

* Created GitHub repository for Nginx website.
* Added webhook to trigger Jenkins automatically on code push.

---

### 4️⃣ Pipeline Workflow

The pipeline automates the complete application lifecycle through the following stages:

- Checkout latest source code from GitHub  
- Perform static code analysis using SonarQube  
- Build and tag Docker image  
- Push image to Docker Hub registry  
- Deploy application to AWS EC2 via SSH:
  - Pull latest image from Docker Hub  
  - Replace existing container with updated version  
  - Run Nginx container and expose application on port 80  
---

### 5️⃣ Website Deployment

- Created a Dockerfile using the official Nginx base image  
- Configured the container to serve the static website content  
- Automated deployment of the Nginx container on AWS EC2 after successful pipeline execution  
- Application is exposed on port 80 and accessible via EC2 public IP  

---

## 📊 Outcome

- Successfully implemented an end-to-end automated CI/CD pipeline  
- Integrated static code analysis using SonarQube  
- Achieved seamless Docker-based application deployment to AWS EC2  
- Reduced manual intervention through pipeline automation  

---

## 💡 Key Learnings

- Implemented end-to-end CI/CD pipeline automation using Jenkins  
- Set up a containerized DevOps environment using Docker  
- Configured Docker networking for seamless communication between services  
- Integrated GitHub webhooks for automated pipeline triggering  
- Performed static code analysis using SonarQube  
- Built and pushed Docker images to Docker Hub  
- Automated application deployment to AWS EC2 using SSH  
---
## 🧱 Architecture Diagram

```mermaid
flowchart LR
    A[Developer] -->|Push Code| B[GitHub Repository]
    B -->|Webhook Trigger| C[Jenkins Pipeline]

    C --> D[SonarQube Analysis]
    D --> E[Docker Build]

    E --> F[Docker Hub]
    F -->|Pull Image| G[AWS EC2 Instance]

    G --> H[Docker Container - Nginx]
    H --> I[End User - Browser]
---
## 🚀 Future Improvements

- Implement Kubernetes-based deployment (Minikube / AWS EKS)  
- Automate infrastructure provisioning using Terraform  
- Configure HTTPS using Nginx reverse proxy and SSL certificates  
- Integrate monitoring and logging using Prometheus and Grafana  
- Implement CI/CD pipeline for Kubernetes deployments  

---

## 👨‍💻 Author

Afzal KH – DevOps Learner

