# Python Installer

**Dockerize PyInstaller and Python 2.7 portable for create binaries projects.**

## Docker Build

```
$ docker build -t srault95/python-installer:py27 .
```

## Exemple for build python-fabric

```
# see build-fabric.sh

$ docker run -it --rm -v $PWD:/app srault95/python-installer:py27 /app/build-fabric.sh

$ ./dist/fab --version
```
