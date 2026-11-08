# Dockerization of a Node.js Application (Dockerfile)

[Back to the learning guide](../README.md)

A Dockerfile contains instructions for building an image. For the sample app from [the Node.js lesson](08-Node-Application.md), create `Dockerfile` in the project root:

```dockerfile
FROM node:22-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --omit=dev
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
```

Use a Node version supported by your application. `npm ci` expects a lockfile; if there is no lockfile, create one or use an appropriate install step. Add `.dockerignore` to keep local dependencies and unnecessary files out of the build context:

```text
node_modules
.git
npm-debug.log
```

Build and run:

```sh
docker build -t my-node-app:1.0 .
docker run --rm --name node-app -p 3000:3000 my-node-app:1.0
```

`EXPOSE` documents the container port; `-p` publishes it on the host. Next: [Docker Compose](10-Docker-Compose.md).
