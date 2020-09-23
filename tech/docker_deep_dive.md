# Docker Deep Dive

## Information

| | Book data |
| --- | --- |
| **Title**  | Docker Deep Dive |
| **Author** | Nigel Pulton |
| **Release Date** | May 14, 2020 |
| **ISBN** | ISBN-13: 978-1-52-182280-7 |
| **Webpage** | https://nigelpoulton.com/books |

## Chapter 4: The big picture

### Images

It's useful to think of a Docker image as an object that contains an OS filesystem, an application, and all application dependencies. If you work in operations, it’s like a virtual machine template. A virtual machine template is essentially a stopped virtual machine. In the Docker world, **an image is effectively a stopped container.**

## Useful commands

### Images

| Command | Description |
| --- | --- |
| `docker image ls` | List all the images that you have in your Docker host. |
| `docker build . -t TAG:VERSION` | Build an image from current directory (the Dockerfile must be there) |

### Containers

| Command | Description |
| --- | --- |
| `docker container ps` | List all the running containers. |
| `docker container run -d -p HOST_PORT:CONTAINER_PORT IMAGE_TAG:IMAGE_VERSION` | Run an image with a port forwarding configuration in background (-d) |
| `docker stop CONTAINER_ID` | Stop a container using the Container ID given by `docker container ps` |
