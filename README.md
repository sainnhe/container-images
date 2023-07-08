# Introduction

This repository contains my personal builds of some container images. These images are built with small in mind, thus are very suitable for CI.

Here is a quick comparison of my builds of node and redis to the official images:

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

As you can see, they are much smaller than the official debian based images, and are even smaller than the official alpine based images!

## List of images

These images support multiple architectures and will be built on schedule, you can pull them from the following registries:

- [`ghcr.io`](https://github.com/sainnhe?tab=packages&repo_name=container-images)
- [`quay.io`](https://quay.io/user/sainnhe)

Available tags:

- `sainnhe/build-tools:clang`
- `sainnhe/build-tools:gcc`, `sainnhe/build-tools:latest`
- `sainnhe/clang:latest`
- `sainnhe/cmake:latest`
- `sainnhe/gcc:latest`
- `sainnhe/git:latest`
- `sainnhe/hugo:latest`
- `sainnhe/mdbook:latest`
- `sainnhe/node:current`, `sainnhe/node:latest`
- `sainnhe/node:lts`
- `sainnhe/redis:latest`
- `sainnhe/vercel:latest`

## License

[MIT](./LICENSE) © sainnhe
