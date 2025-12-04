# Security — Best Practices

## Run non-root where possible
- `USER appuser` in Dockerfile to avoid running as root inside container.

## Scan images
- Use tools like `docker scan` (Snyk powered) or third-party scanners.

## Secrets management
- Do NOT bake secrets into images or commit `.env` files to VCS.
- Use Docker secrets, external secret managers (Vault, AWS Secrets Manager) or environment variables injected at runtime.

## Minimize attack surface
- Use minimal base images (Alpine or distroless when suitable).
- Remove package managers from final image if not needed.

## Network isolation
- Use separate networks and limit inter-service exposure.
