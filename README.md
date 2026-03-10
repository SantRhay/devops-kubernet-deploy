kubectl# Deploy de Aplicação Containerizada com Kubernetes

Projeto de deploy de aplicação containerizada utilizando Kubernetes.

## Tecnologias utilizadas

- Docker
- Kubernetes
- Nginx
- kubectl
- GitHub Codespaces

## Arquitetura

Usuário
 ↓
Service (NodePort)
 ↓
Deployment
 ↓
Pods
 ↓
Container (Nginx)

## Arquivos do projeto

deployment.yaml
service.yaml

## Comandos utilizados

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

kubectl get pods
kubectl get services

## Resultado

A aplicação nginx foi implantada com sucesso em um cluster Kubernetes.

O serviço foi exposto utilizando NodePort, permitindo acesso externo à aplicação.

Projeto desenvolvido para prática de conceitos DevOps e orquestração de containers
