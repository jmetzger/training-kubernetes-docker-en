# Kubernetes Netzwerk (CNI) 

## CNI 

  * Common Network Interface
  * fixed Definition, how containers with network libraries are communicating
  * 
## Docker - Container oder andere 

  * Container is started -> over CNI -> get pod-ip 
  * Container is stopped -> over CNI -> pod - IP is released 

## Which are there ? 

  * Flanel
  * Canal 
  * Calico 
  * Cilium 
  
## Flanel

### Overlay - Network 

  * virtuelles Netzwerk was sich oben drüber und eigentlich auf Netzwerkebene nicht existiert
  * VXLAN 

### Advantage

  * good and easy start
  * reduced to only one binary flanneld 

### Disadvantages 

  * no network policies allowed 
  * hard to debug, because no classical network (virtual), cannot use classic network tools

## Canal 

### General 

  * Auch ein Overlay - Netzwerk 
  * Unterstüzt auch policies 

## Calico

### Generally 

  * klassische Netzwerk (BGP)

### Vorteile gegenüber Flannel 

  * Policy über Kubernetes Object (NetworkPolicies)

### Vorteile 

  * ISTIO integrierbar (Mesh - Netz) 
  * Performance etwas besser als Flannel (weil keine Encapsulation)

### Referenz 
  * https://projectcalico.docs.tigera.io/security/calico-network-policy

## Cilium 

## microk8s Vergleich 

  * https://microk8s.io/compare

```
snap.microk8s.daemon-flanneld
Flannel is a CNI which gives a subnet to each host for use with container runtimes.

Flanneld runs if ha-cluster is not enabled. If ha-cluster is enabled, calico is run instead.

The flannel daemon is started using the arguments in ${SNAP_DATA}/args/flanneld. For more information on the configuration, see the flannel documentation.
```
