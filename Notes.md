# Workshop Kubernetes

## Was ist Kubernetes? (K8s)
    - Container Orchustrieungssystem
        - automatische Konfiguration
                       Verwaltung
                       Koordination

## Ziel von Containerorchustrierung
    - High Availablity (wenig bis keine Downtime)

    - Scalability (Performance hoch halten)

    - Disaster recovery (schneller und datenverlust freie Recovery)

## Architektur von K8s / von einem K8s-Cluster
    - Meine von Servern in einem privaten Netzwerk
        - 1 Server = 1 Node
    
    - 2 Arten von Nodes
        - Worker Node
        - Control Plane Nodes (ehemalig Master Nodes)
    
    - Auf jedem Node müssen mindestens 2 Programme installiert sein:
        - Container Runtime (z.B. docker, containerd)
        - kubelet (Kubernetes-Binary)

## Bausteine von K8s

### Pod
    - Container Abstraktion
    - kleine Unit im Cluster
    - enthält die Anwendung
    - in der Regel: 1 Pod = 1 Container
    - temporäre interne IPs

### Service
    - Exposed eine Pod über eine permanente IP
    - Jedoch noch keinen Support HTTPS oder DNS-Lookups (Urls)

### Ingress
    - Exposed Service an die Außerwelt
    - vergleichbar Reverse Proxy
    - automatische HTTPS integeration möglich

### Deployment
    - Abstraktion über einen Pod
    - Replika von meinem Container (horizontal Skalieren)
    - Updatemachanismen
    - Resource Limits
    - Mounten von Volumes an einem Pod

### Volume
    - Persistenter Filestorage
    - nicht managed von Kubernetes
    - quasi eine externe Festplatte, die mans Cluster hängt

### StatefulSet
    - Äquvivalent zu einem Deployment für Anwendungen mit State
    - Optionen für den zeitgleichen Zugriff auf Daten
    - sehr komplex und nicht so empfehlenswert

## K8s Manifeste
    - Kubernetes ist declarativ
    - Man beschreibt einen Endzustand und Kubernetes kümmert sich um die Umsetzung
    - Manifeste sind yaml-Datein

## Setup eines Clusters

- nginx-ingress-controller:
https://www.digitalocean.com/community/tutorials/how-to-set-up-an-nginx-ingress-on-digitalocean-kubernetes-using-helm
- cert-manager
  https://cert-manager.io/docs/installation/

## Erstes Deployment

## Deployment via GitOps

## CI/CD einer eigenen App

## Euer Code
