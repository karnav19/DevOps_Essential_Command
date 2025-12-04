# NGINX Installation — Step-by-step

## Install & start
```bash
sudo apt update
sudo apt install -y nginx
sudo systemctl enable --now nginx
```

## Firewall
```bash
sudo ufw allow 'Nginx Full'
```

## Reverse proxy example
Edit `/etc/nginx/sites-available/default` and add:
```
location / {
  proxy_pass http://127.0.0.1:8080;
}
```
Then:
```bash
sudo nginx -t
sudo systemctl reload nginx
```
