# Real World Example with mysql 

```
# 01-configmap.yml 
kind: ConfigMap
apiVersion: v1
metadata:
  name: mysql-configmap
data:
  # als Wertepaare
  MYSQL_ROOT_PASSWORD: abcmaster
# 03-pod-mit-env.yml
kind: Pod
apiVersion: v1
metadata:
  name: mysql
spec:
  containers:
    - name: mysql
      image: mysql:5.7
      envFrom:
        - configMapRef:
            name: mysql-configmap


```
