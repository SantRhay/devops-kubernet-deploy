# 🚀 DevOps CI/CD Pipeline com Docker, Kubernetes, GitHub Actions e AWS

![Docker](https://img.shields.io/badge/docker-container-blue)
![Kubernetes](https://img.shields.io/badge/kubernetes-orchestration-blue)
![GitHub Actions](https://img.shields.io/badge/github--actions-ci%2Fcd-orange)
![AWS](https://img.shields.io/badge/aws-ec2-yellow)

Este projeto demonstra a construção de um *pipeline DevOps completo* automatizando o deploy de uma aplicação containerizada utilizando Docker, Kubernetes, GitHub Actions e AWS.

---

# 📌 Arquitetura do Projeto

Fluxo do pipeline:

Developer push code  
↓  
GitHub Repository  
↓  
GitHub Actions CI/CD  
↓  
Build Docker Image  
↓  
Push DockerHub  
↓  
SSH AWS EC2  
↓  
Deploy Kubernetes  
↓  
Application Running

---

# 🧰 Tecnologias Utilizadas

Docker  
Kubernetes  
GitHub Actions  
AWS EC2  
Nginx  

---

# 📂 Estrutura do Projeto

devops-kubernetes-deploy

app/  
&nbsp;&nbsp;&nbsp;&nbsp;index.html  

docker/  
&nbsp;&nbsp;&nbsp;&nbsp;Dockerfile  

k8s/  
&nbsp;&nbsp;&nbsp;&nbsp;deployment.yaml  
&nbsp;&nbsp;&nbsp;&nbsp;service.yaml  

.github/workflows/  
&nbsp;&nbsp;&nbsp;&nbsp;deploy.yml  

README.md

---

# ⚙️ Pipeline CI/CD

O pipeline executa automaticamente sempre que um commit é enviado ao repositório.

Etapas do pipeline:

1. Checkout do código
2. Build da imagem Docker
3. Push da imagem para DockerHub
4. Conexão SSH na EC2
5. Deploy no Kubernetes

---

# 🐳 Docker

Build da imagem

docker build -t usuario/devops-web .

Rodar container local

docker run -p 8080:80 usuario/devops-web

---

# ☸️ Kubernetes

Aplicar deployment

kubectl apply -f k8s/deployment.yaml

Aplicar service

kubectl apply -f k8s/service.yaml

Verificar pods

kubectl get pods

Verificar services

kubectl get svc

---

# 🌐 Acesso à Aplicação

Após o deploy a aplicação pode ser acessada em:

http://IP_DA_EC2:30007

---

# 📊 Comandos úteis Kubernetes

kubectl get pods  
kubectl get svc  
kubectl get deployments  
kubectl describe pod NOME  
kubectl logs NOME  

---

# ⚠️ Problemas comuns

NodePort já utilizado

Erro:

provided port is already allocated

Solução:

kubectl delete service devops-web-service

---

kubectl command not found

Executar dentro da EC2 ou instalar kubectl.

---

# 📈 Fluxo CI/CD

Commit no GitHub  
↓  
GitHub Actions executa pipeline  
↓  
Build Docker Image  
↓  
Push DockerHub  
↓  
SSH EC2  
↓  
kubectl apply  
↓  
Deploy Kubernetes  

---

# 🎯 Objetivo do Projeto

Demonstrar habilidades práticas em:

DevOps  
CI/CD  
Docker  
Kubernetes  
Cloud Computing  

---

# 👨‍💻 Autor
Rayane Santana

Projeto desenvolvido para estudo e prática de DevOps e automação de deploy.
