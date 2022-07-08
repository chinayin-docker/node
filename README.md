# nodejs

[![Docker Image CI](https://github.com/chinayin-docker/node/actions/workflows/ci.yml/badge.svg?event=schedule)](https://github.com/chinayin-docker/php/actions/workflows/ci.yml)
![Docker Image Version (latest semver)](https://img.shields.io/docker/v/chinayin/node?sort=semver)
![Docker Image Size (latest semver)](https://img.shields.io/docker/image-size/chinayin/node?sort=semver)
![Docker Pulls](https://img.shields.io/docker/pulls/chinayin/node)

Node.js is a JavaScript-based platform for server-side and networking applications.

### Supported tags and respective `Dockerfile` links

![](https://img.shields.io/docker/v/chinayin/node/14)
![](https://img.shields.io/docker/v/chinayin/node/16)
![](https://img.shields.io/docker/v/chinayin/node/18)

![](https://img.shields.io/docker/v/chinayin/node/14-slim)
![](https://img.shields.io/docker/v/chinayin/node/16-slim)
![](https://img.shields.io/docker/v/chinayin/node/18-slim)

### Image Variants

- `node:<version>`
- `node:<version>-slim`

### Usage

You can use the image directly, e.g.

```
docker run --rm -it chinayin/node:16
```

The images are built daily and have the security release enabled, so will contain any security updates released more
than 24 hours ago.

You can also use the images as a base for your own Dockerfile:

```
FROM chinayin/node:16
```

[ref](https://github.com/nodejs/docker-node)
