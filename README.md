# NFS Status Monitoring Application

This application is a simple Flask-based web service that monitors the availability of a Network File System (NFS) server. It is designed to run inside a Docker container and provides a web interface to display the NFS server's status.

Docker Compose

Create a local environment file to nominate your NFS Server and NFS Port. 2049 is the default TCP for the NFS service.

```
NFS_SERVER=place.your.server.here
NFS_PORT=2049
```

Create a docker-compose.yaml file

```yaml

services: 
  nfsup:
    image: andreril/nfsup:latest
    restart: unless-stopped
    environment:
      NFS_SERVER: ${NFS_SERVER}
      NFS_PORT: ${NFS_PORT}
    ports:
    - 80:80
```

Start your container using docker compose

```bash

docker compose up -d

```
Start your container using docker run

```bash
docker run -e NFS_SERVER=<server ip> -e NFS_PORT=2049 -d -p 80:80 --name nfsup nfsup
```
OR
```bash
docker run --env-file .env -d -p 80:80 --name nfsup nfsup
```

Dockerfile

You can find the docker hub repository located here for this container. 
https://hub.docker.com/r/andreril/nfsup


