# 🚀 CI/CD Pipeline Project – Jenkins + SonarQube + Docker + GitHub + Nginx

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline using Jenkins and SonarQube running in Docker containers.
The pipeline automatically builds, analyzes, and deploys an Nginx website whenever code is pushed to GitHub.

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

Pipeline stages:

* Source code checkout from GitHub
* Static code analysis using SonarQube
* Docker image build
* Automatic deployment of Nginx website container

---

### 5️⃣ Website Deployment

* Dockerfile created using Nginx base image.
* Website deployed automatically after successful pipeline execution.

---

## 📊 Outcome

* Automated CI/CD pipeline implemented successfully.
* Code quality analysis integrated.
* Website deployment fully automated.

---

## 💡 Key Learnings

* CI/CD pipeline automation using Jenkins
* Containerized DevOps environment setup
* Docker networking between services
* GitHub webhook integration
* Code quality analysis with SonarQube

---

## 🚀 Future Improvements

* Add Docker Hub image push
* AWS EC2 deployment
* HTTPS with reverse proxy
* Monitoring and logging setup

---

## 👨‍💻 Author

Afzal KH – DevOps Learner

