# Fix for restarting docker-compose container 

```
cd
cd Hello-World/
cp -a * /root/bautest/myubuntu/
cd
cd bautest/
docker-compose down
docker-compose build
docker-compose up -d 
# check what is going on 
docker container ls 
```
