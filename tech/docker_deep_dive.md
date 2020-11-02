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

## Chapter 11: Docker Networking

### Single-host bridge networks

The name tell us two things:

* **Single-host** tells us it only exists on a _single Docker host_ and can only connect containers that are on the same host.
* **Bridge** tells us that it’s an implementation of an 802.1d bridge (layer 2 switch).

Every Docker host gets a default single-host bridge network. On Linux it’s called **_bridge_**, and on Windows it’s called **_nat_**.

A bridge network uses a software bridge which allows containers connected to the same bridge network to communicate, while providing isolation from containers which are not connected to that bridge network. The Docker bridge driver automatically installs rules in the host machine so that containers on different bridge networks cannot communicate directly with each other.

## Useful commands

### Images

| Command | Description |
| --- | --- |
| `docker image ls` | List all the images that you have in your Docker host. |
| `docker build . -t TAG:VERSION` | Build an image from current directory (the Dockerfile must be there). |

### Containers

| Command | Description |
| --- | --- |
| `docker container ps` | List all the running containers. |
| `docker container ls -a` | List all containers. |
| `docker container run -d -p HOST_PORT:CONTAINER_PORT IMAGE_TAG:IMAGE_VERSION` | Run an image with a port forwarding configuration in background (-d). |
| `docker stop CONTAINER_ID` | Stop a container using the Container ID given by `docker container ps`. |
| `docker exec -it CONTAINER_ID bash` | Enter a running container.|

### Network

| Command | Description |
| --- | --- |
| `docker network create -d bridge NETWORK_NAME` | Create a new bridge network. |
| `docker network ls` | List all available networks in a Docker host. |
| `docker network inspect NETWORK_NAME` | Returns information about the network by name, for example the containers connected to it. |
