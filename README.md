# Laravel

Create an .env file:

```
NAME=my-service
REGISTRY=my-app-registry
BRANCH=main
DOMAINS=example.com,alias.example.com
```

Use this docker-compose.yml

```yaml
version: '3'

services:
  httpd:
    extends:
      file: https://raw.githubusercontent.com/EmilMoe/docker/main/laravel.yml
      service: httpd

  app:
    extends:
      file: https://raw.githubusercontent.com/EmilMoe/docker/main/laravel.yml
      service: app

  scheduler:
    extends:
      file: https://raw.githubusercontent.com/EmilMoe/docker/main/laravel.yml
      service: scheduler

  worker:
    extends:
      file: https://raw.githubusercontent.com/EmilMoe/docker/main/laravel.yml
      service: worker
```
