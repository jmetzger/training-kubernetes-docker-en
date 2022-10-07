# Exercise runasuser 

## Note:

```
USER does not need to exist on the system.
The settings

securityContext:
  runasuser: 12000
  
overwrites the settings under which the docker container runs
Directive: USER 

BUT: Problems will occur when docker cannot start the software defined by ENTRYPOINT
or CMD and the contaner stops and cannot be started 
```

## Example 1: (normal mit root) 

```
# Schritt 1: 
# mkdir runtest 
# cd runtest 
# vi 01-privileged.yml 
apiVersion: v1
kind: Pod
metadata:
  name: ubsi1
spec:  
  containers:
  - name: bb
    image: ubuntu
    command: ["/bin/bash"]
    tty: true
    stdin: true
```

```
# Schritt 2:
# Ausführen 
kubectl apply -f 01-privileged.yml 
kubectl exec -it ubsi1 -- bash 
# id 
```

## Example 2: (als nobody: 65534)

```
# Step 1: 
# mkdir runtest 
# cd runtest 
# vi 02-nobody-privileged.yml 
apiVersion: v1
kind: Pod
metadata:
  name: ubsi2
spec:
  securityContext:
    runAsUser: 65534 
  containers:
  - name: bb
    image: ubuntu
    command: ["/bin/bash"]
    tty: true
    stdin: true
```

```
# Step 2:
# Execute 
kubectl apply -f 01-nobody-privileged.yml 
kubectl exec -it ubsi2 -- bash 
# id 
# touch testfile 
# ls -la 
```

## Example 3: (as 1001 - user does not exist) 

```
# Step 1: 
# mkdir runtest 
# cd runtest 
# vi 03-user-1001.yml 
apiVersion: v1
kind: Pod
metadata:
  name: ubsi3
spec:
  securityContext:
    runAsUser: 1001  
  containers:
  - name: bb
    image: ubuntu
    command: ["/bin/bash"]
    tty: true
    stdin: true
```

```
# Step 2:
# Execute 
kubectl apply -f 03-user-1001.yml 
kubectl exec -it ubsi3 -- bash 
# id 
# touch testfile 
# ls -la 
```

## Example 4: including group 

```
# Schritt 1:                                                                                             
# mkdir runtest 
# cd runtest 
# vi 04-user-group-1001.yml 
apiVersion: v1
kind: Pod 
metadata:
  name: ubsi4
spec:
  securityContext:
    runAsUser: 1001  
    runAsGroup: 1001
  containers:
  - name: bb
    image: ubuntu
    command: ["/bin/bash"]
    tty: true
    stdin: true
 
```
