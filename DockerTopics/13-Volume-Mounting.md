# Volume Mounting

[Back to the learning guide](../README.md)

Container filesystems are typically removed with their containers. Mounts let containers share files or keep data outside the container’s writable layer.

## Named Volume

Docker manages the storage location. Named volumes are commonly used for persistent application data:

```sh
docker volume create app-data
docker run -d --name db -v app-data:/var/lib/example database-image
```

## Bind Mount

A bind mount maps a specific host path into the container, useful for local source files:

```sh
docker run --rm -it -v "${PWD}:/app" -w /app node:22-alpine
```

Mount syntax and path handling differ by shell and operating system. Mounting over a non-empty container directory hides the files that were there. Compose can declare named volumes and bind mounts; see [Docker Compose](10-Docker-Compose.md).

Next: [Docker Networking](14-Networking.md).
