# docker-workshop
Docker-workshop

## reference : 
- https://docker-curriculum.com/#webapps-with-docker
- https://github.com/Vizuri/docker-exercises
- https://learndocker.online/courses/ 
- https://labs.play-with-docker.com/


Docker Commands

## list images -
      docker image ls 
      docker images
## list running containers -
      docker ps
## list containers including stopped containers
      docker ps -a
## starting a new container
      docker   run -dit --name web debian
        - i : interactive
        -d : detach
        - t : open tty session
      -- rm : automatically removes the containter when it exits
## stop a  running container
      docker stop web
## remove a container
      docker rm web
## inspect container policy
      docker inspect web
## force stop a container
      docker kill web
## show docker logs
      docker logs -f web  (follow log output)
      docker logs -t web (show timestamp)
## start shell of a running container
      docker exec -it 239a /bin/bash
## check exposed ports of a docker container
      docker ports static-site

## Sample Docker run for PostgreSQL and RabbitMQ
      docker run --name postgres-db -p 5432:5432 -e POSTGRES_PASSWORD=xxxxx -d postgres
      docker run --name rabbit-mq --hostname rmq -p 5672:5672 -p 15672:15672 -e RABBITMQ_DEFAULT_USER=admin -e RABBITMQ_DEFAULT_PASS=xxxxx  -d rabbitmq:3.11-management
      
## Docker volumes : local host directory can be mapped to new/existing directory of docker container using -v handle
      docker run -it --name test1 -v C:\Users\ishan\Documents\docker_test:/data alpine
      
      
## Docker shorthands with full commands

- docker pull=docker image pull
- docker create=docker container create
- docker start=docker container start
- docker ps=docker container ps
- docker run=docker create;docker start
- docker rmi=docker image rm
- docker rm=docker container rm


## Dockerfile for python project

- FROM python base image
- WORKDIR working directory
- COPY files to container
- RUN installation of libraries and modules
- EXPOSE ports
- ENV environment variables
- LABEL
- ENTRYPOINT start-up commands
- CMD ... and its arguements
