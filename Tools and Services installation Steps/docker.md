# Docker Engine Installation (Ubuntu) — Step-by-step

## 1) Prerequisites and GPG key
```bash
sudo apt update
sudo apt install -y ca-certificates curl gnupg lsb-release
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

## 2) Add repository
```bash
echo   "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg]   https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"   | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
```

## 3) Install Docker
```bash
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
sudo systemctl enable --now docker
```

## 4) Test & post-install
```bash
sudo docker run --rm hello-world
sudo usermod -aG docker $USER
# Log out and back in for group change to apply
```

## 5) Tips
- Configure daemon.json for registry mirrors, log-driver, etc.
