# Volumes — Persistent Storage

## List volumes
`docker volume ls`

## Create a volume
`docker volume create data_vol`

## Use a volume with a container
`docker run -v data_vol:/app/data <image>`
- Persists `/app/data` inside the named Docker volume.

## Bind mount (host directory)
`docker run -v /host/path:/container/path <image>`
- Good for development (live code), not as portable as volumes.

## Inspect volume
`docker volume inspect data_vol`

## Remove unused volumes
`docker volume prune` — interactive confirmation
