# Apache HTTP Server Installation — Step-by-step

## Install
```bash
sudo apt update
sudo apt install -y apache2
sudo systemctl enable --now apache2
```

## Firewall
```bash
sudo ufw allow 'Apache Full'
```

## Virtual host example
Create `/etc/apache2/sites-available/example.conf` and enable with `a2ensite`.
