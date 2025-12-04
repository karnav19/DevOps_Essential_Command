# Argo CD Installation (Kubernetes) — Step-by-step

## Install to cluster
```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

## Access UI
Expose argocd-server via port-forward or Service/Ingress:
```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
```
Login with initial admin password from `kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d`
