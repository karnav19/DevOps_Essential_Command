# Elasticsearch (OSS) Installation — Step-by-step (Debian/Ubuntu)

## 1) Install Java (if required by version)
```bash
sudo apt update
sudo apt install -y openjdk-11-jdk
```

## 2) Download & install deb
```bash
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.9.0-amd64.deb
sudo dpkg -i elasticsearch-8.9.0-amd64.deb
```

## 3) Enable & start
```bash
sudo systemctl daemon-reload
sudo systemctl enable --now elasticsearch
sudo systemctl status elasticsearch
```

## 4) Post-install
- Configure `/etc/elasticsearch/elasticsearch.yml` for cluster settings.
- Secure with TLS & auth for production.
