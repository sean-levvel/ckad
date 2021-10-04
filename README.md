# ckad udemy


# General notes
- Popular ingress contollers
    ```
    Ambassador: API Gateway based on Envoy with community/commercial support from Datawire
    Voyager: HAProxy based Ingress Controller from AppsCode
    Contour: Envoy based Ingress Controller from Heptio (acquired by VMWare)
    Gloo: Envoy based API Gateway with enterprise support from solo.io
    Citrix: Ingress Controller for MPX, VPX, and CPX ADC products
    F5: Supports F5’s BIG-IP Container Ingress Services
    HAProxy: Community-driven HAProxy Ingress Controller as well as enterprise offering from HAProxy Tech
    Istio: Ingress Gateway for Istio-enabled clusters
    Kong: nginx-based API gateway with community/enterprise options from KongHQ
    NGINX: official Ingress for NGINX and NGINX Plus
    Skipper: HTTP router and reverse proxy from Zalando
    Traefik: HTTP reverse proxy with commercial support from Containous
    ```


# Section 1

## CKAD Exam
- entire documentation is available to you during the exam. 

# Secction 2

## Core Concepts
- Kubernetes installs
    - api server
        - acts as the front end, user commands, UI, 
    - etcd
        - distributed reliable key-value store used by kubernetes key value store, used by kuber, used to managed the cluster
        - implementing logs within the clusters
    - kublet
        - agent that runs on each node on the cluster. 
    - container runtime
        - is the underlying software that is used to run containers. In our case its docker
    - controller
        - brain behinds orchestration. They are responsible for noticing and responding when nodes, containers, or end points go down. 
    - scheduler
        - distributing work or containers across multiple nodes. looks for newly created containers and assigns them to nodes.

## Pods 
- Pod is the smallest thing you can create in kubernetes pod. 
- scale up create more pod, scale down, delete pods
- multiple conitainers can live in a pod - helper containers 
- `kubectl get pods` 
- `kube run nginx --image nginx`

## Yaml in Kubernetes - Pods
- 