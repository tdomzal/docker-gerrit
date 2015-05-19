docker-gerrit
=============

Build a Docker container with the gerrit code review system

The current files will build an image that is based on the ubuntu:trusty
image. the images includes:

  * supervisord
  * Gerrit 2.9 using the H2 storage backend

The following ports are exposed in the image:

  * 8080/tcp (http) - Gerrit Web interface
  * 29418/tcp (ssh) - The restricted gerrit ssh daemon

Forked from [https://github.com/edgester/docker-gerrit](https://github.com/edgester/docker-gerrit).

## Building the image

To build the image run the "./build".

To run normally as a daemon, run "./run" or the following command:

	sudo docker run -p 127.0.0.1:8080:8080 -p 127.0.0.1:29418:29418 -d tdomzal/gerrit

To use gerrit after starting the container, go to [http://localhost:8080](http://localhost:8080) and login with an OpenID service, like Google, Yahoo, or Launchpad. The first person to login is the administrator and may create users and projects.

Source files for this image are at [https://github.com/tdomzal/docker-gerrit](https://github.com/tdomzal/docker-gerrit).