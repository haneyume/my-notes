# Hasura

## Official Doc

{% embed url="https://hasura.io/docs/latest/getting-started/docker-simple/" %}

## Docker Compose

```yaml
version: "3.3"

services:
  hasura:
    image: hasura/graphql-engine:latest
    container_name: hasura
    restart: always
    depends_on:
      - postgres
    environment:
      ## postgres database to store Hasura metadata
      HASURA_GRAPHQL_METADATA_DATABASE_URL: DATABASE_URL
      ## enable the console served by server
      HASURA_GRAPHQL_ENABLE_CONSOLE: "true" # set to "false" to disable console
      ## enable debugging mode. It is recommended to disable this in production
      HASURA_GRAPHQL_DEV_MODE: "true"
      HASURA_GRAPHQL_ENABLED_LOG_TYPES: startup, http-log, webhook-log, websocket-log, query-log
      ## uncomment next line to run console offline (i.e load console assets from server instead of CDN)
      # HASURA_GRAPHQL_CONSOLE_ASSETS_DIR: /srv/console-assets
      ## uncomment next line to set an admin secret
      HASURA_GRAPHQL_ADMIN_SECRET: myadminsecretkey
    ports:
      - 8080:8080
```
