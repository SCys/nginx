[![Docker Container](https://github.com/SCys/nginx/actions/workflows/docker.yaml/badge.svg)](https://github.com/SCys/nginx/actions/workflows/docker.yaml)
![Docker Pulls](https://img.shields.io/docker/pulls/scys/nginx)

Debian image: ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/scys/nginx/latest)

Alpine image: ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/scys/nginx/alpine)

nginx with logrotate and build every day.

i don't not known why the default nginx in docker.io without logrotate.

docker-compose.yml add blew:

```yaml
  nginx:
    image: scys/nginx:alpine
    container_name: nginx
    restart: unless-stopped
    network_mode: host
    volumes:
      - /data/nginx/nginx.conf:/etc/nginx/nginx.conf:ro
      - /data/nginx/log:/var/log/nginx
```
