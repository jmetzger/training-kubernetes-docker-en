# Container - Image - Delete - Kill

```
# stop it 
docker stop my_xenial 
docker container ls -a 


# start it 
docker start my_xenial 
docker container ls 

# Kill it if it cannot be stopped -be careful
docker kill my_xenial

# Works only, if container is not running
docker rm my_xenial

# remove container when running (force) 
docker rm -f my_xenial  

# delete image
docker rmi ubuntu:xenial 

# if container is present but not running
docker rmi -f ubuntu:xenial 

```
