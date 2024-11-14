ARG BUILD_FROM=homeassistant/amd64-base:latest
FROM ${BUILD_FROM}

# Install Docker and Docker Compose
RUN apk add --no-cache docker docker-compose

# Create a directory for the Docker Compose configuration
RUN mkdir -p /etc/ztnet

# Copy Docker Compose file into the created directory
COPY docker-compose.yml /etc/ztnet/docker-compose.yml

# Set working directory
WORKDIR /etc/ztnet

# Ensure Docker service is started (only required for some environments)
# Using `CMD` to start Docker Compose services
CMD ["docker-compose", "-f", "/etc/ztnet/docker-compose.yml", "up", "--no-recreate"]


#FROM homeassistant/amd64-base:latest

# Install Docker and Docker Compose
#RUN apk add --no-cache docker docker-compose

# Copy Docker Compose file
#COPY docker-compose.yml /etc/ztnet/docker-compose.yml

# Start services with Docker Compose
#CMD ["docker-compose", "-f", "/etc/ztnet/docker-compose.yml", "up"]
