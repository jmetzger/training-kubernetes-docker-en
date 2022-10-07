# Simple Example Calico 

```
# Schritt 1:
kubectl create ns policy-demo<tln>
kubectl create deployment --namespace=policy-demo<tln> nginx --image=nginx
kubectl expose --namespace=policy-demo<tln> deployment nginx --port=80
# lassen einen 2. pod laufen mit dem auf den nginx zugreifen 
kubectl run --namespace=policy-demo<tln> access --rm -ti --image busybox /bin/sh
```
```
# within the shell 
wget -q nginx -O -
```


```
# Schritt 2: create policy, that no ingress traffic is allowed at all 
# in this namespace: policy-demo 
# mkdir network; cd network 
# vi 01-policy.yml
kind: NetworkPolicy
apiVersion: networking.k8s.io/v1
metadata:
  name: default-deny
  namespace: policy-demo<tln>
spec:
  podSelector:
    matchLabels: {}
```


```
kubectl apply -f 01-policy.yml 
```

```
# run a  2. pod who wants to access nginx 
kubectl run --namespace=policy-demo<tln> access --rm -ti --image busybox /bin/sh
```

```
# within the shell 
# no access possible
wget -q nginx -O -
```

```
# Schritt 3: Allow access for pods having the label run=access
# 02-allow.yml
kind: NetworkPolicy
apiVersion: networking.k8s.io/v1
metadata:
  name: access-nginx
  namespace: policy-demo<tln>
spec:
  podSelector:
    matchLabels:
      app: nginx
  ingress:
    - from:
      - podSelector:
          matchLabels:
            run: access
```


```
kubectl apply -f 02-allow.yml 
```

```
# run a 2. pod and access nginx  
# using run + name: access for pod -> automatically has label run:access 
kubectl run --namespace=policy-demo<tln> access --rm -ti --image busybox /bin/sh
```

```
# inside the shell 
wget -q nginx -O -
```

``` 
kubectl run --namespace=policy-demo no-access --rm -ti --image busybox /bin/sh
```

```
# in der shell  
wget -q nginx -O -
```

```

kubectl delete ns policy-demo 

```
