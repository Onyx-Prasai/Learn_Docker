# Troubleshooting Containers

[Back to the learning guide](../README.md)

Start by checking the container state, logs, and port configuration:

```sh
docker ps -a
docker logs --tail 100 <container>
docker inspect <container>
docker port <container>
docker exec -it <container> sh
```

Common checks:

- **Container exits:** Read its logs and check the configured command and required environment.
- **Cannot reach the app:** Confirm the app listens on `0.0.0.0` inside the container and the correct port is published.
- **Port already in use:** Choose a different host port or stop the process using it.
- **Image or build issue:** Check the image tag, build output, and Dockerfile paths.
- **Data disappeared:** Check whether the application writes to a mounted volume or only to the container filesystem.

Next: [Using Containers to Build a Node.js Application](08-Node-Application.md).
