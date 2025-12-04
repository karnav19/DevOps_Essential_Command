# Registry — Push & Pull (Docker Hub / Private Registries)

## Login
`docker login` — prompts for username/password (or use token)

## Tag before push
`docker tag local:tag username/repo:tag`

## Push image
`docker push username/repo:tag`

## Pull image
`docker pull username/repo:tag`

## Working with private registries
- Use fully qualified name: `myregistry.example.com/myrepo/myimage:tag`  
- Configure `docker login myregistry.example.com` and use registry credentials or token.
