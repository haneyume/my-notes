# WordPress

## 🔥 Docker Compose

```yaml
version: "3.3"

services:
  wordpress:
    image: wordpress:latest
    container_name: wordpress
    restart: always
    environment:
      WORDPRESS_DB_HOST: mysql
      WORDPRESS_DB_NAME: exampledb
      WORDPRESS_DB_USER: exampleuser
      WORDPRESS_DB_PASSWORD: examplepass
    ports:
      - 8080:80

  mysql:
    image: mysql:latest
    container_name: mysql
    restart: always
    environment:
      MYSQL_DATABASE: exampledb
      MYSQL_USER: exampleuser
      MYSQL_PASSWORD: examplepass
      MYSQL_RANDOM_ROOT_PASSWORD: "1"
```
