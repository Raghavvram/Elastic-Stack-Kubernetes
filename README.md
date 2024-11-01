# Elastic-Stack-Kubernetes
Deploying a ELK ( ElasticSearch, LogStash, Kibana Dashboard) stack with filebeat in Kubernetes.

### Initial Setup

Docker Desktop is setup with Kubernetes. [Official Docker Documentation](https://docs.docker.com/desktop/kubernetes/)
Kubectl is installed.
Helm package manager is also installed and configured.

---

### Installation
```
kubectl create namespace elastic-stack
kubectl apply -f elasticsearch-ss.yaml
kubectl get pods -n elastic-stack
kubectl apply -f logstash-deployment.yaml
kubectl apply -f filebeat-ds.yaml
kubectl apply -f kibana-deployment.yaml
kubectl get pods -n elastic-stack -o wide --watch
```
---
