# Oracle Java on a Raspberry Pi 3, via Docker, deployed with Resin.io

I'm currently working on a java project that I want to be able deploy to a Raspberry Pi 3 using [Resin.io](http://Resin.io).
Resin.io currently has base docker images that support java, but they all use OpenJDK, which I found to be abysmally slow.
My search then took me to images that install the Oracle JDK from the [Ubuntu WebUpd8 PPA](https://launchpad.net/~webupd8team/+archive/ubuntu/java), but 
this required that I use a Debian variant for the base OS, and I was trying to keep my download time to a minimum. This brought
me to building a Docker image on top of Alpine Linux, and only bringing in the JRE from the official Oracle JDK.

By the end of it, I had my docker image down to 172MB (from a start of 318M with raspian Jessie and the PPA) by switching to
Alpine linux, adding in glibc for Oracle Java, then downloading Java 8 and stripping out everything but the JRE.

This also resulted in startup time dropping from ~200s to ~2s for launching a simple dropwizard based web service.

Have a look! https://github.com/dsmyth/docker-alpine-java-raspberrypi3
