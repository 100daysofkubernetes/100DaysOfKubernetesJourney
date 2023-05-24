# Kubernetes high level Architecture

On very top level we have Master (Control Plane) & Worker nodes

Master nodes have:
* Kube-apiserver which is responsible for orchestrating all the operations with in the cluster.
* etcd cluster which stores information about the cluster
* kube-scheduler which is responsible for scheduling pods/containers on the nodes.
* Kube Controller Manager that looks after for different functions such as node controller, replication controller etc.

On Worker Nodes we've:
* kubelet: Listens for instructions from the kube-apiserver, and manages pods.
* Kube-proxy helps in managing the communication between services inside the cluster.
* Container Runtime (Docker, containerd etc.), software that is responsible for running containers.
