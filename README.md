# Monitoring

observability for Prometheus / Grafana Loki / Grafana Tempo / Grafana Alloy

## install cluster

Minikube (kubernetes v1.29)

### required

CPU: 6core
memory: 8G

### Minikube setting

```bash
minikube addons enable metrics-server
```

### start Minikube

```bash
minikube start --memory='9g' --cpus=6 --kubernetes-version=v1.29.4
```

## deploy tool

ArgoCD

### isntall ArgoCD

```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

## install monitoring

```bash
kubectl create ns monitoring
kubectl apply -f deploy/.
kubectl apply -f instrumentation/.
```
