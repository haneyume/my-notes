# Node-Red

## 🔥 Official Doc

{% embed url="https://nodered.org/docs/getting-started/docker" %}

## 🔥 Docker Compose

```yaml
version: "3.3"

services:
  nodered:
    image: nodered/node-red:latest
    container_name: nodered
    restart: always
    ports:
      - 1880:1880
```
