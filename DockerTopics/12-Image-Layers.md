# Layering in Docker Images

[Back to the learning guide](../README.md)

Docker images are built from layers. Docker can reuse layers from previous builds, and images can share layers from the same base image. This saves storage and can make builds faster through caching.

Order instructions from less frequently changed to more frequently changed when practical. For example, copy package manifests and install dependencies before copying source code. A source edit can then reuse the dependency layer:

```dockerfile
COPY package*.json ./
RUN npm ci --omit=dev
COPY . .
```

Exclude unnecessary files with `.dockerignore`. Do not store credentials in image layers: deleting a secret in a later instruction does not remove it from an earlier layer.

Next: [Volume Mounting](13-Volume-Mounting.md).
