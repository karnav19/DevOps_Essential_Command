# Kubernetes (kubectl + Minikube) — Step-by-step (Local dev)

## kubectl (client)
```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
kubectl version --client
```

## Minikube (single-node)
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
minikube start --driver=docker
minikube status
kubectl get nodes
```

## Tips
- For production, use kubeadm or managed services (EKS/GKE/AKS).
