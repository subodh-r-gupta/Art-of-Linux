# kubernetes Commands Cheat Sheet
---

## Cluster Management
Usage | Command
------|--------
Display endpoint information about the master and services in the cluster	| kubectl cluster-info 
Display the Kubernetes version running on the client and server	| kubectl version
Get the configuration of the cluster	| kubectl config view 
List the API resources that are available	| kubectl api-resource
List the API versions that are available	| kubectl api-versions
List everything	| kubectl get all –all -namespaces

## Deamonset Management
Usage | Command
------|-------
List one or more daemonsets	| kubectl get daemonset
Edit and update the definition of one or more daemonset	| kubectl edit daemonset daemonset-name
Delete a daemonset	| kubectl delete daemonset daemonset-name
Create a new daemonset	| kubectl create daemonset daemonset-name
Manage the rollout of a daemonset	| kubectl rollout daemonset
Display the detailed state of daemonsets within a namespace	| kubectl describe ds daemonset-name -n namespace-name


