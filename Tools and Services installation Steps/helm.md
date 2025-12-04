# Helm Installation & Basic Usage

## Install Helm
```bash
curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash
helm version
```

## Add repo & install chart
```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm install my-nginx bitnami/nginx
```

## Tips
- Use values.yaml to configure charts; manage releases with `helm upgrade`.
