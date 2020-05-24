## To run docker start-up images
docker run hello-world
==> docker run converts any images to container

## To run images into an interactive terminal, which helps in running the terminal commands in images
docker run -ti <image-name:version-number> bash

## To see images which are either running or not running
docker images

## To see images which are running
==> If an image is running then it is wrapped inside the container
docker ps
==> In "docker ps" output, command option refers to the command that is running inside the image

Example:
If I run a command "docker run -ti ubuntu:latest bash"
then docker ps returns a container that contains that running image and in its output, command represents "bash" which shows the command running in this image.


Note: Whenever we execute docker run command then it creates a new container, and commands executed in first container is not reflected in new container.

## To see all containers, use -a flag where a stands for All
docker ps -a

## To see last exited container use
docker ps -l

## Till now we have seen how to create container from images

## Now lets look at how to convert a container to image.
## This can be used when we have done some changes to container and want to save it into an image
docker commit <container-ID>
==> This gives new image id

Now if we want to rename this image id then use
==> docker tag <generated image-id from container> <new-image name>


docker commit <Name column in `docker ps` output> <new image name>
==> this one single command is equivalent to
1. docker commit <container-ID>
2. docker tag <image-id> <new image name>
