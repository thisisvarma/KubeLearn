# Kubernetes Architectures

## Container runtime
Which run the containers 

*[Yes]* Need to Install on all servers? 

## kubelet
kubelet interacts with containers and node and it starts a container in the pod. 

*[Yes]* Need to Install on all servers? 

## Kubeproxy
its redirects the traffic based on the cluster usage. Its intelligent enough.

*[Yes]* Need to Install on all servers? 

## control plane

## 1. API Server
It validates the every request and process it and schedule the pod. 

## 2. Scheduler
Once API server validates the request, scheduler schedules the pods on the worker nodes based on resources.

## 3. Controller manager
Detects cluster changes, and reschedule/restart pods etc..

## 4. etcd
The key value store of the cluster. We call it as cluster brain. 
