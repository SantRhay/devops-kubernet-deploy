# DevOps Kubernetes Deploy

Projeto de deploy de aplicação containerizada utilizando Kubernetes.

## Tecnologias utilizadas

- Docker
- Kubernetes
- Nginx
- kubectl
- GitHub Codespaces

## Arquitetura

Application Container → Deployment → Pods → Service NodePort

## Arquivos do projeto

deployment.yaml
service.yaml

## Comandos utilizados

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

kubectl get pods
kubectl get services

## Resultado

Aplicação nginx rodando no Kubernetes e acessível via NodePort.

Projeto desenvolvido para estudo de DevOps e Cloud Computing.