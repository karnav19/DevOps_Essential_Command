# Logstash Installation — Step-by-step

## Install
```bash
sudo apt update
sudo apt install -y logstash
```

## Configure pipeline
Create `/etc/logstash/conf.d/your-pipeline.conf` with input/filter/output and restart.

## Start & enable
```bash
sudo systemctl enable --now logstash
sudo systemctl status logstash
```
