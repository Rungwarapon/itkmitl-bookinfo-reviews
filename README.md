# How to run reviews service

## Prerequisite

* Java 8

```bash
/opt/ibm/wlp/bin/server run defaultServer
```

## How to run with Docker

```bash
# Build Docker Image for reviews service
docker build -t reviews .

# Run details service on port 8082
docker run -d --name reviews -p 8082:8082 -e ENABLE_EXTERNAL_BOOK_SERVICE=true reviews
```

* Test with path `/reviews/1` and `/health`

## How to run with Docker Compose

```bash
# Build Docker Image for reviews service
docker-compose build

# Run details service on port 8082
docker-compose up
```