# Using Containers to Build a Node.js Application

[Back to the learning guide](../README.md)

Create a Node.js project with a `package.json` and an entry point such as `server.js`:

```js
const http = require('node:http');

const server = http.createServer((_request, response) => {
  response.end('Hello from Node.js in Docker!');
});

server.listen(3000, '0.0.0.0');
```

The `0.0.0.0` binding allows connections through the container interface. Add a start script such as `"start": "node server.js"` to `package.json`. Once it runs locally, package the app with a [Dockerfile](09-Dockerfile.md) and use [port mapping](06-Ports-and-Environment-Variables.md) to reach it from the host.
