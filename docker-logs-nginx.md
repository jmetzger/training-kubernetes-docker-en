# Docker logs (Nginx) 

## in general 
```
# start nginx and container-id will be shown  
docker run -d nginx 
a234
docker logs a234 # a234 are first 4 chars of container id 
```

## ongoing Log-output 

```
docker logs -f a234 
# stop ->  CTRL + c 
```
