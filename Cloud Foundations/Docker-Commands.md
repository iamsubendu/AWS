# Docker commands

## docker info

To get docker details and also its working for us or not

## docker pull hello-world:latest

To download a dockerized image

We can find out the images in Docker Hub

docker pull packageName:tagName

if we don't use tagName, by default it will use latest

![alt text](image-12.png)

## docker images

To see all the images in our container

![alt text](image-13.png)

docker images hello-world -> to see specific image

## docker container run hello-world/ docker run hello-world

To run a image

Container run specifies we want to run the container

## docker ps

To see actively running processes

## docker ps -a/--all

To see all the processes

![alt text](image-14.png)

if we don't give names while running a container, it will by default give a name to the container

## docker container run --name subendu hello-world

naming the container

![alt text](image-15.png)

## docker container run --name hellow-web-instance-1 -p 3333:80 nginxdemos/hello

-p -> port mapping

3333:80 -> port for owr(host) machine: port for docker(guest) machine

    In guest machine its running on port 80<br>
    For accessing that port we also need a port

![alt text](image-16.png)

![alt text](image-17.png)

![alt text](image-18.png)

## docker container run --name hellow-web-instance-2 -d -p 3334:80 nginxdemos/hello

returns long format of containerId

-d -> detached mode

With this, we can use the same terminal with the process running

![alt text](image-19.png)

## docker container logs containerId

To see the logs of any container

![alt text](image-20.png)

## docker kill/stop containerId

To kill any process

We can add multiple containerId seprated by spaces

## docker run -d -p 30:80 yeasy/simple-web:latest

![alt text](image-21.png)

On this, the image was not found locally, so it checked in docker hub if present.
After found, it started downloading and started in detached mode

![alt text](image-22.png)

## docker remove containerId

To remove a container

We can add multiple containerId seprated by spaces
