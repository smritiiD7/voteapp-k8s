# 🗳️ Kubernetes Voting App (Simple Version)

This is a simple Kubernetes-based microservices project that deploys a classic **Voting App** with frontend, backend, worker, Redis, and PostgreSQL — all managed via individual deployments and services. Perfect for showcasing container orchestration skills with **no Ingress controller**, just `NodePort` or `minikube service`.

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

yaml
Copy
Edit

- **deployments/**: YAML files for Kubernetes Deployments (recommended over raw pods)
- **pod-manifests/**: Raw Pod YAMLs (for manual testing/learning; not used in production)
- **services/**: ClusterIP or NodePort Services for each component

---

## 🚀 Getting Started

### 1. Start Minikube
```bash
minikube start
2. Apply Deployments and Services
Apply only the deployments/ and services/ (ignore pod-manifests/ unless you're testing Pods manually):


kubectl apply -f deployments/
kubectl apply -f services/
3. Access the Frontend App
Use Minikube to expose the vote service:


minikube service vote
This will give you a URL like:

cpp
Copy
Edit
http://127.0.0.1:<some-random-port>
Click that URL to open the voting app in your browser.

🔧 Notes
This app consists of 5 components:

vote (Python Flask frontend)

result (Node.js results page)

worker (background job processor)

redis (queue)

db (PostgreSQL)

Communication is handled via internal Kubernetes networking using ClusterIP services.

🧹 Clean Up
To remove everything:

kubectl delete -f deployments/
kubectl delete -f services/

To stop Minikube:

minikube stop
🧠 Why This Project?
This setup is ideal for:

Practicing Kubernetes basics

Understanding Deployments, Pods, and Services

Local DevOps learning using Minikube

GitHub portfolio to showcase K8s understanding

📬 License
MIT License

Feel free to fork, star, and build on top of this.


Let me know if you want:
- ✨ A badge section
- 📸 Screenshots
- 📦 A version with Dockerfiles and CI/CD for GitHub Actions
- 🌀 A pro version with Ingress & TLS

Good luck publishing this — it’s gonna look awesome on GitHub! 🚀








