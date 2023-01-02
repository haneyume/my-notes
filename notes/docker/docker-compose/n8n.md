# n8n

## Official Doc

{% embed url="https://docs.n8n.io/hosting/installation/docker/" %}

## Docker Compose

```yaml
version: "3.3"

services:
  n8n:
    image: n8nio/n8n:latest
    container_name: n8n
    restart: always
    environment:
      EXECUTIONS_PROCESS: main
      DB_TYPE: postgresdb
      DB_POSTGRESDB_SCHEMA: public
      DB_POSTGRESDB_DATABASE: n8n_data
      DB_POSTGRESDB_USER: postgres
      DB_POSTGRESDB_PASSWORD: a123456
      DB_POSTGRESDB_HOST: postgres
      DB_POSTGRESDB_PORT: 5432
    ports:
      - 5678:5678
```
