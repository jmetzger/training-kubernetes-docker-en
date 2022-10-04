# Ubuntu HelloWorld 

## Simple Version 

```
## Step 1:
cd 
mkdir Hello-World 
cd Hello-World

## Step 2:
# nano Dockerfile
FROM ubuntu:latest 

COPY hello.sh .
RUN chmod u+x hello.sh
CMD ["/hello.sh"]

## Step 3:
nano hello.sh 
#!/bin/bash
echo hello-docker

## Step 4:
# docker build -t dockertrainereu/<your-name>-hello-docker . 
# Example
docker build -t dockertrainereu/<your-name>-hello-docker .
docker images
docker run dockertrainereu/<your-name>-hello-docker 

```


```
docker login
user: dockertrainereu 
pass: --bekommt ihr vom trainer--

# docker push dockertrainereu/<your-name>-hello-docker 
# z.B. 
docker push dockertrainereu/<your-name>-hello-docker

# and look if we find it 
# in browser
https://hub.docker.com/u/dockertrainereu 
```

## Advanced Version 

```
## Schritt 1:
cd 
mkdir Hello-World 
cd Hello-World

## Schritt 2:
# nano Dockerfile
FROM ubuntu:latest 

COPY hello.sh .
RUN chmod u+x hello.sh
CMD ["/hello.sh"]

## Schritt 3:
nano hello.sh 
#!/bin/bash
while true
do 
  echo hello-docker
done 

## Schritt 4:
# docker build -t dockertrainereu/<dein-name>-hello-docker . 
# Beispiel
docker build -t dockertrainereu/jm-hello-docker .
docker images
docker run -d -t --name hello dockertrainereu/<dein-name>-hello-docker 
docker exec -it hello sh 

docker login
user: dockertrainereu 
pass: --bekommt ihr vom trainer--

# docker push dockertrainereu/<dein-name>-hello-docker 
# z.B. 
docker push dockertrainereu/jm-hello-docker

# und wir schauen online, ob wir das dort finden

```
