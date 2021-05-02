# Building a docker container, push to Docker Hub and link to GitHub repo

## Introduction

Learnt how to build a container from scratch using docker then push it to a repository. I also linked Docker repo back to my GitHub repo that held my container configuration files, and sync'd. So when I next update the container configuration in GitHub, docker will build a new image to host.

## Prerequisite

Tools:
- Docker
- Docker Hub Free Account
- GitHub account

## Use Case

I have a small idea on how to build a pipeline in [VMware vRA Code Stream](https://docs.vmware.com/en/vRealize-Automation/8.4/Using-and-Managing-CodeStream/GUID-3625AE99-C60C-4517-803B-18C526ADCFF1.html), which will use a container and the AWS CLI tools to build an AWS EKS cluster. This pipeline can be enabled as a [catalog item](https://docs.vmware.com/en/vRealize-Automation/8.4/Getting-Started-Service-Broker/GUID-8DDBB69B-6316-40FC-B584-C4F89643FA27.html) to be consumed by end users to build EKS clusters within a business based on the defined parameters the business is happy with.

Today I just built the container I need with a number of tools I expect to use in the CI task. 

## Research

- [Blog on gettng started building a docker image](https://stackify.com/docker-build-a-beginners-guide-to-building-docker-images/)
- [Docker documentation for building an image](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
- [My container I pushed](https://hub.docker.com/r/saintdle/aws-k8s-ci)
- [My container configuration files](https://github.com/saintdle/aws-k8s-ci)


## Try yourself

I wrote a bit of a [twitter thread here](https://twitter.com/saintdle/status/1388545101442560001?s=20)
