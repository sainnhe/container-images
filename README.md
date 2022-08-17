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

Simply pull them from docker hub or github container registry:

- [docker.io/sainnhe/redis](https://hub.docker.com/r/sainnhe/redis/tags)
- [docker.io/sainnhe/node](https://hub.docker.com/r/sainnhe/node/tags)
- [ghcr.io/sainnhe/redis](https://github.com/sainnhe/minimal-container-images/pkgs/container/redis)
- [ghcr.io/sainnhe/node](https://github.com/sainnhe/minimal-container-images/pkgs/container/node)

## Is this ready for production?

Nope.

Currently this is more like an idea instead of a project for production. The idea behind it can be widely used in other images, so we can make more small images instead of just these two.

If people like this idea and would like to contribute, then it will turn into a real project for production and will get long-term support, but if no one like this idea then it will turn into my personal project and get very limited support. Personally I will continue to use them, bugs will be handled and the images will be rebuilt to receive the latest updates every week, and I may add some new images for my personal use, however I can't guarantee long-term support in the future.

But for now, I think it's usable enough for your personal projects.

The binary itself comes from the official repo of alpine 3.16 so it should be stable enough. And the entry point files are based on those from the official docker images.

So far, I use them to run some CI and deploy some services on my raspberry pi 4, everything works fine.

## License

[MIT](./LICENSE) © sainnhe
