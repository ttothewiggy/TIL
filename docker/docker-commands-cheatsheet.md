## DOCKER IMAGE COMMANDS

|arduino|

|Copy code|

|docker images                          |   # list all images|

|docker pull <image-name>             |    # download an image from a registry|

|docker build -t <image-name> <path>    |  # build an image from a Dockerfile|

|docker push <image-name>               |  # push an image to a registry|

|docker rmi <image-name>                 | # remove an image|


## DOCKER CONTAINER COMMANDS

|bash

|Copy code

|docker ps                                # list running containers

|docker ps -a                             # list all containers (including stopped ones)

|docker run <image-name>                  # start a new container from an image

|docker start <container-id/name>         # start a stopped container

|docker stop <container-id/name>          # stop a running container

|docker rm <container-id/name>            # remove a container

|docker exec <container-id/name> <command>   # execute a command inside a running container



## DOCKER NETWORK COMMANDS

bash

Copy code

docker network ls                         # list available networks

docker network create <network-name>      # create a new network

docker network connect <network-name> <container-id/name>   # connect a container to a network

docker network disconnect <network-name> <container-id/name>  # disconnect a container from a network


## DOCKER VOLUME COMMANDS

bash

Copy code

docker volume ls                          # list available volumes

docker volume create <volume-name>        # create a new volume

docker volume inspect <volume-name>       # inspect a volume

docker volume rm <volume-name>            # remove a volume

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
