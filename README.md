# 🚀 DevOps Kubernetes Deploy

Projeto prático de deploy de aplicação containerizada utilizando Kubernetes.

Este projeto demonstra como realizar o deploy de um container *Nginx* em um cluster Kubernetes utilizando *Deployment, **Service* e *Horizontal Pod Autoscaler (HPA)*.

O objetivo é demonstrar conceitos fundamentais de *DevOps, **orquestração de containers* e *infraestrutura como código*.

---

# 📦 Tecnologias utilizadas

- Kubernetes
- Docker
- Nginx
- kubectl
- GitHub
- GitHub Actions
- GitHub Codespaces

---

# 🏗 Arquitetura do Projeto

Usuário  
↓  
Service (NodePort)  
↓  
Pods Kubernetes  
↓  
Container Nginx  

O Kubernetes gerencia automaticamente:

- criação dos containers
- balanceamento de carga
- escalabilidade
- auto recuperação

---

# 📁 Estrutura do projeto


devops-kubernet-deploy
│
├── deployment.yaml
├── service.yaml
├── README.md
└── .github
    └── workflows
        └── deploy.yml


---

# ⚙️ Como executar o projeto

## 1️⃣ Criar cluster Kubernetes


kind create cluster


---

## 2️⃣ Aplicar Deployment


kubectl apply -f deployment.yaml


---

## 3️⃣ Criar Service


kubectl apply -f service.yaml


---

## 4️⃣ Verificar pods


kubectl get pods


Resultado esperado:


devops-web-xxxxx   Running


---

## 5️⃣ Verificar serviços


kubectl get services


---

## 6️⃣ Acessar aplicação


kubectl port-forward service/devops-service 8080:80


Abrir no navegador:


http://localhost:8080


---

# 📈 Escalabilidade

Escalar manualmente a aplicação:


kubectl scale deployment devops-web --replicas=4


Verificar pods:


kubectl get pods


---

# ⚡ Autoscaling (HPA)

Criar autoscaling baseado em CPU:


kubectl autoscale deployment devops-web --cpu-percent=50 --min=2 --max=10


Verificar autoscaler:


kubectl get hpa


---

# 🔁 Self-Healing

O Kubernetes recria automaticamente pods que falham.

Exemplo:


kubectl delete pod NOME_DO_POD


O Kubernetes cria um novo pod automaticamente.

---

# ⚙️ CI/CD com GitHub Actions

O projeto utiliza *GitHub Actions* para validar os arquivos Kubernetes automaticamente sempre que houver push no repositório.

Pipeline:


GitHub
   ↓
GitHub Actions
   ↓
Validação dos arquivos Kubernetes


---

# 🎯 Conceitos DevOps aplicados

Este projeto demonstra:

- Containerização
- Orquestração de containers
- Deploy automatizado
- Escalabilidade horizontal
- Alta disponibilidade
- Infraestrutura como código

---

# 📊 Comandos úteis

Ver pods


kubectl get pods


Ver deployments


kubectl get deployments


Ver serviços


kubectl get services


Ver autoscaling


kubectl get hpa


---

# 🚀 Melhorias futuras

- Deploy automatizado com DockerHub
- Monitoramento com Prometheus
- Dashboard Kubernetes
- Ingress Controller
- Observabilidade com Grafana

---

# 👨‍💻 Autor
Rayane Santana

Projeto desenvolvido como parte de estudos em *DevOps e Kubernetes*