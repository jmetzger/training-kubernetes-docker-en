# Use curl from within a pod 

## Situation 

  * No access to the nodes, to test the connection to pods and services

## Solution  

```
# using busybox (swiss army knife of embedded)
# busytester is the name  
# long version 
kubectl run -it --rm --image=busybox busytester 
# wget <pod-ip-des-ziels> 
# exit 


# quick and dirty 
kubectl run -it --rm --image=busybox busytester -- wget <pod-ip-des-ziels>  

```
