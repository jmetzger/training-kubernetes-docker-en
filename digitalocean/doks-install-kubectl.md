# Install and configure kubectl with doks 

## what is doks ? 

  * Managed digital ocean kubernetes cluster 

## Walkthroug 

```
# on an ubuntu machine using it as client
# being root - user 
snap install --classic kubectl 
kubectl completion bash > /etc/bash_completion.d/kubectl
# relogin for the config to take effect
su - 
```
