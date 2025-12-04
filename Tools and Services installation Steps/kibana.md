# Kibana Installation — Step-by-step

## 1) Download & install
```bash
wget https://artifacts.elastic.co/downloads/kibana/kibana-8.9.0-amd64.deb
sudo dpkg -i kibana-8.9.0-amd64.deb
```

## 2) Enable & start
```bash
sudo systemctl enable --now kibana
sudo systemctl status kibana
```

## 3) Access UI
Open http://<server-ip>:5601 and configure index patterns.

## Tips
- Secure Kibana with proxy+TLS in production.
