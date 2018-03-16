# Python Installer

[![Docker Automated build](https://img.shields.io/docker/automated/srault95/python-installer.svg)](https://hub.docker.com/r/srault95/python-installer/) [![Docker Stars](https://img.shields.io/docker/stars/srault95/python-installer.svg)](https://hub.docker.com/r/srault95/python-installer)

**Dockerize PyInstaller and Python portable for create binaries projects.**

> This project depends of https://github.com/srault95/python-binary

## Docker Build

```
$ docker build -t srault95/python-installer:py27 -f Dockerfile .
$ docker build -t srault95/python-installer:py35 -f Dockerfile_py35 .
$ docker tag srault95/python-installer:py35 srault95/python-installer:latest
```

## Example for building python-fabric

```
# see build-fabric-py2.sh

$ docker run -it --rm -v $PWD:/app srault95/python-installer:py27 /app/build-fabric-py2.sh

$ ./dist/fab --version

$ ldd dist/fab
        linux-vdso.so.1 =>  (0x00007fffd539e000)
        libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007f2abac45000)
        libz.so.1 => /lib/x86_64-linux-gnu/libz.so.1 (0x00007f2abaa2b000)
        libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f2aba661000)
        /lib64/ld-linux-x86-64.so.2 (0x00007f2abae49000)
```
