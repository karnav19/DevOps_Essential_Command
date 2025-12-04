# Grafana Loki Installation (Basic)

## Download binary (or use Docker/Helm)
```bash
wget https://github.com/grafana/loki/releases/latest/download/loki-linux-amd64.zip
unzip loki-linux-amd64.zip
sudo mv loki-linux-amd64 /usr/local/bin/loki
sudo chmod +x /usr/local/bin/loki
```

## Run with config file and systemd for production
Create `loki-config.yaml` then systemd unit to run `/usr/local/bin/loki -config.file=/etc/loki/loki-config.yaml`

## Tips
- Use Promtail or Fluent-bit to push logs to Loki; visualize logs in Grafana.
