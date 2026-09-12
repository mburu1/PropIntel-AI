# Docker

Local development should provide disposable PostgreSQL, Redis, broker, and object-storage-compatible services through the existing [`docker-compose.yml`](../../docker-compose.yml). Application containers must be multi-stage, run as non-root, pin base images, include health checks, and contain no secrets.

Production images are immutable and promoted by digest. Compose is for local development and integration testing, not production orchestration.
