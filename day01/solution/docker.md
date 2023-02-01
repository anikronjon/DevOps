## Docker

### Install docker in your local system

Install docker in windows
> step01: Download docker from https://www.docker.com/products/docker-desktop/
>
> step02: Install the downloaded file.

Install docker in linux debian/ubuntu system
```docker
# Open terminal
# Update debian system
sudo apt update
# Check docker installed or not
docker
# Install docker
sudo apt install docker.io -y
# Note: If you want to avoid typing sudo whenever you run the docker command(optional)
sudo usermod -aG docker ${USER}
```


### Check docker version
```docker
sudo docker version
# or
sudo docker --version
```
[docker_version](assets/docker/docker_version1.png)
[docker_version](assets/docker/docker_version2.png)

### Pull some image from DockerHub
```docker
sudo docker pull ubuntu
sudo docker pull nginx
sudo docker pull alpine
```

### List down images
```docker
sudo docker images
# or
sudo docker image ls
```


### Create container from images
```docker
# Base command
# sudo docker run [options] image

# running container on background with custom name and expose port
sudo docker run -it -d -p 8000:80 --name nginx-container nginx

# running container on background with custom name
sudo docker run -it -d --name ubuntu-container ubuntu

# running container on background
sudo docker run -it -d ubuntu

# running container and inside access
sudo docker run -it ubuntu

# Just create a stop container
sudo docker run ubuntu
```

Here the options are
- it  : interactive teletype mode (container will be running)
- d   : detach mode or background
- p   : expose port local/system:container
- name: set container name

### List all running and stop container
```docker
# List all container
sudo docker ps -a

# List all running container
sudo docker ps
```

### Stop, start, restart and kill the containers.
```docker
# Stop one or more running containers
# docker stop [OPTIONS] CONTAINER
sudo docker stop Name|id [Name|id..]

# Start one or more stopped containers
sudo docker start Name|id [Name|id..]

# Restart one or more containers
sudo docker restart Name|id [Name|id..]

# Kill one or more running containers
sudo docker kill Name|id [Name|id..]
```

### Access inside of a container
```docker
# NOTE: Run this command in a running container
# docker exec [OPTIONS] CONTAINER COMMAND
sudo docker exec -it Name|id bash
# or
sudo docker exec -it Name|id shell

# Name|id or container name/id
# Here the options are
# -it : interactive teletype(TTY) mode
```

### Inspect the container
```docker
# To inspect a container or 
# see information of a container
# docker inspect [OPTIONS] NAME|ID [NAME|ID...]
sudo docker inspect Name|id [Name|id..]
```

### Remove all containers
```docker
# Remove one or more containers
sudo docker rm Name|id [Name|id..]
# OR Force the removal of a running container
sudo docker rm -f Name|id [Name|id..]

# Remove all stopped containers
sudo docker container prune
# or
sudo docker container -f prune
```

### Remove all images
```docker
# Base command | docker image
# Remove one or more images
sudo docker rmi Name|id [Name|id..]

# Remove unused images
sudo docker image prune
# OR Remove unused images forcefully
sudo docker image prune -f
```
