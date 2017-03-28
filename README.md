# Whalebrew on Barge

https://github.com/bfirsh/whalebrew
> Whalebrew creates aliases for Docker images so you can run them as if they were native commands. It's like Homebrew, but everything you install is cleanly packaged up in a Docker image.

## Requirements

- [VirtualBox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)

## Boot up

```bash
$ vagrant up
```

That's it.

## Hello World

```bash
$ vagrant ssh
Welcome to Barge 2.4.3, Docker version 17.03.1-ce, build c6d412e
[bargee@barge ~]$ sudo -E whalebrew install whalebrew/whalesay
Unable to find image 'whalebrew/whalesay' locally
Using default tag: latest
latest: Pulling from whalebrew/whalesay
627beaf3eaaf: Pull complete
393e7670a5d3: Pull complete
a24b8e210a6f: Pull complete
9556b59f5c1d: Pull complete
Digest: sha256:9df31cc255ae8ce802f4e9615c055da864213c1c7d265d40273b03b4dc4f9b15
Status: Downloaded newer image for whalebrew/whalesay:latest
🐳  Installed whalebrew/whalesay to /opt/bin/whalesay
[bargee@barge ~]$ whalesay Hello, world!
 _______________
< Hello, world! >
 ---------------
    \
     \
      \
                    ##        .
              ## ## ##       ==
           ## ## ## ##      ===
       /""""""""""""""""___/ ===
  ~~~ {~~ ~~~~ ~~~ ~~~~ ~~ ~ /  ===- ~~~
       \______ o          __/
        \    \        __/
          \____\______/
```
