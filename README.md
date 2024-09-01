Here’s a `README.md` for the Kubernetes cheat sheet:

---

# Kubernetes Cheat Sheet

This cheat sheet provides a quick reference to common Kubernetes commands and operations, helping you manage your clusters, pods, services, and other resources efficiently.

## Table of Contents
- [Basic Commands](#basic-commands)
- [Pod Management](#pod-management)
- [Deployment Management](#deployment-management)
- [Service Management](#service-management)
- [Namespace Management](#namespace-management)
- [ConfigMap & Secret Management](#configmap--secret-management)
- [Persistent Volume & Persistent Volume Claim](#persistent-volume--persistent-volume-claim)
- [Ingress Management](#ingress-management)
- [Miscellaneous](#miscellaneous)

---

## Basic Commands

- **Check Cluster Info**: 
  ```sh
  kubectl cluster-info
  ```
- **List Nodes**:
  ```sh
  kubectl get nodes
  ```
- **List Pods**:
  ```sh
  kubectl get pods
  ```
- **List Services**:
  ```sh
  kubectl get svc
  ```
- **List Deployments**:
  ```sh
  kubectl get deployments
  ```
- **List Namespaces**:
  ```sh
  kubectl get namespaces
  ```

## Pod Management

- **Create a Pod**:
  ```sh
  kubectl run <pod-name> --image=<image-name>
  ```
- **Delete a Pod**:
  ```sh
  kubectl delete pod <pod-name>
  ```
- **Describe a Pod**:
  ```sh
  kubectl describe pod <pod-name>
  ```
- **Logs of a Pod**:
  ```sh
  kubectl logs <pod-name>
  ```
- **Execute Command in Pod**:
  ```sh
  kubectl exec -it <pod-name> -- /bin/bash
  ```

## Deployment Management

- **Create a Deployment**:
  ```sh
  kubectl create deployment <deployment-name> --image=<image-name>
  ```
- **Scale a Deployment**:
  ```sh
  kubectl scale deployment <deployment-name> --replicas=<number>
  ```
- **Update a Deployment Image**:
  ```sh
  kubectl set image deployment/<deployment-name> <container-name>=<new-image>
  ```
- **Rollout History**:
  ```sh
  kubectl rollout history deployment/<deployment-name>
  ```
- **Rollout Undo**:
  ```sh
  kubectl rollout undo deployment/<deployment-name>
  ```

## Service Management

- **Expose a Pod as a Service**:
  ```sh
  kubectl expose pod <pod-name> --port=<port> --target-port=<target-port> --name=<service-name>
  ```
- **Delete a Service**:
  ```sh
  kubectl delete svc <service-name>
  ```

## Namespace Management

- **Create a Namespace**:
  ```sh
  kubectl create namespace <namespace-name>
  ```
- **Delete a Namespace**:
  ```sh
  kubectl delete namespace <namespace-name>
  ```
- **Switch Namespace**:
  ```sh
  kubectl config set-context --current --namespace=<namespace-name>
  ```

## ConfigMap & Secret Management

- **Create ConfigMap**:
  ```sh
  kubectl create configmap <configmap-name> --from-literal=<key>=<value>
  ```
- **Create Secret**:
  ```sh
  kubectl create secret generic <secret-name> --from-literal=<key>=<value>
  ```
- **Describe ConfigMap**:
  ```sh
  kubectl describe configmap <configmap-name>
  ```
- **Describe Secret**:
  ```sh
  kubectl describe secret <secret-name>
  ```

## Persistent Volume & Persistent Volume Claim

- **List Persistent Volumes**:
  ```sh
  kubectl get pv
  ```
- **List Persistent Volume Claims**:
  ```sh
  kubectl get pvc
  ```

## Ingress Management

- **Get Ingress Rules**:
  ```sh
  kubectl get ingress
  ```
- **Describe Ingress**:
  ```sh
  kubectl describe ingress <ingress-name>
  ```

## Miscellaneous

- **View All Resources in Namespace**:
  ```sh
  kubectl get all -n <namespace>
  ```
- **Apply YAML Configuration**:
  ```sh
  kubectl apply -f <file.yaml>
  ```
- **Delete Resource Using YAML**:
  ```sh
  kubectl delete -f <file.yaml>
  ```
- **Port Forward a Pod**:
  ```sh
  kubectl port-forward pod/<pod-name> <local-port>:<pod-port>
  ```

---

This cheat sheet is intended to provide a quick reference to common Kubernetes operations and commands, helping you manage your Kubernetes environments effectively.

---
