# Grafana Installation (Ubuntu/Debian) — Step-by-step

## Overview
Grafana visualizes metrics from Prometheus, Loki, and others.

## 1) Prerequisites
```bash
sudo apt-get update
sudo apt-get install -y apt-transport-https software-properties-common wget
```

## 2) Add repository & install
```bash
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"
sudo apt update
sudo apt install -y grafana
sudo systemctl enable --now grafana-server
```

## 3) Firewall & access
```bash
sudo ufw allow 3000/tcp
```
Open http://<server-ip>:3000 (default admin/admin).

## 4) Tips
- Configure data sources (Prometheus) and dashboards.
- Secure with HTTPS via reverse proxy (NGINX).
