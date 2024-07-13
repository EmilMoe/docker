# Laravel

Create an .env file:

```
APP_NAME=my-service
DOMAINS=example.com,alias.example.com
APP_REGISTRY=my-app-registry
APP_BRANCH=main
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
