# Docker Images and Containers

[Back to the learning guide](../README.md)

An image is a packaged filesystem and configuration. A container is an instance created from an image. You can start multiple containers from the same image, each with its own runtime state and configuration.

```sh
docker pull nginx
docker run --name web nginx
docker ps
docker ps -a
docker stop web
docker rm web
```

`docker run` creates and starts a container. Add `-d` to run it in the background. Removing a container does not remove its image.

Next: [Install Docker](03-Installation.md) or review [important commands](04-Important-Commands.md).
