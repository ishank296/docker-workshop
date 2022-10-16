# docker-workshop
Docker-workshop


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
