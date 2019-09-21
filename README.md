# Kubernetes Practice

Kubernetes practice including yaml files, etc.

`kubectl` cheatsheet: https://kubernetes.io/docs/reference/kubectl/cheatsheet/

## Minikube
[Minikube](https://minikube.sigs.k8s.io/) is a a way of running a local kubernetes cluster with a single master and worker. It uses virtualization software (VirtualBox, hyperkit, etc.) to start a VM containing the cluster.
#### Installation
`brew cask install minikube`
`brew install hyperkit`
#### Usage
To set hyperkit as the default driver:
`minikube config set vm-driver hyperkit`
Then to start:
`minikube start`
To stop (but still have the cluster available):
`minikube stop`
To completely remove the cluster:
`minikube delete`

Minikube also offers a web based visual dashboard:
`minikube dashboard`

## kubectl
CLI tool for interacting with kubernetes clusters.
#### Installation
`brew install kubectl`
#### Usage
Show info about the cluster:
`kubectl cluster-info`
Display the nodes in a cluster:
`kubectl get nodes`
Post a manifest to the api server:
`kubectl apply -f manifest.yml`

## Other useful commands:

`gcloud container clusters get-credentials --zone [ZONE] [CLUSTER_NAME]`

fetch credentials for cluster running on GKE
