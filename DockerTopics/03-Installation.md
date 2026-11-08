# Installation of Docker CLI and Desktop

[Back to the learning guide](../README.md)

Docker installation depends on your operating system. Docker Desktop provides a managed local environment for Windows and macOS and includes Docker CLI tools. On Linux, Docker Engine and the CLI can be installed using the distribution’s supported instructions.

1. Follow the official [Docker Desktop installation guide](https://docs.docker.com/desktop/).
2. Start Docker Desktop or the Docker Engine service.
3. Open a terminal and check the installation:

```sh
docker --version
docker info
docker run hello-world
```

On Windows, some configurations use WSL 2 as the backend. Follow Docker’s current instructions for your Windows edition and WSL setup.

Next: [Important Docker Commands](04-Important-Commands.md).
