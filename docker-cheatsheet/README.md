# 🐳 Docker Commands Cheat Sheet

A complete Docker commands cheat sheet with explanations. Designed for DevOps engineers, SREs,
and interview preparation. This repository contains a single consolidated `README.md` and a
structured set of topic-specific Markdown files.

## Repo structure
```
docker-cheatsheet/
├── README.md
├── basic/
│   ├── containers.md
│   ├── images.md
│   ├── volumes.md
│   └── networks.md
├── intermediate/
│   ├── dockerfile.md
│   ├── compose.md
│   └── debugging.md
└── advanced/
    ├── registry.md
    ├── performance.md
    └── security.md
```

## How to use
- Browse topic folders for focused commands + explanations.
- Copy commands into your terminal (adjust placeholders).
- Contribute by sending a PR or updating files.

## Quick start (examples)
- Build: `docker build -t myapp:1.0 .`
- Run: `docker run -d -p 8080:80 myapp:1.0`
- Compose: `docker compose up -d`

Enjoy! ⭐
