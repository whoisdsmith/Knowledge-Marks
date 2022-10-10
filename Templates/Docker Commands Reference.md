---
Date: 2022-07-31
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Topic/Dev", "#Type/Reference"]
Alias: ["Docker Commands"]
---

# Docker Commands Reference

*Source: [tech-workbook/docker-commands.md at master · akarazhev/tech-workbook (github.com)](https://github.com/akarazhev/tech-workbook/blob/master/commands/docker-commands.md)*

## Contents

- [[#Manage Images|Manage Images]]
- [[#Manage Containers|Manage Containers]]
- [[#Manage Containers (ctd)|Manage Containers (ctd)]]
- [[#Manage your (local) Virtual Machine|Manage your (local) Virtual Machine]]
- [[#Manage Networks|Manage Networks]]
- [[#Manage Volumes|Manage Volumes]]
- [[#Docker Compose|Docker Compose]]
- [[#Manage a Swarm|Manage a Swarm]]
- [[#Manage Stacks|Manage Stacks]]
- [[#Appendix: Links and References|Appendix: Links and References]]

## Manage Images

```bash
docker image pull <image name>
```

Download an image from DockerHub

```bash
docker image ls
```

List all local images

```bash
docker image build -t <image name> .
```

Build an image with a tag (note the dot!)

```bash
docker image push <image name>
```

Publish an image to dockerhub

```bash
docker image tag <image id> <tag name>
```

Tag an image - either alias an exisiting image or apply a :tag to one

## Manage Containers

```bash
docker container run -p <public port>:<container port> <image name>
```

Run a container from an image, publishing the specified ports

```bash
docker container ls -a
```

List all containers, even the stopped ones

```bash
docker container stop <container id>
```

Stop a running container

```bash
docker container start <container id>
```

Restart a stopped container

```bash
docker container rm <container id>
```

Remove a stopped container
 
## Manage Containers (ctd) 

```bash
docker container prune
```

Remove all stopped containers

```bash
docker container run -it <image name>
```

Run a container with interactive terminal

```bash
docker container run -d <image name>
```

Run a container detached (or in a daemon like way)

```bash
docker container exec -it <container id> <command>
```

Run a command in a container

```bash
docker container exec -it <container id> bash
```

Special form of the above, runs a bash shell, connected to your local terminal (your distro needs to have bash, alpine will require /bin/sh)

```bash
docker container logs -f <container id>
```

Follow the log (STDIN/System.out) of the container

```bash
docker container commit -a "author" <container id> <image name>
```

Take a snapshot image of a container

## Manage your (local) Virtual Machine

```bash
docker-machine ip
```

Find the IP address of your VirtualMachine, required for Docker Toolbox users only

## Manage Networks 

```bash
docker network ls
```

List all networks

```bash
docker network create <network name>
```

Create a network using the bridge driver

## Manage Volumes 

```bash
docker volume ls
```

List all volumes

```bash
docker volume prune
```

Delete all volumes that are not currently mounted to a container

```bash
docker volume inspect <volume name>
```

Inspect a volume (can find out the mount point, the location of the volume on the host system)

```bash
docker volume rm <volume name>
```

Remove a volume

## Docker Compose

```bash
docker-compose up
```

Process the default docker-compose.yaml file, starting any containers as required. If containers are already running they are ignored, meaning this command also serves as a "redeploy".

```bash
docker-compose up -d
```

Run containers in the detached state. Note the order of the command line arguments!

```bash
docker-compose logs -f <service name>
```

Follow the log for the specified service. Omit the -f to tail the log.

```bash
docker-compose down
```

Stop all the containers (services) listed in the default compose file.

## Manage a Swarm

```bash
docker swarm init (--advertise-addr <ip address>)
```

Switch the machine into Swarm mode. We didn't cover how to stop swarm mode: docker swarm leave --force

```bash
docker service create <args>
```

Start a service in the swarm. The args are largely the same as those you will have used in docker container run.

```bash
docker network create --driver overlay <name>
```

Create a network suitable for using in a swarm.

```bash
docker service ls
```

List all services

```bash
docker node ls
```

List all nodes in the swarm

```bash
docker service logs -f <service name>
```

Follow the log for the service. This feature is a new feature in Docker and may not be available on your version (especially if using Linux Repository Packages).

```bash
docker service ps <service name>
```

List full details of the service - in particular the node on which it is running and any previous failed containers from the service.

```bash
docker swarm join-token <worker|manager>
```

Get a join token to enable a new node to connect to the swarm, either as a worker or manager.

## Manage Stacks 

```bash
docker stack ls
```

List all stacks on this swarm.

```bash
docker stack deploy -c <compose file> <stack name>
```

Deploy (or re-deploy) a stack based on a standard compose file.

```bash
docker stack rm <stack name>
```

Delete a stack and its corresponding services/networks/etc.

***

## Appendix: Links and References

- [[Developer/Development]]
- [[Docker]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022