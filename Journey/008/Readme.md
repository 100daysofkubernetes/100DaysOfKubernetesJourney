# Getting started to build EKS Custers

## Introduction
A little more on Pod Security Policy. 

I started to look at how to Build EKS clusters using vRA Code Stream. So I needed to start understanding how to build a cluster manually first. I also did some research into how others are automating the build of EKS clusters. 

Check out in a few days for my blog post on how I achieve the cluster build using vRA Code Stream. 

## Research
- [AWS EKS - Pod Security Policy](https://docs.aws.amazon.com/eks/latest/userguide/pod-security-policy.html)
- [Getting started with Amazon Elastic Kubernetes Service (Amazon EKS)](https://vzilla.co.uk/vzilla-blog/getting-started-with-amazon-elastic-kubernetes-service-amazon-eks)
- [Creating a K8s Cluster with Amazon EKS](https://docs.cambridgesemantics.com/anzo/v5.0/userdoc/cloud-eks.htm)
- [Amazon EKS cluster automation with GitLab CI/CD](https://aws.amazon.com/blogs/containers/amazon-eks-cluster-automation-with-gitlab-ci-cd/)

## Try yourself
- Install the AWS CLI and the EKSCLI
- Get an IAM access key and secret
- Create a cluster from the command line
> eksctl create cluster –name veducate-eks –region eu-west-2 –nodegroup-name standard –managed –ssh-access –ssh-public-key=EKS1 –nodes 3 –nodes-min 1 –nodes-max 4

Two hang over links from things I found during KubeCon 
- jfrog - [docker challenge](https://jfrog.com/docker-challenge/?utm_source=booth&utm_medium=event&utm_campaign=kubecon-2021&utm_term=Docker-challenge&utm_content=emea-05-2021)
- [LogDNA Lab](https://go.logdna.com/kubeconeu-logginglab?utm_medium=event&utm_source=-&utm_campaign=fy21q2%20kubecon%20eu)

