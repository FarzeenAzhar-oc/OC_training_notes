#command 
- Command line tool for k8s cluster
- **Api server** enables interaction 

For practice use [minicube](https://minikube.sigs.k8s.io/docs/start/)
To install kubectl use [this](https://kubernetes.io/docs/tasks/tools/)
# Commands
- **To get node status** `kubectl get nodes`
- **To see info on an k8s objects** `kubectl get <object>`
- **Create k8s components** see  `kubectl create -h
	- In practice for k8s you don't create pod directly, you create deployment/statefulset/deamon etc
	- **Deployment**  automatically creates a **replicaset** which creates the **pod**
		`kubctl get deployment`	
		`kubectl ger replicaset`
	- **Deployment** manges -> **Replicaset** manages -> all replicas of **pod**, which is an abstraction -> **container**
	- Everything below **deployment** is managed by k8s
- `kubectl apply -f <config-file.yaml>` configure a deployment or a component using a file
	- k8s know when to create or update based on existance of deployment

# Commands Summary
## CRUD commands
- **Creat component** `kubectl create <command>`
- **Edit component** `kubectl edit <command>`
- **Delete component** `kubectl delete <command>`

## Status of different k8s components
`kubectl get <nodes|pods|services|replicaset|deployment>`

## Debugging pods
**Log to console ** `kubectl logs <pod name>`
** Get interactive terminal** `kubectl exec -it <pod name> --bin/bash`

## Use configuration file for CRUD
**Apply a config file** `kubectl apply -f <file name>`
**Delete a config file** `kubectl delete -f <filename>`