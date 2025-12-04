# Containers — Commands & Explanations

## Run a container
`docker run <image>`
Runs the image in a new container (foreground).

## Run detached (background)
`docker run -d <image>`
Use `-d` to run container in background.

## Run with port mapping
`docker run -p 3000:80 <image>`
Maps host port 3000 → container port 80.

## Interactive shell
`docker run -it <image> /bin/bash`
Starts container with an interactive terminal (useful for debugging).

## List containers
`docker ps` — running containers  
`docker ps -a` — all containers (including stopped)

## Stop / Start / Restart
`docker stop <container>` — graceful stop (sends SIGTERM then SIGKILL after timeout)  
`docker start <container>` — start a stopped container  
`docker restart <container>` — stop then start

## Remove container
`docker rm <container>` — remove stopped container  
`docker rm -f <container>` — force remove (kills if running)

## Remove all stopped containers
`docker container prune` — interactive confirmation

## Execute a command in a running container
`docker exec -it <container> bash`
Use `exec` to run commands inside an existing container.

## Copy files
`docker cp hostfile.txt <container>:/path/`  
`docker cp <container>:/path/log.txt ./`
