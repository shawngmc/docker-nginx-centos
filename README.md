# docker-nginx-centos7

Nginx docker image based on the centos 7 official image and using the latest nginx from the CentOS 7 repo. Based off of Chentex's repo at https://github.com/chentex/docker-nginx-centos

## What is Nginx?
Nginx (pronounced "engine x") is a web server. It can act as a reverse proxy server for HTTP, HTTPS, SMTP, POP3, and IMAP protocols, as well as a load balancer and an HTTP cache.

See: [Nginx](http://Nginx.org/)

## What is inside of this repo?
In this git repository you will find the docker image definitions for Nginx 1.16.x in centos 7.

## How do I use this images?
To use this images you must do as follows:

```
# latest tag is the only generally populated one, as there should be only minor patch differences between versions 
docker pull shawngmc/docker-nginx-centos:latest

# to run the image just execute
docker run -d -p 80:80 shawngmc/docker-nginx-centos:latest

# to run the with a volume for /data/www
docker run -d -p 80:80 -v /custom/volume/path:/data/www shawngmc/docker-nginx-centos:latest
```

You will have now a docker container running nginx on centos you can look for it with

```
docker ps
```

You can log into the container with this command

```
docker exec -ti <container-id> bash
```

## How do I build this images?
First things first, you can find these docker images in `shawngmc/docker-nginx-centos`
but you can also build a specific version on your own, you only need:

- docker

Clone this repo

`git clone https://github.com/shawngmc/docker-nginx-centos.git`

Go to the folder in your terminal and type this:

```
# Then build the new image
docker build -f Dockerfile .
```

If you want to tag your image use the following command

```
docker build -f Dockerfile -t yourbase/yourname:version .
```
---
For more on docker build reference to the [Documentation](https://docs.docker.com/engine/reference/commandline/build/)

You can get the source from the images in the [Repository](https://github.com/shawngmc/docker-nginx-centos)
