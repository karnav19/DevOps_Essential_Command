# Prometheus Installation (Standalone) — Step-by-step

## Overview
Prometheus scrapes metrics from exporters and stores time-series data.

## 1) Create user & download
```bash
sudo useradd --no-create-home --shell /bin/false prometheus
wget https://github.com/prometheus/prometheus/releases/latest/download/prometheus-*-linux-amd64.tar.gz
tar -xvf prometheus-*-linux-amd64.tar.gz
```

## 2) Move binaries & setup directories
```bash
sudo mv prometheus-*/prometheus /usr/local/bin/
sudo mv prometheus-*/promtool /usr/local/bin/
sudo mkdir -p /etc/prometheus /var/lib/prometheus
sudo mv prometheus-*/prometheus.yml /etc/prometheus/prometheus.yml
sudo chown -R prometheus:prometheus /etc/prometheus /var/lib/prometheus
sudo chown prometheus:prometheus /usr/local/bin/prometheus /usr/local/bin/promtool
```

## 3) systemd service
Create `/etc/systemd/system/prometheus.service` with ExecStart pointing to /usr/local/bin/prometheus --config.file=/etc/prometheus/prometheus.yml --storage.tsdb.path=/var/lib/prometheus
Then:
```bash
sudo systemctl daemon-reload
sudo systemctl enable --now prometheus
sudo systemctl status prometheus
```

## 4) Configure scrape targets
Edit `/etc/prometheus/prometheus.yml` and add exporters (node_exporter, app metrics).

## 5) Access
Open http://<server-ip>:9090
