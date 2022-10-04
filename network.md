# Network 

## Overview

```
3 types 

o none
o bridge (Standard-network) 
o host 

## Additionally possible to install
o overlay (needed for multi-node)

```


## command

```
# show networks 
docker network ls 

# show bridged network  
# also show the ips of the container  
docker inspect bridge

# network from the container perspective 
docker inspect ubuntu-container 

```

## create network 

```
docker network create -d bridge test_net 
docker network ls 

docker container run -d --name nginx --network test_net nginx
docker container run -d --name nginx_no_net --network none nginx 

docker network inspect none 
docker network inspect test_net 

docker inspect nginx 
docker inspect nginx_no_net 

```

## delete network /  

```
docker network disconnect none nginx_no_net
docker network connect test_net nginx_no_net 

## Das Löschen von Netzwerken ist erst möglich, wenn es keine Endpoints 
## d.h. container die das Netzwerk verwenden 
docker network rm test_net 
```


