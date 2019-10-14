# learning-docker

The goal of this project is to familiarize myself with Docker.

# Docker Build

```sh
docker build -f Dockerfile.dev -t learning-docker:local .
```

# Docker Run

```sh
docker run -p 3000:3000 learning-docker:local
```

# Docker Compose

```sh
docker-compose up
```
