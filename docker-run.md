# Docker run 

## Example (bind it to a terminal), detached

```
# before that we did
docker pull ubuntu:xenial
docker run -t -d --name my_xenial ubuntu:xenial
# will wollen überprüfen, ob der container läuft
docker container ls 
# image is there 
docker images

# exec in /into container
docker exec -it my_xenial bash 
docker exec -it my_xenial cat /etc/os-release
# 

```
