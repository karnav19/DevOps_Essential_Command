# Promtail Installation (to send logs to Loki)

## Download
```bash
wget https://github.com/grafana/loki/releases/latest/download/promtail-linux-amd64.zip
unzip promtail-linux-amd64.zip
sudo mv promtail-linux-amd64 /usr/local/bin/promtail
sudo chmod +x /usr/local/bin/promtail
```

## Configure promtail to read /var/log and send to Loki, then run as systemd service.

## Tips
- For Kubernetes use the promtail DaemonSet via Helm.
