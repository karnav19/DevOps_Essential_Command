# MySQL Installation (Ubuntu) — Step-by-step

## Install
```bash
sudo apt update
sudo apt install -y mysql-server
sudo systemctl enable --now mysql
```

## Secure install
```bash
sudo mysql_secure_installation
```

## Login
```bash
sudo mysql -u root -p
```

## Tips
- Use data directory on separate disk for production.
