# Label Studio

## 🔥 Official Doc

{% embed url="https://labelstud.io/guide/install.html#Install-with-Docker" %}

## 🔥 Docker Compose

```yaml
version: "3.3"

services:
  label-studio:
    image: heartexlabs/label-studio:latest
    container_name: label-studio
    restart: always
    volumes:
      - ./mydata:/label-studio/data
    ports:
      - 8080:8080
```
