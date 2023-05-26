# Kubernetes Core Concepts
Below i wud be writing about the core concepts one by one.

## Kubernetes Namespaces
In Linux, we use the namespace which helps in isolating the processes from one another. Similary, in kubernetes we have ns which can provide a scope for object names.
* Kubernetes uses the namespaces to organize objects inside a cluster, we can think of these like folders holding different objects that perform strict resource separation. 
* By default, kubectl cmd line tool interacts with default namespace.
* We can also list all namespace using --all or specific with its name.

Multiple Namspaces helps in splitting complex systems with multiple components into smaller separate groups.

A namespace can be created by posting a YAML file to the Kubernetes API server or directly via kubectl command as it is just like an object in the kubernetes.
* kubectl create -f create-namespace.yml would be used to create namespace using file. 
* kubectl describe command is used to get the detail about the namespace. (e.g. kubectl describe ns default, -o output.yaml to get output in a file)
* By default any resource object you create such as Pods, deployments or any other objects, all of them are created in default namespace unless you explicitly define the namespace in YAML file or as an input argument to kubectl. 
To delete namespcve or pods we can use below commands:
* kubectl get pods -n app (get) &  kubectl delete pods -n app --all (delete)
* kubectl delete all --all -n app (for deleting all resources in a namespace)

