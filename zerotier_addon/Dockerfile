ARG BUILD_FROM=ghcr.io/hassio-addons/base:15.0.8
FROM ${BUILD_FROM}

# Copy docker-compose files into the container
COPY . /usr/src/app
WORKDIR /usr/src/app

# Ensure Docker Compose is installed and accessible
RUN apk add --no-cache docker-compose

ENTRYPOINT ["docker-compose", "up", "--no-recreate"]
