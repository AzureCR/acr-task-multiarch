# ACR Tasks Samples for Multi-arch builds

ACR Tasks can be used to build Linux,Windows or ARM (using QEMU) images. 
A multi-arch manifest can be used to help build an image manifest that can point to images of different architectures and variants. The docker client when pulling the image determines the approprate images.

This repo contains a sample Task that builds  an ARM and AMD64 image which is then used to construct a multi-arch manifest. 
The multi-arch manifest is created using the [`docker manifest`](https://docs.docker.com/edge/engine/reference/commandline/manifest/) command. 

1. [acr-task.yaml](acr-task.yaml) uses 2 docker files to create 2 images and push the tags and multi-arch tag as well. 
2. [acr-task-composed.yaml](acr-task-composed.yaml) Creates a docker file during execution and uses that to build the images. 
