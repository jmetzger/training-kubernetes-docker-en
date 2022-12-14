# Collection istio 

## Overview 

![Architecture](https://istio.io/latest/docs/ops/deployment/architecture/arch.svg)

## Istio 

```
# Visualization 
# with kiali (included in istio) 
https://istio.io/latest/docs/tasks/observability/kiali/kiali-graph.png

# Example 
# https://istio.io/latest/docs/examples/bookinfo/
The sidecars are injected in all pods within the namespace by labeling the namespace like so:
kubectl label namespace default istio-injection=enabled

# Gateway (like Ingress in vanilla Kubernetes) 
kubectl label namespace default istio-injection=enabled
```

## Visualization of Services (kiali - included in istio)

![Kiali Visualization](https://istio.io/latest/docs/tasks/observability/kiali/kiali-graph.png)


## istio - the next generation without sidecar 

  * https://istio.io/latest/blog/2022/introducing-ambient-mesh/
