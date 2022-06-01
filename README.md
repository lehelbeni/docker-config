# docker Commands

# Run Docker Container

docker run -it --env-file ./.env -v %cd%\src:/app/src -d -p 3000:3000 --name react-app react image

# Create docker image

docker build . -t (tag) <react-image>

# see runing images

docker image ls

# docker image rm <id>

Create container

# create container

docker run -d -p 3000:3000 --name <name of docker container> <react-image-name>

# see runing containers

docker ps
