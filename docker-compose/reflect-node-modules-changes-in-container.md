# Reflect `node_modules` changes in container

When using a Docker container for a Node.js application and the `node_modules` are bundled into the container the container is not updated when using `docker-compose build`.

Example `Dockerfile`:

```Dockerfile
FROM node

COPY package.json /my/app/

RUN cd /my/app && npm install

WORKDIR /my/app
```

There is a [Github issue](https://github.com/docker/compose/issues/4337#issuecomment-358459746) describing the problem which is about anonymous volumes.

The if is using the `-V` CLI flag like this:

```bash
docker-compose up --build -V
```
