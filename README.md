# AKS-Microservices-App
# Building a Microservices App with Azure Kubernetes Service (AKS) & Minikube

This project demonstrates how to deploy a simple Flask-based microservices app using Docker, Kubernetes, and Azure Kubernetes Service (AKS). The app returns a “Hello, World!” message.

## 🔧 Tech Stack

- Azure Kubernetes Service (AKS)
- Docker
- Kubernetes (kubectl)
- Minikube (for local testing)
- Python & Flask

## ⚙️ Project Structure

AKS-Microservices-App/
├── app.py
├── Dockerfile
├── requirements.txt
├── deployment.yaml
├── service.yaml
├── .gitignore
└── README.md



## 🚀 Run Locally with Docker

```bash
docker build -t flask-app .
docker run -p 8080:80 flask-app
curl http://localhost:8080



🧪 Test with Minikube

minikube start --driver=docker
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
minikube service myservice



☁️ Deploy on AKS

az login
az group create --name myResourceGroup --location eastus
az aks create --resource-group myResourceGroup --name myAKSCluster --node-count 3 --enable-addons monitoring --generate-ssh-keys
az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml




Author
Ibne Sabid Saikat
Cloud Solution Architect | Microsoft Learn Student Ambassador
