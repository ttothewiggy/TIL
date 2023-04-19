# Docker Cheat Sheet

## Basic Commands

- `docker run <image-name>`: Runs a container from the specified image.
- `docker ps`: Lists running containers.
- `docker ps -a`: Lists all containers, including stopped ones.
- `docker stop <container-id>`: Stops a running container.
- `docker rm <container-id>`: Deletes a container.

## Image Management

- `docker images`: Lists all available images.
- `docker pull <image-name>`: Downloads an image from a registry.
- `docker build -t <image-name> .`: Builds an image from a Dockerfile in the current directory.
- `docker push <image-name>`: Pushes an image to a registry.

## Container Management

- `docker exec -it <container-id> <command>`: Runs a command inside a running container.
- `docker logs <container-id>`: Shows the logs of a container.
- `docker inspect <container-id>`: Shows detailed information about a container.
- `docker port <container-id>`: Shows the mapped port of a container.

## Networking

- `docker network ls`: Lists available networks.
- `docker network create <network-name>`: Creates a new network.
- `docker network connect <network-name> <container-id>`: Connects a container to a network.
- `docker network disconnect <network-name> <container-id>`: Disconnects a container from a network.

## Docker Compose

- `docker-compose up`: Starts all services defined in a `docker-compose.yml` file.
- `docker-compose down`: Stops all services defined in a `docker-compose.yml` file.

## Miscellaneous

- `docker system prune`: Deletes all unused resources, including images, containers, and networks.
- `docker version`: Shows the Docker version information.
- `docker info`: Shows detailed information about the Docker installation.
