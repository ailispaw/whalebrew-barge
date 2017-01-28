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
Welcome to Barge 2.3.5, Docker version 1.13.0, build 49bf474
[bargee@barge ~]$ sudo -E whalebrew install whalebrew/whalesay
Unable to find image 'whalebrew/whalesay' locally
Using default tag: latest
latest: Pulling from whalebrew/whalesay
e190868d63f8: Pull complete
909cd34c6fd7: Pull complete
0b9bfabab7c1: Pull complete
a3ed95caeb02: Pull complete
00bf65475aba: Pull complete
c57b6bcc83e3: Pull complete
8978f6879e2f: Pull complete
8eed3712d2cf: Pull complete
Digest: sha256:c6e9ea15126cfb12d0377111e18019a692a2358eee2f1653ee981bbe67a0dfd4
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
