NFS Status Monitoring Application

This application is a simple Flask-based web service that monitors the availability of a Network File System (NFS) server. It is designed to run inside a Docker container and provides a web interface to display the NFS server's status.


Table of Contents

[Getting Started](#getting-started)
[Prerequisites](#prerequisites)
[Installation](#installation)
[Usage](#usage)
[Environment Variables](#environment-variables)
[Health Check](#health-check)
[Contributing](#contributing)
[License](#license)

Getting Started

These instructions will help you set up and run the NFS Status Monitoring application on your local machine for development and testing purposes.


Prerequisites

Docker: Ensure Docker is installed on your system. You can download it from [here](https://www.docker.com/products/docker-desktop\).
Docker Compose: Required to manage multi-container Docker applications. Installation instructions can be found [here](https://docs.docker.com/compose/install/\).

Installation

Clone the repository

bash
Copy Code
git clone https://github.com/yourusername/nfs-status-monitor.git
cd nfs-status-monitor
Build the Docker image

Execute the following command to build your Docker image:

bash
Copy Code
docker-compose build

Usage

To start the application, simply run:


bash
Copy Code
docker-compose up

This command will start the Flask application in a Docker container. By default, the application listens on port 80.


Open your web browser and navigate to http://localhost to view the NFS status.


Environment Variables

The application requires two environment variables to communicate with the NFS server:


NFS_SERVER: The IP address or hostname of the NFS server.
NFS_PORT: The port on which the NFS server is listening. Default is 2049.

These variables can be set in a .env file at the root of your project:


env
Copy Code
NFS_SERVER=your_nfs_server_address
NFS_PORT=2049

Health Check

The Docker container includes a health check to monitor the status of the NFS server every 30 seconds. If the NFS server becomes unreachable, the health check will fail.


Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements.


Fork the Project
Create your Feature Branch (git checkout -b feature/AmazingFeature)
Commit your Changes (git commit -m 'Add some AmazingFeature')
Push to the Branch (git push origin feature/AmazingFeature)
Open a Pull Request

License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
