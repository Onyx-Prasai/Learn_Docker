# What is Docker? Why do we need it?

[Back to the learning guide](../README.md)

Docker is a platform for building and running containers. A container is an isolated process with the application files and dependencies it needs, while sharing the host operating system’s kernel.

Applications can behave differently across computers because runtimes, libraries, and configuration differ. Docker images describe repeatable application environments. Running an image creates a container, helping make development and deployment more consistent.

## Key terms

- **Docker Engine:** Builds and runs containers.
- **Image:** A read-only template used to create containers.
- **Container:** A running or stopped instance of an image.
- **Registry:** A service for storing and distributing images.

Containers are not full virtual machines. They are useful for local development, testing, and deploying services.

Next: [Docker Images and Containers](02-Images-and-Containers.md).
