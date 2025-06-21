# 🚀 AKS Microservices App with Flask, Docker & Minikube

This project demonstrates how to build, containerize, and deploy a simple **Flask-based microservices app** using **Docker**, **Kubernetes**, and **Azure Kubernetes Service (AKS)**. It also includes local testing using **Minikube**.

---

## 📌 Features

- ✅ Microservices architecture with Flask
- 🐳 Docker containerization
- ☸️ Kubernetes deployment using `kubectl`
- 🔁 Local testing using Minikube
- ☁️ Full deployment to Azure Kubernetes Service (AKS)

---

## 🧰 Tech Stack

- Python 3.8
- Flask
- Docker
- Kubernetes (kubectl)
- Minikube
- Azure CLI & AKS

---

## 🗂️ Project Structure

AKS-Microservices-App/
├── app.py # Flask app
├── Dockerfile # Docker config
├── requirements.txt # Python dependencies
├── deployment.yaml # Kubernetes Deployment config
├── service.yaml # Kubernetes Service config
├── .gitignore
└── README.md






---

## ⚙️ Getting Started

### 1. Run Locally with Docker

```bash
docker build -t flask-app .
docker run -p 8080:80 flask-app
curl http://localhost:8080





2. Test Locally with Minikube

minikube start --driver=docker
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
minikube service myservice





☁️ Deploy to Azure Kubernetes Service (AKS)
Step-by-Step:

az login
az group create --name myResourceGroup --location eastus
az aks create --resource-group myResourceGroup --name myAKSCluster --node-count 3 --enable-addons monitoring --generate-ssh-keys
az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml




Expected Output
When accessing the service endpoint:

Hello, World!




Author
Ibne Sabid Saikat
Cloud Solution Architect | Microsoft Learn Student Ambassador
🔗 LinkedIn | AZ-104 | AZ-305

