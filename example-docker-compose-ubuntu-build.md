# Example Docker Compose (Ubuntu with Dockerfile) 

```
cd
mkdir bautest
cd bautest 
```

```
# nano docker-compose.yml
version: "3.8"

services:
  myubuntu:
    build: ./myubuntu
    restart: always
```

```
mkdir myubuntu 
cd myubuntu 
```

```
# nano Dockerfile 
FROM ubuntu:latest
RUN apt-get update; apt-get install -y inetutils-ping
CMD ["/bin/bash"]
```

```
cd ../
# wichtig, im docker-compose - Ordner seiend 
#pwd 
#~/bautest
docker-compose up -d 
# image is being created and container started  

# When Dockerfile changes you have to use the parameter --build
docker-compose up -d --build 
```
