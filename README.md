# 🗳️ Kubernetes Voting App (Simple Version)

A simple Kubernetes-based microservices project that deploys a classic **Voting App** with frontend, backend, worker, Redis, and PostgreSQL — all managed via individual Deployments and Services.  
Perfect for showcasing container orchestration skills **without an Ingress controller**, using only `NodePort` or `minikube service`.

---

| Component  | Technology    | Purpose                  |
| ---------- | ------------- | ------------------------ |
| **vote**   | Python Flask  | Frontend voting app      |
| **result** | Node.js       | Results display page     |
| **worker** | .NET / Python | Background job processor |
| **redis**  | Redis         | Message queue            |
| **db**     | PostgreSQL    | Data storage             |


- **`deployments/`** → Kubernetes Deployments (recommended over raw Pods)
- **`pod-manifests/`** → Raw Pod YAMLs (for manual testing/learning; not for production)
- **`services/`** → ClusterIP or NodePort Services for each component

---

## 🚀 Getting Started

### 1️⃣ Start Minikube
```bash
minikube start

2️⃣ Apply Deployments and Services
(Only use deployments/ and services/; ignore pod-manifests/ unless testing manually.)

kubectl apply -f deployments/
kubectl apply -f services/

3️⃣ Access the Frontend App
Expose the vote service:
minikube service vote

This will open a URL like:
http://127.0.0.1:<random-port>

🧹 Clean Up
To remove everything:
kubectl delete -f deployments/
kubectl delete -f services/

To stop Minikube:
minikube stop

🧠 Why This Project?
Practice Kubernetes basics

Understand Deployments, Pods, and Services

Learn local DevOps with Minikube

Showcase Kubernetes skills in your GitHub portfolio
