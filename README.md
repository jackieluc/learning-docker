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

# Testing With Docker

`-it` - lets us interact with the docker container (short hand for `--interactive` and `--tty`, which runs the docker container with pseudo terminal and stdin/stdout)

NOTE: this will not auto-update when you add, remove, or modify any tests. To get auto-updating tests, see [Testing With Docker Compose](#testing-with-docker-compose).

```sh
docker run -it learning-docker:local npm test
```

# Testing With Docker Compose

Docker Compose will create a new service (container) to run the tests and watch and auto-update when you add, remove, or modify any tests.

NOTE: we will no longer have interactivity with the test container... you may investigate changing the PID of the process of the docker container so you can `docker attach` to the test container

```sh
docker-compose up
```
