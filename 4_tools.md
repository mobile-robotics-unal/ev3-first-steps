# Tools, Programming languages, libraries and APIs

<!--
APIs y lenguajes de programación: Identificar las APIs o librerías disponibles para programar los
robots. Enumerar los lenguajes de programación compatibles con los robots.
-->

## ROS 
### Prerequisites
In order to work with ROS in the EV3 you will need Docker and get the image from docker hub

```
docker pull ev3dev/debian-stretch-cross
```

Add a tag to the image for ease of usage

```
docker tag ev3dev/debian-stretch-cross ev3cc
```

Or you can create a dockerfile for extended configuration

```
docker build -t ev3dev .
```
And then run it
```
docker run -i  --rm --name production_container -t  ev3dev:latest  
```

We created a .devcontainer to develop with vscode inside the container

Once inside the container you can use to compile the code
```
arm-linux-gnueabi-gcc -o hello hello.c
```

```
qemu-arm-static -L /usr/arm-linux-gnueabi/ ./hello
```


## References

1. [ROS Robot With Lego EV3 and Docker blogpost](https://www.instructables.com/ROS-Robot-With-Lego-EV3-and-Docker/)
2. [Docker for cross compilation ](https://www.ev3dev.org/docs/tutorials/using-docker-to-cross-compile/)
3. [ev3 docker](https://hub.docker.com/u/ev3dev)