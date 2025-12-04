# Redis Installation — Step-by-step

## Install
```bash
sudo apt update
sudo apt install -y redis-server
sudo systemctl enable --now redis-server
```

## Test
```bash
redis-cli ping
# PONG expected
```

## Tips
- Configure persistence (RDB/AOF) and set maxmemory for eviction.
