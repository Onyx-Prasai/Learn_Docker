# Port Mapping and Setting Environment Variables

[Back to the learning guide](../README.md)

## Port mapping

A process listening inside a container is not automatically reachable from the host. Publish a container port with `-p hostPort:containerPort`:

```sh
docker run --name web -d -p 8080:80 nginx
```

Visit `http://localhost:8080`. The first port is on the host; the second is inside the container. Publishing to `127.0.0.1:8080:80` limits access to the local machine.

## Environment variables

Pass configuration when starting a container with `-e`:

```sh
docker run --name app -e NODE_ENV=production my-node-app
```

Avoid putting passwords or other secrets directly into image layers or source control. Use an appropriate secret-management method for production.

Next: [Troubleshooting Containers](07-Troubleshooting.md).
