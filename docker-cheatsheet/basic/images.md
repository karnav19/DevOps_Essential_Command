# Images — Commands & Explanations

## List images
`docker images` — list local images

## Pull an image from registry
`docker pull <image:tag>` (default tag is `latest`)

## Build image from Dockerfile
`docker build -t myapp:1.0 .`
- `-t` tags the image
- `.` is build context (current directory)

## Build without cache
`docker build --no-cache -t myapp:1.0 .`

## Tagging
`docker tag source:tag username/repo:tag`
Prepares image for pushing to a registry.

## Remove image
`docker rmi <image_or_id>`

## Remove all unused images (dangling and unreferenced)
`docker image prune -a`

## Save / Load (transferable file)
`docker save -o myapp.tar myapp:1.0`  
`docker load -i myapp.tar`
