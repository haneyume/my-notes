# MinIO

## 🔥 Official Doc

{% embed url="https://min.io/docs/minio/container/operations/install-deploy-manage/deploy-minio-single-node-single-drive.html" %}

## 🔥 Docker Compose

```yaml
version: "3.3"

services:
  minio:
    image: quay.io/minio/minio:latest
    container_name: minio
    restart: always
    environment:
      MINIO_ROOT_USER: admin
      MINIO_ROOT_PASSWORD: Aa123456
    ports:
      - 9000:9000
      - 9090:9090
    command: server /data --console-address ":9090"
```
