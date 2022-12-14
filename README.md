# Kubernetes and Docker Administration  

## Agenda 

  1. Docker-Basics 
     * [Overview Architecture](architektur.md)
     * [What is a container ?](container.md)
     * [What are container images](container-images.md) 
     * [Container vs. Virtual machines](container-vs-vm.md)
     * [What is a Dockerfile](dockerfile.md) 
  
  1. Docker-Installation
     * [Installation Docker under Ubuntu with snap](install-ubuntu-snap.md)
  
  1. Docker-Commands 

     * [The most important commands](docker-befehle.md)
     * [docker run](docker-run.md)
     * [Logs anschauen - docker logs - mit Beispiel nginx](docker-logs-nginx.md)
     * [Docker container/image stoppen/löschen](container-image-delete.md)
     * [Docker containerliste anzeigen](container-liste.md)
     * [Docker container analysieren](docker-inspect.md)
     * [Docker container in den Vordergrund bringen - attach](/docker/docker-attach.md) 
     * [Aufräumen - container und images löschen](prune-container-images.md)
     * [Nginx mit portfreigabe laufen lassen](docker-example-nginx.md)    
  
  1. Dockerfile - Examples 
     * [Ubuntu mit hello world](ubuntu-hello-world.md)
     * [Ubuntu mit ping](ubuntu-ping.md) 
     * [Nginx mit content aus html-ordner](nginx-html-content.md)
     * [ssh server](ubuntu-ssh-server.md)
  
  1. Docker-Container Examples 
     * [2 Container mit Netzwerk anpingen](2-containers-with-network-ping.md)
     * [Container mit eigenem privatem Netz erstellen](container-with-own-bridge.md)  
  
  1. Docker-Daten persistent machen / Shared Volumes 
     * [Überblick](storage-overview.md) 
     * [Volumes](storage-volumes.md) 
  
  1. Docker-Netzwerk 
     * [Netzwerk](network.md)
  
  1. Docker Compose
     * [yaml-format](yaml-format.md)
     * [Ist docker-compose installiert?](docker-compose-installed.md) 
     * [Example with Wordpress / MySQL](example-wordpress-mysql.md)
     * [Example with Wordpress / Nginx / MariadB](example-wnm-docker-compose.md)
     * [Example with Ubuntu and Dockerfile](example-docker-compose-ubuntu-build.md)
     * [Logs in docker - compose](docker-compose-logs.md)
     * [docker-compose und replicas](docker-compose-replicas.md)
  
  1. Docker Swarm 
     * [Docker Swarm Beispiele](docker-swarm-examples.md)

  1. Docker - Dokumentation 
     * [Vulnerability Scanner with docker](https://docs.docker.com/engine/scan/#prerequisites)
     * [Vulnerability Scanner mit snyk](https://snyk.io/plans/)
     * [Parent/Base - Image bauen für Docker](https://docs.docker.com/develop/develop-images/baseimages/)
    
  1. Kubernetes - Überblick
     * [Why Kubernetes, what is kubernetes doing](warum-kubernetes.md) 
     * [Architecture](/kubernetes/architecture.md)
     * [Aufbau mit helm,OpenShift,Rancher(RKE),microk8s](/kubernetes/aufbau-helm-microk8s-kubernetes.md)
     * [Welches System ? (minikube, micro8ks etc.)](welches-system.md)
     * [Installation - Welche Komponenten from scratch](/kubernetes/installation-components-overview.md)

  1. Kubernetes - Installer - microk8s (Installation und Management) 
     * [Installation Ubuntu - snap](microk8s/installation-ubuntu-snap.md)
     * [Patch to next major release - cluster](microk8s/patch-next-major.md)
     * [Remote-Verbindung zu Kubernetes (microk8s) einrichten](microk8s/connect-from-remote.md)
     * [Create a cluster with microk8s](microk8s/cluster.md)
     * [Ingress controller in microk8s aktivieren](microk8s/ingress.md) 
     * [Arbeiten mit der Registry](microk8s/registry.md)
     * [Installation Kubernetes Dashboard](/microk8s/dashboard.md) 

  1. Kubernetes - doks (digitaloean) (Installation and Management) 
     * [Setup Cluster with kubectl client](/digitalocean/doks-install-kubectl.md)

  1. Kubernetes - Installer - Rancher 
     * [Installation on digitalocean](/rancher/setup-on-digitalocean.md) 

  1. Kubernetes Praxis API-Objekte 
     * [Das Tool kubectl (Devs/Ops) - Cheatsheet](/kubectl/spickzettel.md)
     * [kubectl example with run](/kubectl/run-with-example.md)
     * Arbeiten mit manifests (Devs/Ops)
     * Pods (Devs/Ops)
     * [kubectl/manifest/pod](/kubectl-examples/01-pod-nginx.md)
     * ReplicaSets (Theorie) - (Devs/Ops)
     * [kubectl/manifest/replicaset](/kubectl-examples/01a-replicaset-nginx.md)
     * Deployments (Devs/Ops)
     * [kubectl/manifest/deployments](/kubectl-examples/03-nginx-deployment.md)
     * [Services - Structure](/kubernetes/services-aufbau.md)
     * [kubectl/manifest/service](/kubectl-examples/03b-service.md)
     * DaemonSets (Devs/Ops)
     * IngressController (Devs/Ops)
     * [Background IngressController](/kubernetes/ingress.md)
     * [Documentation for default ingress nginx](https://kubernetes.github.io/ingress-nginx/user-guide/nginx-configuration/configmap/)
     * [Beispiel Ingress](/kubectl-examples/04-ingress-nginx.md)
     * [Install Ingress On Digitalocean DOKS](/digitalocean/ingress-auf-digitalocean-mit-helm.md)
     * [Ingress Example with  hostnames](/kubectl-examples/04-ingress-nginx-with-hostnames.md)
     * [Achtung: Ingress mit Helm - annotations](/ingress-mit-helm-class-achtung.md)
     * [Permanente Weiterleitung mit Ingress](/kubectl-examples/05-ingress-permanent-redirect.md)
     * [ConfigMap Example](/kubectl-examples/06-configmap.md)

  1. Kubernetes - RBAC 
     * [Nutzer einrichten](/kubernetes/rbac-create-user.md) 
 
  1. Kubernetes - Netzwerk (CNI's) + Mesh 
     * [Übersicht Netzwerke](/kubernetes-networks/overview.md) 
     * [Callico - nginx example](/kubernetes-network/callico/00-simple-example.md)
     * [Callico - client-backend-ui-example](/kubernetes-network/callico/01-example-with-services.md)
     * [Mesh - istio as a type of implementation](sammlung-istio.md)
   
  1. Kubernetes - Monitoring (microk8s und vanilla) 
     * [metrics-server aktivieren (microk8s und vanilla)](/microk8s/metrics-server.md)
     * [prometheus](/monitoring/prometheus)
     * [checkmk plugin](https://docs.checkmk.com/latest/de/monitoring_kubernetes.html)
    
  1. Kubernetes - Shared Volumes 
     * [Shared Volumes with nfs](shared-volumes/nfs.md)
     * [Shared Volumes with nfs/multipe](/shared-volumes/nfs-multiple.md)

  1. Kubernetes - Backups 
     + [Kubernetes Aware Cloud Backup - kasten.io](/backups/cluster-backup-kasten-io.md)

  1. Kubernetes - Wartung 
     * [kubectl drain/uncordon](/kubectl/uncordon-drain.md)
     * [Alte manifeste konvertieren mit convert plugin](/kubectl/convert-plugin.md)

  1. Kubernetes Probes (Liveness and Readiness) 
     * [Übung Liveness-Probe](/probes/uebung-liveness.md)
     * [Funktionsweise Readiness-Probe vs. Liveness-Probe](/probes/readiness.md) 
 
  1. configmaps / secrets 
     * [configmap](/kubectl-examples/06-configmap.md)
     * [configmap-mysql-realworld example](/kubectl-examples/07-configmap-mysql-realworld.md)
     * [Working with secrets](uebung-secrets.md)
     * [Bitnami](/secrets/sealed-secrets.md)
   
  1. Helm (Kubernetes Package Manager) 
     * [Basics](/helm/basics.md)
     * [Example with kubernetes package manager](/helm/example.md)
  
  1. Kustomize 
     * [Kustomize Exercise/Example](/kustomize/02-overlay-example.md) 
     * [Marriage between helm and kustomize](/kustomize/helm-kustomize-options.md)
  
  1. Kubernetes - Tipps & Tricks 
     * [Assigning Pods to Nodes](/tipps-tricks/pods-2-nodes.md) 
     * [Kubernetes debugging ClusterIP/PodIP](/tipps-tricks/cluster-ip-debug.md)
     * [Debugging pods](tipps-tricks/debugging-pods.md)

  1. Kubernetes - Documentation 
     * [Documentation zu microk8s plugins/addons](https://microk8s.io/docs/addons)
     * [LDAP-Anbindung](https://github.com/apprenda-kismatic/kubernetes-ldap)
     * [Shared Volumes - Welche gibt es ?](https://kubernetes.io/docs/concepts/storage/volumes/)
     * [Helpful to learn - Kubernetes](https://kubernetes.io/docs/tasks/)
     * [Environment to learn](https://killercoda.com/killer-shell-cks)
     * [Youtube Channel](https://www.youtube.com/watch?v=01qcYSck1c4)
     * [Defining defaultBackend for IngressController](https://dev.to/kenmoini/custom-kubernetes-ingress-default-backend-and-error-pages-3alh)

  1. Kubernetes -Wann / Wann nicht 
     * [Kubernetes Wann / Wann nicht](kubernetes/wann-kubernetes-wann-nicht.md)

  1. Kubernetes - Hardening 
     * [Kubernetes Tipps Hardening](kubernetes-security/tipps-hardening.md)
     * [Kubernetes run as non root](security/uebung-runasuser.md)
     * [Kubernetes find unprivileged images](security/find-unprivileged-containers.md)
    
  1. Kubernetes Deployment Scenarios 
     * [Deployment green/blue,canary,rolling update](/kubernetes/deployment-strategies-en.md)
    
  1. Linux und Docker Tipps & Tricks allgemein 
     * [Auf ubuntu root-benutzer werden](sudo.md)
     * [IP - Adresse abfragen](ip-a.md)
     * [Hostname setzen](hostname.md)
     * [Proxy für Docker setzen](proxy-docker.md)
     * [vim einrückung für yaml-dateien](/vim/vim-yaml.md)
     * [YAML Linter Online](http://www.yamllint.com/)
     * [Läuft der ssh-server](ssh-running.md)
     * [Basis/Parent - Image erstellen](docker-base-image.md)
     * [Eigenes unsichere Registry-Verwenden. ohne https](insecure-registry.md)
