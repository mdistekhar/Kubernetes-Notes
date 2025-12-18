# Kubernetes in One Shot

This README is a comprehensive guide for **Kubernetes in One Shot**. It contains categorized Kubernetes commands, structured by core topics, with brief explanations for quick understanding and hands-on usage.

---

## Core Concepts

### Monolithic vs Microservices, Kubernetes Architecture

```bash
kubectl cluster-info
```

Displays cluster information to understand the Kubernetes control plane and overall architecture.

---

## Setup on Local / AWS EC2

### Create a Kind Cluster

```bash
kind create cluster --name=tws-cluster --config=config.yml
```

Creates a Kubernetes cluster using **Kind** with a custom configuration file.

### Switch kubectl Context

```bash
kubectl config use-context kind-tws-cluster
```

Switches kubectl to use the Kind cluster context.

---

## Kubectl and Pods

### List Cluster Nodes

```bash
kubectl get nodes
```

Lists all nodes participating in the Kubernetes cluster.

### Create an Nginx Pod

```bash
kubectl run nginx --image=nginx -n nginx
```

Creates a Pod named `nginx` in the `nginx` namespace.

### Describe a Pod

```bash
kubectl describe pod nginx -n nginx
```

Shows detailed information about the specified Pod, including events and container status.

---

## Namespaces, Labels, Selectors, and Annotations

### Create a Namespace

```bash
kubectl create namespace monitoring
```

Creates a namespace for isolating monitoring-related resources.

### List Namespaces

```bash
kubectl get namespace
```

Lists all namespaces in the cluster.

### Add a Label to a Namespace

```bash
kubectl label namespace monitoring team=devops
```

Applies a label to the `monitoring` namespace for organization and selection.

### Describe a Namespace

```bash
kubectl describe namespace monitoring
```

Displays metadata, labels, annotations, and status of the namespace.

---

## Notes

* This guide focuses on **essential Kubernetes commands** used in real-world setups.
* Best suited for **beginners to intermediate learners** practicing on Kind or AWS EC2.
* Extend this README with Deployments, Services, Ingress, ConfigMaps, and Helm as next steps.

---

Happy Learning Kubernetes 🚀
