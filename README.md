# AlpineLinux + Java + Docker [![Build Status](https://travis-ci.org/simeg/docker-alpine-java-docker.svg?branch=master)](https://travis-ci.org/simeg/docker-alpine-java-docker)
This image is based on [AlpineLinux](https://alpinelinux.org/) and has Bash, Java 8 (JDK/JRE) and Docker installed.

## JDK vs. JRE
>JDK 8 is a superset of JRE 8, and contains everything that is in JRE 8, plus tools such as the compilers and debuggers necessary for developing applets and applications. JRE 8 provides the libraries, the Java Virtual Machine (JVM), and other components to run applets and applications written in the Java programming language. Note that the JRE includes components not required by the Java SE specification, including both standard and non-standard Java components.

(Source: [Oracle](http://docs.oracle.com/javase/8/docs/))

## Usage
```
docker run -it -v $(pwd):/docker-images simeg/alpine-java-docker /bin/sh 
```
This command will fire up a container with the current folder (`$(pwd)`) mounted as `/docker-images`  and use bash (`/bin/sh`) as the entrypoint. Inside the container you can now access any local images.

## Docker inside of Docker?!
I needed this for an application that required a running DB instance during it's build process. I'm not the first one to think of this, you can read more about [Docker in Docker (dind) here](https://github.com/jpetazzo/dind).

