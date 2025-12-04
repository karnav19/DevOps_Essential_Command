# RabbitMQ Installation — Step-by-step

## Install Erlang & RabbitMQ
```bash
sudo apt update
sudo apt install -y erlang
sudo apt install -y rabbitmq-server
sudo systemctl enable --now rabbitmq-server
```

## Enable management UI
```bash
sudo rabbitmq-plugins enable rabbitmq_management
```
Access http://<server-ip>:15672 (guest/guest default on localhost).

## Tips
- Create users and virtual hosts for isolation.
