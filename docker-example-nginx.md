# Beispiel nginx 

## Internal ip 

```
docker run --name test-nginx -d -p 8080:80 nginx

docker container ls
lsof -i
cat /etc/services | grep 8080
curl http://localhost:8080
docker container ls
# wenn der container gestoppt wird, keine ausgabe mehr, weil kein webserver
docker stop test-nginx 
curl http://localhost:8080

```

## External 

```
docker run --name test-nginx -d -p 8080:80 nginx 
lsof -i 
cat /etc/services | grep 8080

# ip - address ? -> e.g. 134.209.247.10 
ip a 

# use browser on local machine (our desktop) 
# and open <ip> http://<ip>:8080 

# after the stop docker container docker, it is exposing anymore
docker stop test-nginx 
# browser will complain 
```
