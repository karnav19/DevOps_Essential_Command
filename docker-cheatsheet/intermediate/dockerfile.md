# Dockerfile — Best Practices & Common Instructions

## Basic Dockerfile example
```
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --production
COPY . .
CMD ["node", "server.js"]
```

## Important instructions
- `FROM` — base image
- `WORKDIR` — sets working directory
- `COPY` / `ADD` — copy files into image (`ADD` can extract archives & fetch remote URLs`)
- `RUN` — commands executed at build time
- `ENV` — environment variables baked into image
- `EXPOSE` — documents container port (doesn't map host port)
- `CMD` vs `ENTRYPOINT`:
  - `CMD` provides default args for `docker run` (can be overridden)
  - `ENTRYPOINT` sets a fixed executable (CMD supplies default args)

## Multi-stage builds (smaller final images)
```
FROM golang:1.20 AS builder
WORKDIR /src
COPY . .
RUN go build -o app

FROM alpine:3.18
COPY --from=builder /src/app /usr/local/bin/app
ENTRYPOINT ["/usr/local/bin/app"]
```

## Tips
- Order your Dockerfile to maximize layer caching (frequently changing lines at bottom).
- Use `.dockerignore` to reduce build context size.
