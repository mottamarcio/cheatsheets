## DOCKER

**Basic Commands:**

|Command|Description|
|---|---|
|`docker --version`|Show the Docker version information|
|`docker info`|Display system-wide information|
|`docker run <image>`|Run a container from an image|
|`docker ps`|List running containers|
|`docker ps -a`|List all containers (running and stopped)|
|`docker stop <container_id>`|Stop a running container|
|`docker stop $(docker ps -a -q)`|Stop all running containers|
|`docker start <container_id>`|Start a stopped container|
|`docker restart <container_id>`|Restart a container|
|`docker kill <container_id>`|Kill a running container|
|`docker rm <container_id>`|Remove a stopped container|
|`docker rm $(docker ps -a -q)`|Remove all stopped containers|
|`docker rmi <image_id>`|Remove an image|
|`docker rmi $(docker images -q)`|Remove all images|
|`docker rmi -f $(docker images -q)`|Force remove all images|
|`docker exec -it <container_id> <command>`|Execute a command in a running container|
|`docker logs <container_id>`|View container logs|

**Intermediate Commands:**

|Command|Description|
|---|---|
|`docker build -t <image_name> .`|Build an image from a Dockerfile|
|`docker images`|List all images|
|`docker images -q`|List only image IDs|
|`docker search <image_name>`|Search for an image on Docker Hub|
|`docker pull <image_name>`|Pull an image from Docker Hub|
|`docker push <image_name>`|Push an image to Docker Hub|
|`docker run -d <image>`|Run a container in detached mode (background)|
|`docker run -p <host_port>:<container_port> <image>`|Map a host port to a container port|
|`docker run -v <host_directory>:<container_directory> <image>`|Mount a host directory to a container|
|`docker run --name <container_name> <image>`|Give a container a name|
|`docker network create <network_name>`|Create a new network|
|`docker network ls`|List all networks|
|`docker network connect <network_name> <container_id>`|Connect a container to a network|

**Advanced Commands:**

|Command|Description|
|---|---|
|`docker build --build-arg <key>=<value> .`|Build an image with build arguments|
|`docker history <image_id>`|Show the history of an image|
|`docker inspect <container_id>`|Get detailed information about a container|
|`docker cp <container_id>:<src_path> <dest_path>`|Copy files/folders between a container and the host|
|`docker volume create <volume_name>`|Create a volume|
|`docker volume ls`|List all volumes|
|`docker volume prune`|Remove unused volumes|
|`docker volume rm $(docker volume ls -q)`|Remove all volumes|
|`docker system prune`|Remove unused containers, networks, images (dangling)|
|`docker system prune -a`|Remove all unused containers, networks, images, and volumes|
|`docker compose up`|Start services defined in a docker-compose.yml file|
|`docker compose down`|Stop and remove services defined in a docker-compose.yml file|

**Tips and Tricks:**

* Use tab completion to quickly complete commands and image/container names.
* Use `docker logs -f <container_id>` to follow container logs in real-time.
* Use `docker-compose` for managing multi-container applications.
* Use a `.dockerignore` file to exclude files from being copied into the image during the build process.
* Explore Docker Hub for a vast repository of pre-built images.

**Resources:**

* **Official Docker documentation:** [https://docs.docker.com/](https://docs.docker.com/)
* **Docker Hub:** [https://hub.docker.com/](https://www.google.com/url?sa=E&source=gmail&q=https://hub.docker.com/)
* **Docker Compose documentation:** [https://docs.docker.com/compose/](https://www.google.com/url?sa=E&source=gmail&q=https://docs.docker.com/compose/)
