# Introduction

This repository contains my personal builds of some container images, the following images are included:

## node && redis

The size of these two images are very very small, they are even smaller than the official alpine based images:

```shell
$ sudo docker images --format "{{.Repository}}:{{.Tag}}    {{.Size}}" | grep node
sainnhe/node:18    67.4MB
sainnhe/node:16    61.1MB
node:16-alpine    111MB
node:18-alpine    164MB
node:16    853MB
node:18    939MB

$ sudo docker images --format "{{.Repository}}:{{.Tag}}    {{.Size}}" | grep redis
sainnhe/redis:7    9.87MB
redis:7-alpine    28.2MB
redis:7    111MB

$ uname -a
Linux lima-fedora 5.18.17-200.fc36.aarch64 #1 SMP PREEMPT_DYNAMIC Thu Aug 11 13:58:26 UTC 2022 aarch64 aarch64 aarch64 GNU/Linux

$ docker --version
Docker version 20.10.17, build 100c701
```

They are available in the following repositories:

- [docker.io/sainnhe/redis](https://hub.docker.com/r/sainnhe/redis/tags)
- [docker.io/sainnhe/node](https://hub.docker.com/r/sainnhe/node/tags)
- [ghcr.io/sainnhe/redis](https://github.com/sainnhe/minimal-container-images/pkgs/container/redis)
- [ghcr.io/sainnhe/node](https://github.com/sainnhe/minimal-container-images/pkgs/container/node)

Available tags:

- `sainnhe/node:16`, `sainnhe/node:lts`
- `sainnhe/node:18`, `sainnhe/node:current`, `sainnhe/node:latest`
- `sainnhe/redis:7`, `sainnhe/redis:latest`

Supported architectures:

- `linux/386`
- `linux/amd64`
- `linux/arm/v6`
- `linux/arm/v7`
- `linux/arm64/v8`
- `linux/ppc64le`
- `linux/s390x`

## mdbook

Repository:

- [docker.io/sainnhe/mdbook](https://hub.docker.com/r/sainnhe/mdbook/tags)
- [ghcr.io/sainnhe/mdbook](https://github.com/sainnhe/minimal-container-images/pkgs/container/mdbook)

Available tags:

- `sainnhe/mdbook:latest`

Supported architectures:

- `linux/386`
- `linux/amd64`
- `linux/arm/v6`
- `linux/arm/v7`
- `linux/arm64/v8`
- `linux/ppc64le`

## hugo

Repository:

- [docker.io/sainnhe/hugo](https://hub.docker.com/r/sainnhe/hugo/tags)
- [ghcr.io/sainnhe/hugo](https://github.com/sainnhe/minimal-container-images/pkgs/container/hugo)

Available tags:

- `sainnhe/hugo:latest`

Supported architectures:

- `linux/386`
- `linux/amd64`
- `linux/arm/v6`
- `linux/arm/v7`
- `linux/arm64/v8`
- `linux/ppc64le`
- `linux/s390x`

## License

[MIT](./LICENSE) © sainnhe
