# 🚀 Ammax Deployment (GitOps CI/CD Platform)

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![CI](https://img.shields.io/badge/CI-Jenkins-red)]()
[![CD](https://img.shields.io/badge/CD-ArgoCD-orange)]()
[![Docker](https://img.shields.io/badge/Docker-Containerized-blue)]()
[![Kubernetes](https://img.shields.io/badge/Kubernetes-Enabled-blue)]()

---

## 📌 Overview

The **Ammax Deployment** project is a production-grade **GitOps-based CI/CD system** designed for automated deployment of a MERN application using **Jenkins, Docker, Kubernetes, and ArgoCD**.

This architecture follows modern DevOps practices used in scalable cloud environments.

---

## 🏗 Full System Flow

```text
GitHub (Source Code)
        ↓
Jenkins CI Pipeline
        ↓
Docker Build (Backend + Frontend Images)
        ↓
Docker Registry (Push Images)
        ↓
GitOps Repo Update (Kubernetes Manifests)
        ↓
ArgoCD Sync
        ↓
Kubernetes Cluster Deployment
```

---

## 📊 Architecture Diagram

![Architecture](https://res.cloudinary.com/dqjjreavg/image/upload/v1779388076/pd2j1btkg5ued7dgevxy.png)

---

## ⚙️ CI/CD Pipeline

The Jenkins pipeline automates the full delivery process:

### 🔹 Stages

* ✔ Checkout Source Code
* ✔ Generate Build Tag (Git Commit SHA)
* ✔ Build Docker Images (Backend + Frontend)
* ✔ Push Images to Docker Registry
* ✔ Update GitOps Repository
* ✔ Trigger ArgoCD Sync

![Jenkins Pipeline](https://res.cloudinary.com/dqjjreavg/image/upload/v1779388090/ji1kd57hyrii2aljvwu0.jpg)

---

## 🔄 ArgoCD (GitOps Layer)

ArgoCD continuously monitors the GitOps repository and automatically deploys changes to Kubernetes.

```text
GitOps Repo → ArgoCD → Kubernetes Cluster
```

![ArgoCD](https://res.cloudinary.com/dqjjreavg/image/upload/v1779388085/e0vg0y7mhirggcvesq7f.jpg)

---

## ☸️ Kubernetes Features

* Deployments (Frontend + Backend)
* Services (ClusterIP / LoadBalancer)
* Ingress Controller
* ConfigMaps
* Secrets Management
* HPA (Horizontal Pod Autoscaler)
* VPA (Vertical Pod Autoscaler)

---

## 📊 Monitoring

* Prometheus → Metrics collection
* Grafana → Dashboards & visualization
* Node Exporter → System-level metrics

![Monitoring](https://res.cloudinary.com/dqjjreavg/image/upload/v1779388095/c5o9to6oyrj1ackeavxt.jpg)

---

## 🧱 Repository Structure

```bash
.
├── argocd/
│   └── main.yml
├── jenkins/
│   └── Jenkinsfile
├── k8s/
│   ├── backend-deployment.yml
│   ├── frontend-deployment.yml
│   ├── service.yml
│   ├── ingress.yml
│   ├── configmap.yml
│   ├── secret.yml
│   ├── hpa.yml
│   ├── vpa.yml
├── docs/
│   └── images/
│       ├── architecture.png
│       ├── jenkins.png
│       ├── argocd.png
│       ├── monitoring.png
└── README.md
```

---

## 🚀 Getting Started

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/ammax-deployment.git
cd ammax-deployment
```

---

### 2️⃣ Configure ArgoCD

Update `argocd/main.yml` with your Git repository URL.

---

### 3️⃣ Setup Jenkins

* Import Jenkins pipeline from `/jenkins`
* Add credentials:

  * Docker Registry credentials
  * GitHub token

---

### 4️⃣ Deploy Application

```bash
argocd app sync ammax-app
```

---

## 🔐 Security Best Practices

❌ Never store secrets in Git
❌ Never hardcode passwords in YAML

✔ Use:

* Kubernetes Secrets
* Jenkins Credentials Store
* Docker Registry Authentication

---

## ⭐ Key Highlights

* 🚀 Fully automated CI/CD pipeline
* 🔄 GitOps-based deployment model
* 🐳 Dockerized microservices
* ☸️ Scalable Kubernetes architecture
* 📊 Monitoring with Grafana & Prometheus
* 🔐 Secure secret management

---

## 🧠 Tech Stack

* Frontend: React.js
* Backend: Node.js / Express
* Database: MongoDB
* CI/CD: Jenkins
* GitOps: ArgoCD
* Containers: Docker
* Orchestration: Kubernetes
* Monitoring: Prometheus + Grafana

---

## 📸 Screenshots

| Jenkins                             | ArgoCD                            | Monitoring                                |
| ----------------------------------- | --------------------------------- | ----------------------------------------- |
| ![Jenkins](https://res.cloudinary.com/dqjjreavg/image/upload/v1779388090/ji1kd57hyrii2aljvwu0.jpg) | ![ArgoCD](https://res.cloudinary.com/dqjjreavg/image/upload/v1779388085/e0vg0y7mhirggcvesq7f.jpg) | ![Monitoring](https://res.cloudinary.com/dqjjreavg/image/upload/v1779388095/c5o9to6oyrj1ackeavxt.jpg) |

---

## 🎯 Outcome

This project demonstrates:

✔ Real-world DevOps CI/CD pipeline
✔ Production-ready Kubernetes deployment
✔ GitOps automation with ArgoCD
✔ Scalable microservices architecture

---

## 👨‍💻 Author

**Rajeel Siddiqui**
DevOps & Frontend Developer

---

🔥 Bas ab isko paste karo GitHub me — ye **100% professional DevOps portfolio README** hai.
