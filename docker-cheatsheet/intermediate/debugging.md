# Debugging & Logs

## View logs
`docker logs <container>`  
`docker logs -f <container>` — follow logs  
`docker logs --tail 100 <container>` — last 100 lines

## Real-time metrics
`docker stats` — CPU / memory / network I/O (live)

## Inspect container metadata
`docker inspect <container>` — detailed JSON about container, mounts, network, env vars

## Enter running container
`docker exec -it <container> bash` or `sh`

## Check exposed ports
`docker port <container>`

## Container events (troubleshooting lifecycle)
`docker events --since "1h"` — events in last hour

## Common troubleshooting flow
1. `docker ps -a` — is container running?  
2. `docker logs <container>` — check app logs  
3. `docker inspect <container>` — check env & mounts  
4. `docker exec -it <container> /bin/sh` — replicate failures interactively
