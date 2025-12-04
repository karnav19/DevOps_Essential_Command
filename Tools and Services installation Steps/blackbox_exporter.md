# Blackbox Exporter — Step-by-step

## Download & install (binary)
```bash
wget https://github.com/prometheus/blackbox_exporter/releases/latest/download/blackbox_exporter-*-linux-amd64.tar.gz
tar -xvf blackbox_exporter-*-linux-amd64.tar.gz
sudo mv blackbox_exporter-*/blackbox_exporter /usr/local/bin/
```

## Configure probes in config file and add to Prometheus scrape configs.

## Tips
- Use to probe endpoints (HTTP, TCP, ICMP) from Prometheus.
