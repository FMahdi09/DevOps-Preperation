# DevOps

## Containers

### Containers vs VMs

Different containers share the host operating system.
They can also share binaries and libraries and are not dependant on a hypervisor.
(copies and modifications of a container share the libraries with the original one)

Because they dont need their own operating system, containers need much less overhead and are faster to resart.

On VMs every duplicate or modification of an application needs their own Guest OS while in a containerized enviroment, everything runs on the same operating system (assuming all containers are able to run on the same OS) and can even share bins and libs.

### Docker File

Is a text document which holds instructions on how to build an image.

It holds the same commands a user would type into the CLI to install and start the application.

### Docker Image

Product of a Dockerfile.

Similiar to an executeable, in the sense that it can be started to run a container.

### Container

A running instance of a image.

It is an isolated and selfcontained process on the host, which contains all software, configs and bins to function.

On removal all data the container contains is removed.

### Volumes

Data storage on the host OS, that containers are given access to.

If a container is deleted everything in the container is aswell.
Volumes used by these containers persist. 

### Docker Deamon

Gets its commands from a docker client.

Builds images from docker files, builds and runs containers from images and manages volumes.

Listens for requests from a docker client.