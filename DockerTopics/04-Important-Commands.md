# Important Docker Commands

[Back to the learning guide](../README.md)

```sh
docker pull nginx                 # Download an image
docker images                     # List local images
docker run --name web -d nginx    # Create and start a container
docker ps                         # List running containers
docker ps -a                      # List all containers
docker logs web                   # Read container output
docker exec -it web sh            # Open a shell, if available in the image
docker stop web                   # Stop a running container
docker start web                  # Start an existing container
docker rm web                     # Remove a stopped container
docker rmi nginx                  # Remove a local image
```

Use `docker <command> --help` to see options for your installed version. A container must be stopped before it can normally be removed.

Next: [Docker vs. Virtual Machines](05-Docker-vs-VMs.md).
