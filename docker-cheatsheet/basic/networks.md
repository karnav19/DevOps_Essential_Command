# Networks — Container Networking

## List networks
`docker network ls`

## Create a network
`docker network create mynet`

## Run a container attached to a specific network
`docker run --network mynet --name webapp -d myimage`

## Connect/disconnect running container
`docker network connect mynet mycontainer`  
`docker network disconnect mynet mycontainer`

## Inspect network
`docker network inspect mynet`
- Shows connected containers and IP addresses.

## Common use: `bridge`, `host`, and `none`
- `bridge` (default user-defined bridge is recommended)  
- `host` (container uses host network stack)  
- `none` (no network)
