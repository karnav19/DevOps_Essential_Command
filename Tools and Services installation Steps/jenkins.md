# Jenkins Installation (Ubuntu/Debian) — Step-by-step

## Overview
Jenkins is an automation server for CI/CD. This guide installs Jenkins LTS on Ubuntu/Debian.

## 1) Install Java (Jenkins needs Java)
```bash
sudo apt update
sudo apt install -y openjdk-11-jdk
java -version
```
Verify Java 11 is installed.

## 2) Add Jenkins repo & key
```bash
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt update
```

## 3) Install Jenkins
```bash
sudo apt install -y jenkins
sudo systemctl enable --now jenkins
sudo systemctl status jenkins
```

## 4) Firewall (optional)
```bash
sudo ufw allow 8080/tcp
sudo ufw reload
```

## 5) Unlock Jenkins & initial setup
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
Open http://<server-ip>:8080, paste password, install suggested plugins, create admin user.

## 6) Tips
- Run Jenkins behind NGINX for TLS and reverse proxy.
- Store `JENKINS_HOME` on persistent volume for backups.
