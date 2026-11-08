# Docker Networking

[Back to the learning guide](../README.md)

Containers use networks to communicate. Docker provides built-in network drivers, including bridge, host, and none. Availability and behavior vary across platforms; host networking support differs between Docker Engine on Linux and Docker Desktop.

## Default and Custom Networks

Containers attached to a user-defined bridge network can discover one another by container or service name. Create and inspect a network with:

```sh
docker network create app-network
docker network ls
docker network inspect app-network
```

## Using a Custom Network for Multi-container Apps

Attach related containers to the same user-defined network with `--network app-network`. They can communicate using their container names. Compose creates a project network by default and makes services discoverable by service name.

## Network Drivers

- **Bridge:** A common choice for container communication on one Docker host.
- **Host:** Uses the host network stack where supported, with less network isolation.
- **None:** Disables normal network connectivity for the container.

Publishing a port is separate from attaching containers to a shared network. See [port mapping](06-Ports-and-Environment-Variables.md) and [Docker Compose](10-Docker-Compose.md).

[Back to the learning guide](../README.md)
