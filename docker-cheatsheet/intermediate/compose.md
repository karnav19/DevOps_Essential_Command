# Docker Compose — Multi-container Applications

## Basic `docker-compose.yml` example
```
version: "3.9"
services:
  web:
    build: .
    ports:
      - "8080:80"
    volumes:
      - .:/app
  db:
    image: postgres:15
    environment:
      POSTGRES_PASSWORD: example
```

## Commands
- `docker compose up` — start services (foreground)  
- `docker compose up -d` — start in background  
- `docker compose down` — stop & remove networks/containers  
- `docker compose logs -f` — follow logs  
- `docker compose exec web bash` — run command in service container  
- `docker compose up --build` — rebuild images then start

## Tips
- Use named volumes for persisting DB data.  
- `depends_on` controls startup order but does not wait for readiness. Use healthchecks for readiness dependent services.
