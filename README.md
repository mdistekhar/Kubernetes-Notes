#Kubernetes in One Shot
This README is a comprehensive guide for "Kubernetes in One Shot." It contains categorized commands from your history, structured by core Kubernetes topics. Each command is briefly described for ease of understanding and use.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Core Concepts
Monolithic vs Microservices, Kubernetes Architecture
kubectl cluster-info
Display cluster information to understand the Kubernetes architecture.
Setup On Local/AWS EC2
kind create cluster --name=tws-cluster --config=config.yml
Create a Kubernetes cluster using Kind with a specific configuration.
kubectl config use-context kind-tws-cluster
Switch the context to the Kind cluster.
Kubectl and Pods
kubectl get nodes
List all nodes in the Kubernetes cluster.
kubectl run nginx --image=nginx -n nginx
Create a pod named nginx in the nginx namespace.
kubectl describe pod nginx -n nginx
Display detailed information about the nginx pod.
Namespaces, Labels, Selectors, Annotations
kubectl create namespace monitoring
Create a namespace for monitoring resources.
kubectl get namespace
List all namespaces in the cluster.
kubectl label namespace monitoring team=devops
Add a label to the monitoring namespace.
kubectl describe namespace monitoring
Display detailed information about the monitoring namespace.
