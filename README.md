# NFS Status Monitoring Application

This application is a simple Flask-based web service that monitors the availability of a Network File System (NFS) server. It is designed to run inside a Docker container and provides a web interface to display the NFS server's status.

Docker Compose

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


# Dockerfile

You can find the docker hub repository located here for this container. 
https://hub.docker.com/r/andreril/nfsup


