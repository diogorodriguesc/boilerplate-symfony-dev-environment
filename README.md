
# Boilerplate Symfony Dev Environment

This development environment is supported on top of docker for PHP Symfony framework.

- PHP 8.3
- NGINX

## Pre-Installation Requirements
- docker engine (https://docs.docker.com/engine/install/) (Recommended version: >=v27)
- docker-compose (https://docs.docker.com/compose/install/) (Recommended version: >=v2.29)

## Installation

Building docker images:
```bash
cd docker && docker compose -f docker-compose.yaml build
```

## Running

Starting docker containers:
```bash
cd docker && docker compose -f docker-compose.yaml up
```

## Monitoring Logs

### Nginx

```bash
docker exec -it $(docker ps --filter "ancestor=docker-xm-nginx" -q) tail -f /var/log/nginx/symfony_access.log
```

```bash
docker exec -it $(docker ps --filter "ancestor=docker-xm-nginx" -q) tail -f /var/log/nginx/symfony_error.log
```