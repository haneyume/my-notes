# PostgreSQL

## 🔥 Docker Compose

```yaml
version: "3.3"

services:
  postgres:
    image: postgres:latest
    container_name: postgres
    restart: always
    environment:
      POSTGRES_PASSWORD: a123456
    ports:
      - 5432:5432

  adminer:
    image: adminer:latest
    container_name: adminer
    restart: always
    ports:
      - 8080:8080
```
