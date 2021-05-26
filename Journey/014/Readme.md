# Kubernetes Finalizers

## Introduction
Finalizer issues were one of the first issues I hit whilst working with Kubernetes. Actually the finalizer wasn't the issue, the issue was the task the finalizer was waiting to complete. 

A finalizer is a protection method, which waits for all tasks related to deleting an object to complete before removing the object from etcd. So if you delete a persistant volume, then there will be tasks to call off to your cloud provider or storage to delete the data. 

Below are two helpful links including a recording I found useful. I still won't fully pretend to understand finalizers completely. However I do now understand why my work around for removing the finalizer from an object is probably the wrong thing to do. 
- [How to fix in Kubernetes – Deleting a PVC stuck in status “Terminating”](https://veducate.co.uk/kubernetes-pvc-terminating/)

At some point I plan to update this blog post. 

## Research
- [KSS - Kubernetes pod status on steroid](https://github.com/chmouel/kss)
- [Install Guide: TKG and AKO 1.3 (Tanzu with Avi on vSphere)](https://www.youtube.com/watch?v=yvjQSAE6UUs)
- [Using Finalizers to Control Deletion](https://kubernetes.io/blog/2021/05/14/using-finalizers-to-control-deletion/)
- [Clean Up Your Room! What Does It Mean to Delete Something in K8s - Aaron Alpar, Kasten](https://www.youtube.com/watch?v=F7-ZxWwf4sY)

