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

## Deamonsets
Usage | Command
------|-------
List one or more daemonsets	| kubectl get daemonset
Edit and update the definition of one or more daemonset	| kubectl edit daemonset daemonset-name
Delete a daemonset	| kubectl delete daemonset daemonset-name
Create a new daemonset	| kubectl create daemonset daemonset-name
Manage the rollout of a daemonset	| kubectl rollout daemonset
Display the detailed state of daemonsets within a namespace	| kubectl describe ds daemonset-name -n namespace-name

## Deplyoments
Usage | Command
------|-------
List one or more deployments	| kubectl get deployment
Display the detailed state of one or more deployments	| kubectl describe deployment <deployment_name>
Edit and update the definition of one or more deployment on the server	| kubectl edit deployment <deployment_name>
Create one a new deployment	| kubectl create deployment <deployment_name>
Delete deployments	| kubectl delete deployment <deployment_name>
See the rollout status of a deployment	| kubectl rollout status deployment <deployment_name>

## Events
Usage | Command
------|-------
List recent events for all resources in the system	| kubectl get events
List Warnings only	| kubectl get events –field-selector type=Warning 
List events but exclude Pod events	| kubectl get events –field-selector involvedObject.kind!=Pod 
Pull events for a single node with a specific name	| kubectl get events –field-selector involvedObject.kind=Node, involvedObject.name=<node_name>
 Filter out normal events from a list of events	| kubectl get events –field-selector type!=Normal

