# Aufbau 

## Diagram 

![Kubernetes Architecture - src: syseleven](https://www.syseleven.de/wp-content/uploads/2020/11/syseleven-webiste-loesungen-kubernetes-modell-800x400-web.jpg)

## Components

### Master (Control Plane)

#### Tasks / Jobs

  * The master coordinates all the activities within the cluster
    * planning of applications (deployment of those)
    * management of the desired state of the applications
    * scaling of the applications 
    * rollout of new updates.

#### componnents of the master 

##### etcd

  * management of the cluster configuration (key/value - pairs) 
  
##### kube-controller-manager  
  
  * in charge of monitoring the state of the cluster with endless loops 
  * communicated with the cluster through the kubernetes-api (provided by the kube-api-server)

##### kube-api-server 

  * provides api-frontend for administration (no gui)
  * Exposes an HTTP API (users, parts of the cluster and external components communicate with it)
  * REST API
 
##### kube-scheduler 

  * assigns Pods to Nodes. 
  * scheduler determines which Nodes are valid placements for each Pod in the scheduling queue 
    ( according to constraints and available resources )
  * The scheduler then ranks each valid Node and binds the Pod to a suitable Node. 
  * Reference implementation (other schedulers can be used)
 
### Nodes  

  * Nodes are workers (machines), that execute applications 
  * Ref: https://kubernetes.io/de/docs/concepts/architecture/nodes/

### Pod/Pods 

  * pods are the smalles usable unit, that can be created and managed 
  * a pod (=group) is a group of one or more containers
    * they usage mutual storage and network ressources   
    * they are always on the same physical/virtual server  
    
## Control Plane Node (former: master) - components 

## Node (Minion) - components 

### General 

  * On the nodes we will rollout the applications

### kubelet

```
Node Agent that runs on every node (worker) 
Er stellt sicher, dass Container in einem Pod ausgeführt werden.
```

### Kube-proxy 

  * runs on every node  
  * = network proxy for the kubernetes-network-services.
  * Kube-proxy manages the network communication inside and (to/from) the outside of the cluster
 
## source: 

  * https://www.redhat.com/de/topics/containers/kubernetes-architecture

