# 🗳️ Kubernetes Voting App (Simple Version)

A simple Kubernetes-based microservices project that deploys a classic **Voting App** with frontend, backend, worker, Redis, and PostgreSQL — all managed via individual Deployments and Services.  
Perfect for showcasing container orchestration skills **without an Ingress controller**, using only `NodePort` or `minikube service`.

---

## 📁 Project Structure

KUBERNETES/
├── deployments/
│ ├── db-deployment.yaml
│ ├── redis-deployment.yaml
│ ├── result-deployment.yaml
│ ├── vote-deployment.yaml
│ └── worker-deployment.yaml
│
├── pod-manifests/
│ ├── db-pod.yaml
│ ├── redis-pod.yaml
│ ├── result-app-pod.yaml
│ ├── voting-app-pod.yaml
│ └── worker-pod.yaml
│
└── services/
├── db-service.yaml
├── redis-service.yaml
├── result-service.yaml
└── vote-service.yaml