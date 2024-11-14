FROM docker/compose:latest

COPY . /usr/src/app
WORKDIR /usr/src/app

ENTRYPOINT ["docker-compose", "up", "--no-recreate"]
