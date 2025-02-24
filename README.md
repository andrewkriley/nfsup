#NFS Status Monitoring Application

This application is a simple Flask-based web service that monitors the availability of a Network File System (NFS) server. It is designed to run inside a Docker container and provides a web interface to display the NFS server's status.

Getting Started TBC


Docker Compose

# My Project

This is a simple example of how to include a code snippet in a README file.

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



Dockerfile 

You can find the docker hub repository located here
https://hub.docker.com/r/andreril/nfsup


