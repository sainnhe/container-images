## What's this?

This is yet another build of some commonly used container images, which are very small, even smaller than the official alpine based images.

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

## Amazing! How did you do that?

Most of the official images are built by downloading the source code and then compiling, or directly downloading the compiled tarballs and extracting them.

However, this build method does not actually take full advantage of Alpine Linux, instead the Alpine Linux team also built these softwares but optimized specifically for Alpine Linux that are smaller most of the time.

This project directly uses the packages in the official Alpine Linux repository to build container images.

## Good. How can I try them?

Simply pull them from docker hub.

- [sainnhe/redis](https://hub.docker.com/r/sainnhe/redis/tags)
- [sainnhe/node](https://hub.docker.com/r/sainnhe/node/tags)

## License

[MIT](./LICENSE) © sainnhe
