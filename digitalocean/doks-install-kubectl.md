# Install and configure kubectl with doks 

## what is doks ? 

  * Managed digital ocean kubernetes cluster 

## Step 1: Setup Cluster online 

```
https://cloud.digitalocean.com/kubernetes/clusters/new
* 3 nodes 
* at least 8 GB Ram per Node
* No HA for the control plan 

Takes a while till it ready... take some coffee 
```



## Step 2: Install and configure client  

```
# on an ubuntu machine using it as client
# being root - user 
snap install --classic kubectl 
kubectl completion bash > /etc/bash_completion.d/kubectl
# relogin for the config to take effect
su - 
```
