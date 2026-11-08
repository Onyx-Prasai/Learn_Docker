# Docker

Docker is a platform for packaging and running applications in containers. A container includes an application and the dependencies it needs, helping it run consistently across development, testing, and production environments.

Imagine an application works on one computer but fails on another because the machines have different runtimes or system packages. Docker helps address this by building a repeatable image and running it as an isolated container.

Docker allows developers to:

- Package applications with their dependencies
- Run isolated workloads on a shared host
- Start and stop consistent environments quickly
- Connect services and keep persistent data outside containers
- Share application images through registries such as Docker Hub

This is why Docker is useful throughout software development: it makes application environments easier to reproduce and share.

---

# What you will learn

- What Docker is and why we need it
- Docker images and containers
- Installation of Docker CLI and Desktop
- Important Docker commands
- Docker vs. virtual machines
- Port mapping and setting environment variables
- Troubleshooting containers
- Using containers to build a Node.js application
- Dockerizing a Node.js application with a Dockerfile
- Docker Compose: services, port mapping, environment variables, and volumes
- Publishing to Docker Hub
- Layering in Docker images
- Volume mounting
- Docker networking: default and custom networks, multi-container apps, and bridge, host, and none drivers

---

# Learning Structure

- [Docker Topics](DockerTopics/) - The folder containing the lesson files
- [What is Docker? Why do we need it?](DockerTopics/01-What-is-Docker.md)
- [Docker Images and Containers](DockerTopics/02-Images-and-Containers.md)
- [Installation of Docker CLI and Desktop](DockerTopics/03-Installation.md)
- [Important Docker Commands](DockerTopics/04-Important-Commands.md)
- [Docker vs. Virtual Machines](DockerTopics/05-Docker-vs-VMs.md)
- [Port Mapping and Setting Environment Variables](DockerTopics/06-Ports-and-Environment-Variables.md)
- [Troubleshooting Containers](DockerTopics/07-Troubleshooting.md)
- [Using Containers to Build a Node.js Application](DockerTopics/08-Node-Application.md)
- [Dockerization of a Node.js Application (Dockerfile)](DockerTopics/09-Dockerfile.md)
- [Docker Compose](DockerTopics/10-Docker-Compose.md): [Services](DockerTopics/10-Docker-Compose.md#services), [Port Mapping](DockerTopics/10-Docker-Compose.md#port-mapping), [Environment Variables](DockerTopics/10-Docker-Compose.md#environment-variables), [Volumes](DockerTopics/10-Docker-Compose.md#volumes)
- [Publishing to Docker Hub](DockerTopics/11-Docker-Hub.md)
- [Layering in Docker Images](DockerTopics/12-Image-Layers.md)
- [Volume Mounting](DockerTopics/13-Volume-Mounting.md)
- [Docker Networking](DockerTopics/14-Networking.md): [Default and Custom Networks](DockerTopics/14-Networking.md#default-and-custom-networks), [Multi-container Apps](DockerTopics/14-Networking.md#using-a-custom-network-for-multi-container-apps), [Network Drivers](DockerTopics/14-Networking.md#network-drivers)

---

After studying these lessons, you will be able to run containers, build an image for a Node.js application, manage a small multi-container setup, and understand the basics of image storage and container networking. This guide reflects the topics in my study plan and may not cover every Docker feature.

[Let's Start](DockerTopics/01-What-is-Docker.md)
