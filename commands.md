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

Checking docker status `service docker status`, `systemctl is-active docker`

Building a image `docker image build -t web:latest .`

Changing tag of image `docker image tag web:latest nigelpoulton/web:latest`

Pushing image to default registry `docker image push soaib024/web:latest`

History of docker build `docker image history web:latest`

Image inspect `docker image inspect`