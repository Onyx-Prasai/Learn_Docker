# Publishing to Docker Hub

[Back to the learning guide](../README.md)

Docker Hub is a registry for storing and sharing container images. Create a repository, authenticate with Docker, tag the image with your Docker Hub username and repository, then push it:

```sh
docker login
docker build -t YOUR_DOCKERHUB_USERNAME/my-node-app:1.0 .
docker push YOUR_DOCKERHUB_USERNAME/my-node-app:1.0
```

Replace the placeholder with your username. Avoid putting access tokens in shell history or source files. On another machine, retrieve the image with `docker pull YOUR_DOCKERHUB_USERNAME/my-node-app:1.0`.

Next: [Layering in Docker Images](12-Image-Layers.md).
