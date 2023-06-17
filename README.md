# Kubernetes Cheat sheet

### Core Components

## 1. PODS: 
Its smallest unit of the K8s and its abstraction over the container. So, its similar to docker container.
Usually pod contains one or more containers inside the pod.
K8s offers inbuilt networking to the pods and each pod has its own IP address

## 2. Service:
On dedicated IP addresses assigned to the application.
a. Internal service
b. External service (we use ingress in real life for external service which has powerful advantages)

## 3. configMap:
its external configuration for the applications. Good examples to "How application connects to the database"
Config Map is plan text format. Its not safe to store credentials, thats why we use secrets.

## 4. Secretes:
We is to store secretes in base64 encoded format.

## 5. Volumes:
this is to have persistent storage to the application. Even though application restarted/pod replaced, application data is persistent since its load it from system Hard disk instead of loading it from inside the container.

## 6. Deployment
its helpful when application is crashed, to minimized downtime, we replicate the application into multiple nodes. Those replicas we control through deployment of the application. In simply we deploy the blueprint of application on multiple nodes, so that when one pod got crashed, other replica will serve the traffic. 

## 7. Stateful set
Its similar to deployment, however when deploying the databases, we use stateful set which require state of the pods. This stateful helps to avoid data in-synchronizations and data in consistency due to pod crashes.

[a link](KubernetesArch.md)