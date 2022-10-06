# Helm - Basics

## Where ? 

```
artifacts helm 
https://artifacthub.io/
```
## components  

```
Chart - contains description and components 
tar.gz - Format 
or a folder

when executen a chart a release will be created.
(parallel: image -> container, analog: chart -> release 
```

## Installation 

```
# Beispiel ubuntu 
# snap install --classic helm

# Cluster muss vorhanden, aber nicht notwendig wo helm installiert 

# Voraussetzung auf dem Client-Rechner (helm ist nichts als anderes als ein Client-Programm) 
Ein lauffähiges kubectl auf dem lokalen System (welches sich mit dem Cluster verbinden.
-> saubere -> .kube/config 

# Test
kubectl cluster-info 

```

