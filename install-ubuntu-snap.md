# Install docker (ubuntu) with snap

```

sudo su -
snap install docker

# for information retrieval 
snap info docker
systemctl list-units
systemctl list-units -t service
systemctl list-units -t service | grep docker

systemctl status snap.docker.dockerd.service
# oder (aber veraltet) 
service snap.docker.dockerd status

systemctl stop snap.docker.dockerd.service
systemctl status snap.docker.dockerd.service
systemctl start snap.docker.dockerd.service 

# is the docker service being started on next book (autostart in windows) 
systemctl is-enabled snap.docker.dockerd.service

```
