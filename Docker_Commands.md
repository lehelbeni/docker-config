# Create Docker Image

docker build . -t <image-name>
docker build . -t <image-name> -f Dockerfile.dev

# See images

docker image ls

# Remove image

docker image rm <ID>

---

# Create Docker Container

docker run -d -p 3000:3000 --name <container-name> <image-name>

# See runing containers

docker ps

# Stop runing container

doker stop <container-name>

# Remove Docker container

doker rm <container-name> -f

# Get inside docker container

docker exec -it react-app bash

---

# Bine mount Syncronize Folder

- docker volume to create bin mount
- read-olny localdir:containerdir:ro
  docker run -v dirlocal:container directory -d -p 3000:3000 --name image-name

docker run -v $(pwd):/app:ro -d -p 3000:3000 --name react-app react-image

# Docker Compose

docker-compose.yml file creation

# Start all containers

docker-compose up -d
docker-compose up -d --build

# Kill all containers

docker-compose down

---

# Create production enviroment for react

1. Multi stage Docker Build

# Docker compose multiple

# Development server

docker-compose -f docker-compose.yml -f docker-compose-dev.yml

## Production server

docker-compose -f docker-compose.yml -f docker-compose-prod.yml