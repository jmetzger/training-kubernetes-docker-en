# Ubuntu mit ping 

```
# create a build folder 
cd 
mkdir myubuntu 
cd myubuntu/
```
```
# nano Dockerfile
FROM ubuntu:latest
RUN apt-get update; apt-get install -y inetutils-ping
CMD ["/bin/bash"]
```


docker build -t myubuntu .
docker images
# -t is needed to run in the background 
# also with -d (ohne -t) the bash is being executed, but  "the terminal" is stopped 
# -> the container stops to run.
docker run -d -t --name container-ubuntu myubuntu
docker container ls
# enter the container by name myubuntu 
docker exec -it container-ubuntu bash
ls -la
``` 
 
``` 
# Zweiten Container starten
docker run -d -t --name container-ubuntu2 myubuntu 

# docker inspect to find out ip of other container 
# 172.17.0.3 
docker inspect <container-id>

# Ersten Container -> 2. anpingen 
docker exec -it container-ubuntu bash 
# Jeder container hat eine eigene IP 
ping 172.17.0.3

 
```
