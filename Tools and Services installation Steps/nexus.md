# Sonatype Nexus OSS Installation — Step-by-step

## Download & extract
```bash
wget https://download.sonatype.com/nexus/3/latest-unix.tar.gz
tar -xvf latest-unix.tar.gz
sudo mv nexus-3* /opt/nexus
sudo mv sonatype-work /opt/sonatype-work
```

## Create user & systemd
Create nexus user and systemd service to run /opt/nexus/bin/nexus run
Start and enable service; access UI on port 8081.
