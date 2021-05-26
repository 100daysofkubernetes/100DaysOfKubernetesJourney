# Deploying AWS EKS Clusters using VMware vRealize Automation

## Introduction
Kicked off by a customer wishing that VMware's Tanzu Mission Control (TMC) could provision and lifecycle AWS EKS clusters, rather than just attach and manage. 

So I thought about how else we could use the VMware tooling to achieve this. 

I settled on using vRealize Automation to deploy the clusters in an automated fashion, where end users could consume this automation via a cloud like catalog request.

Then my goal was to integrate this new cluster into vRA as endpoints for consumption by other automation workflows. And finally adding this to Tanzu Mission Control as an attached cluster as well. 

To build this automation pipeline, I had to build my [own container image](https://github.com/saintdle/aws-k8s-ci) with my tools installed. I looked at the [official docker image for the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-docker.html) to give me a hint of what I needed to be doing. I essentially needed more tools in the container image than just AWS CLI. 
## Research
- Recording - [3 Key Takeaways from KubeCon EU 2021](https://www.youtube.com/watch?v=xSAP9rPmitM)
  - Hosted by:
    - Bryan Liles, Principal Engineer at VMware 
    - Cheryl Hung, VP of Ecosystem at the Cloud Native Computing Foundation
- Docker Docs - [Sample app](https://docs.docker.com/get-started/02_our_app/)
- Docker Docs - [Create a base image](https://docs.docker.com/develop/develop-images/baseimages/)
- Docker Build -  [A Beginner’s Guide to Building Docker Images](https://stackify.com/docker-build-a-beginners-guide-to-building-docker-images/)
- [Getting started with AWS EKS](https://vzilla.co.uk/vzilla-blog/getting-started-with-amazon-elastic-kubernetes-service-amazon-eks)

## Try yourself
- Building your own container image, see the above links.
  - Set yourself a goal, such as create a container with some tools that you need
  - Figure out how to package it :D
  - I wrote a little more about this back in [day 1](Journey/001/Readme.md)

- Building an EKS Cluster using vRA
  - See my [blog post here](https://veducate.co.uk/vra-deploy-eks-tmc/)
