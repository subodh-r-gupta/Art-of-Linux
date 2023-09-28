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

## Listing resources
Usage | Command
------|-------
Generate a plain-text list of all namespaces | kubectl get namespaces
Generate a plain-text list of all pods	| kubectl get pods
Generate a detailed plain-text list of all pods	| kubectl get pods -o wide
Generate a list of all pods running on a particular node server	| kubectl get pods–field-selector=spec. nodeName=[server-name]
List a specific replication controller in plain text	| kubectl get replicationcontroller [replication-controller-name]
Generate a plain-text list of all replication controllers and services	| kubectl get replicationcontroller, services

 ## Logs
 Usage | Command
------|-------
Print the logs for a pod	| kubectl logs <pod_name>
Print the logs for a pod for last 1 hour	| kubectl logs –since=1h <pod_name> 
Get the most recent 20 lines of logs	| kubectl logs –tail=20 <pod_name>
Get logs from a service and optionally select which container	| kubectl logs -f <service_name> [-c <$container>] 
Print the logs for a pod and follow new logs	| kubectl logs -f <pod_name>
Print the logs for a container in a pod	| kubectl logs -c <container_name> <pod_name>
Output the logs for a pod into a file named ‘pod.log’	| kubectl logs <pod_name> pod.log 
View the logs for a previously failed pod	| kubectl logs –previous <pod_name> 

