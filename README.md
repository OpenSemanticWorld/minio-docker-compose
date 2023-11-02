# minio-docker-compose

## Deploy

### Base
```bash
git clone https://github.com/OpenSemanticWorld/minio-docker-compose
cd minio-docker-compose
cp .env.example .env
docker compose up
```
## Overrides

e. g. to use caddy as reverse proxy (see [caddy-docker-proxy](https://github.com/OpenSemanticWorld/caddy-docker-proxy))
```bash
cp docker-compose.caddy.example.override.yml docker-compose.override.yml
docker compose up
```

## Settings
.env:

| Key        | Description           | Example | Change |
| ------------- |:-------------:|:-----:|:-----:|
| MINIO_UI_SERVER | Domain for the web UI | https://minio.example.com | Required |
| MINIO_API_SERVER | Domain for the S3 API | https://s3.example.com | Required |
| MINIO_ROOT_USER | Admin user name | admin | Recommended |
| MINIO_ROOT_PASSWORD | admin password | change_me | Recommended |

## Further readings

- https://github.com/minio/minio/tree/master/docs/orchestration/docker-compose
- https://github.com/minio/minio/blob/master/docs/sts/keycloak.md
- Client: e. g. https://prefecthq.github.io/prefect-aws/s3/