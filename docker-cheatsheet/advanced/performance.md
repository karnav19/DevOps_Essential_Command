# Performance & Resource Constraints

## Resource limits (run)
`docker run --cpus="1.5" -m 512m <image>`

## Inspect runtime usage
`docker stats` — live metrics per container

## Image size optimization tips
- Use slim or alpine base images when appropriate.  
- Use multi-stage builds to avoid shipping build-time dependencies.  
- Clean package caches (`apt-get clean`, remove `/var/lib/apt/lists/*`).  
- Leverage `.dockerignore` to reduce build context.

## Layer best practices
- Combine related RUN statements to reduce layers (but balance caching).
- Put rarely-changing commands at top of Dockerfile to utilize cache.
