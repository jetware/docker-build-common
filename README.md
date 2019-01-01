

Commond scripts and templates for the automated building of images for Docker Hub

Base OS images are built using https://github.com/jetware/docker-base_os


The 'build-common' should be placed as a submodule to the DockerHub Auto Build project with symlbolic links in the root of the project targeting to 'hooks' and 'Dockerfile': 

ln -s build-common/hooks
ln -s build-common/Dockerfile
