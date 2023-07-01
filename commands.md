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

# Docker Swarm - Commands

* `docker swarm init` is the command to create a new swarm. The node that you run the command on becomes the first manager and is switched to run in swarm mode.
* `docker swarm join-token` reveals the commands and tokens needed to join workers and managers to existing swarms. To expose the command to join a new manager, use the docker swarm join-token manager command. To get the command to join a worker, use the docker swarm join-token worker command.

* `docker node ls` lists all nodes in the swarm including which are managers and which is the leader.

* `docker service create` is the command to create a new service.

* `docker service ls` lists running services in the swarm and gives basic info on the state of the service and any replicas it’s running.

* `docker service ps <service>` gives more detailed information about individual service replicas.

* `docker service inspect` gives very detailed information on a service. It accepts the --pretty flag to limit the information returned to the most important information.

* `docker service scale` lets you scale the number of replicas in a service up and down.

* `docker service update` lets you update many of the properties of a running service.

* `docker service logs `lets you view the logs of a service.
docker service rm is the command to delete a service from the swarm. Use it with caution as it deletes all service replicas without asking for confirmation.