
# Docker Basics

docker image = executable package that includes everything needed to run an application - the code, a runtime, libraries, environment variables, and config files. 

docker container = a runtime instance of an image

Docker images contain layers. When you run it as a container it adds a writable layer on top. 
Bottom layer is Manifest. Next is OS layer, stating which OS to use. Next is config changes such as host name. Next is maybe applications you wish to install etc etc. 
Lastly is the writeable layer that is created when you run the image as a container. 

Dockerfile = textfile that contains all commands in order needed to build a given image. Uses `docker build` command to execute. 

### Dockerfile commands

ADD - coppies a file into the image but supports tar and remote URL
COPY - copy files into the image, preferred over ADD
VOLUME - creates a mount point as defined when the container is run
ENTRYPOINT - The executable runs when a container is run 
EXPOSE - documents the ports that should be published
CMD - provides arguments for the entrypoint (only one is allowed)
ENV - used to define environmental variables in the container
FROM - defined the base image; the from instruction must be first line in dockerfile
MAINTAINER - legacy, used to provide email of image maker
ONBUILD - only used as a trigger when the image is used to build other images; will define commands to run on "on build"
RUN - runs a new command layer
WORKDIR - defined working directory of the container

`docker image history` = shows history of image layers. 

`docker image rm` + imageID removes image
`docker rmi` does the same
`docker image prune` removes all dangling images. 
`docker image prune -a` removes all images without at least 1 container associated with them. 

## Docker Storage and Volumes

Issues with storing data inside containers
* Containers are designed to be disposable
* When containers are stopped, data is not accessible
* Containers are typically stored on each host - not globally 
* The container filesytem wasn't designed for high performance i/o

#### Options for Data Storage with Containers

- Volumes
    * The recommended way to persist data, stored at /var/lib/docker/volumes/
- Bind Mounts
    * Have limited functionality + must use exact file path. Less preferred option. 
- tmpfs mounts
    * Stored only at host's memory in Linux. Least preferred option. 
