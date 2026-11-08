# Docker Compose

[Back to the learning guide](../README.md)

Docker Compose describes an application made of services in a YAML file. It can build images, configure ports and environment, attach volumes, and create a network for the application.

Example `compose.yaml` for the Node app:

```yaml
services:
  app:
    build: .
    ports:
      - "3000:3000"
    environment:
      NODE_ENV: development
    volumes:
      - .:/app
      - /app/node_modules
```

Run `docker compose up --build` to build and start services, and `docker compose down` to stop and remove their containers and network. Named volumes are useful for persistent data; a bind mount is convenient during development and can hide files already present at the mount path.

## Services

Each entry under `services` defines an application component, such as a web app or database. Compose creates a network so services can usually reach one another by service name.

## Port Mapping

The `ports` setting publishes a service port to the host. In `"3000:3000"`, the first port is on the host and the second is in the container.

## Environment Variables

The `environment` setting passes runtime configuration into a service. Do not commit credentials in a Compose file; use an appropriate secrets mechanism for sensitive values.

## Volumes

The `volumes` setting mounts named volumes or host paths into a service. Named volumes are useful for data that should persist beyond a container’s lifecycle.

Next: [Publishing to Docker Hub](11-Docker-Hub.md).
