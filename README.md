# scribeui-docker
ScribeUI Dockerfile

ScribeUI v1.8 with MapServer and Apache.

Reference : http://mapgears.github.io/scribeui/
GitHub : https://github.com/mapgears/scribeui

The image is based on Ubuntu 14.04 Trusty.
The demo data was loaded into the image.
The image is configured to run in production (in Apache).

1- Start in background:

docker run --name scribeui -p 8080:80 -d christianbeland/scribeui-docker

2- Attach to running container:

docker ps

docker exec -it CONTAINER_ID bash

3- Edit /opt/scribeui/local.ini and modify to set the url:port on the following lines:

cgi.url = http://your_site_domain.com:8080/cgi-bin
mapserver.url = http://your_site_domain.com:8080/cgi-bin/mapserv

4- Start Apache service:

/etc/init.d/apache2 start

5- Browse to http://your_site_domain.com:8080/scribeui/


Note: Password for the default workspace is 'default'.