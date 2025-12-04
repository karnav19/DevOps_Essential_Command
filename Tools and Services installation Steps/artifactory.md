# JFrog Artifactory OSS Installation — Step-by-step

## Download & install (deb)
```bash
wget https://releases.jfrog.io/artifactory/artifactory-oss-latest.deb
sudo dpkg -i artifactory-oss-latest.deb
sudo systemctl enable --now artifactory
```

## Access UI
Open http://<server-ip>:8081 and complete setup.
