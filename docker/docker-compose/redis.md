# Redis

## 🔥 Docker Compose

```yaml
version: "3.3"

services:
  redis:
    image: redis:latest
    container_name: redis
    restart: always
    ports:
      - 6379:6379
```
