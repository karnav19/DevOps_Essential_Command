# Node Exporter (Prometheus) — Step-by-step

## Download & install
```bash
wget https://github.com/prometheus/node_exporter/releases/latest/download/node_exporter-*-linux-amd64.tar.gz
tar -xvf node_exporter-*-linux-amd64.tar.gz
sudo mv node_exporter-*/node_exporter /usr/local/bin/
sudo useradd --no-create-home --shell /bin/false nodeusr || true
sudo chown nodeusr:nodeusr /usr/local/bin/node_exporter
```

## systemd service
Create `/etc/systemd/system/node_exporter.service` and enable it.

## Tips
- Add scrape target to Prometheus: `<host>:9100`
