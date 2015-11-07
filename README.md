# ScribeUI
ScribeUI v1.8 with MapServer and Apache.

[![DockerPulls](https://img.shields.io/docker/pulls/christianbeland/scribeui-docker.svg)](https://hub.docker.com/r/christianbeland/scribeui-docker/)
[![DockerStars](https://img.shields.io/docker/stars/christianbeland/scribeui-docker.svg)](https://hub.docker.com/r/christianbeland/scribeui-docker/)

Reference : http://mapgears.github.io/scribeui/

GitHub : https://github.com/mapgears/scribeui

The image is based on Ubuntu 14.04 Trusty.
The demo data was loaded into the image.
The image is configured to run in production (in Apache).

To start in background:
```
docker run --name scribeui -p 8080:80 -e "SCRIBEUI_URL=your_site_domain.com:8080" -d christianbeland/scribeui-docker apachectl -D FOREGROUND
```
To attach to running container:
```
docker ps
docker exec -it CONTAINER_ID bash
```

To use, browse to **http://your_site_domain.com:8080/scribeui/**

Note: Password for the default workspace is 'default'.
