# PostgreSQL Installation — Step-by-step

## Install
```bash
sudo apt update
sudo apt install -y postgresql postgresql-contrib
sudo systemctl enable --now postgresql
```

## Basic usage
```bash
sudo -u postgres psql
CREATE USER myuser WITH PASSWORD 'pass';
CREATE DATABASE mydb OWNER myuser;
```

## Tips
- Use pg_hba.conf for access control and backups (pg_dump).
