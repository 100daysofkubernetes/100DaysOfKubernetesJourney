# Understanding the VMware Tanzu terminology - General Kubernetes reading including Pod Security Policy

## Introduction
Writing these things in retrospect is not a good idea at all! If you ever do one of these kinds of challenges or tasks. Note down your days even in short form, even if you can't publish straight away. 

But luckily I have a lot of previous stuff to share aswell. 

One of my most visited blog posts I've written up recently is breaking down the VMware Tanzu terminology, helping explain the differences in the portfolio and its features. You can find the link below. 

Pod Security Policy is a pain in the backside. I know it's there for a reason, to increase the security posture of your cluster. But for my demo and tests I don't care. PSP is actuallly being [deprecated](https://github.com/kubernetes/kubernetes/pull/97171) in the future. I've posted some useful links below as well. 

## Research
- [Kubernetes Operators 101](https://thecloud.christmas/2020/11)
- [Understanding the VMware Tanzu Kubernetes Terminology](https://veducate.co.uk/tanzu-terminology/)
- [Kubernetes Pod Security Policy Best Practices](https://resources.whitesourcesoftware.com/blog-whitesource/kubernetes-pod-security-policy)
- [Example Role Bindings for Pod Security Policy](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-4CCDBB85-2770-4FB8-BF0E-5146B45C9543.html)
- [How to Manage Kubernetes Pod Security Policy Deprecation](https://www.paloaltonetworks.com/blog/prisma-cloud/kubernetes-psp-deprecation/)
- Unofficial Kubernetes - [Pod Security Policy](https://unofficial-kubernetes.readthedocs.io/en/latest/concepts/policy/pod-security-policy/)

## Try yourself

- Using Helm I needed to specify a [particual storage class](https://github.com/helm/charts/issues/10913) during a deployment. You can do this using:
> helm install --name my-release --set persistence.storageClass=nfs-client,mariadb.master.persistence.storageClass=nfs-client stable/wordpress
