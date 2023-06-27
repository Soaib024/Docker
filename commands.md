List down all docker images `docker image ls`

Pulling docker image `docker image pull ubuntu:latest`

Running a container `docker container run -it ubuntu:latest /bin/bash`

Attaching bash to existing container `docker container exec -it <container id/name> bash`

Building a image from dockerfile `docker image build -t test:latest .`

Stopping a running container `docker container stop vigilant_borg`

Removing a running container `docker container rm vigilant_borg`

Pulling a image `docker image pull redis:latest`

Docker info `docker info`

Pulling a image `docker image pull <repository>:<tag>` 

Filtering docker image ls `docker image ls --filter dangling=true`

checking docker status `service docker status`, `systemctl is-active docker`