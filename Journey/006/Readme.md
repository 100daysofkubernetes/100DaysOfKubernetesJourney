# KubeCon Europe Day 2 - Accessing Kubernetes platform data from within a pod

## Introduction
I use this [Pac-Man application](https://github.com/saintdle/pacman-tanzu) quite a lot in my Kubernetes testing and demos. One of components is the UI should show some basic information about where the pod is that your connected to for the UI. However this wasn't working on my deployments on Tanzu Kubernetes Grid. I managed to find the fault eventually. The pods were unable to query the Kubernetes API due to the wrong RBAC. I fixed this in my application with [this commit](https://github.com/saintdle/pacman-tanzu/commit/ece3f1d7c609b05dede0984187b84ab4f031b1a7). 
## Research

Kubernetes in Action - Book - Ch 6 - [Accessing pod metadata and other resources from applications](https://livebook.manning.com/book/kubernetes-in-action/chapter-8/1)
Kubernetes error - [cannot get resource \"nodes\" in API group \"\" at the cluster scope](https://stackoverflow.com/questions/53908848/kubernetes-pods-nodes-is-forbidden)
Kubernetes Documentation - [Accessing Clusters](https://kubernetes.io/docs/tasks/access-application-cluster/access-cluster/)

## Try yourself

Run a basic pod on your infrastructure, exec into that pod, and then try to connect to your Kubernetes cluster API to output some information. The above links should help you. 