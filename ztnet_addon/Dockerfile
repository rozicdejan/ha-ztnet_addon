FROM homeassistant/amd64-base:latest

# Install Docker and Docker Compose
RUN apk add --no-cache docker docker-compose

# Copy Docker Compose file
COPY docker-compose.yml /etc/ztnet/docker-compose.yml

# Start services with Docker Compose
CMD ["docker-compose", "-f", "/etc/ztnet/docker-compose.yml", "up"]
