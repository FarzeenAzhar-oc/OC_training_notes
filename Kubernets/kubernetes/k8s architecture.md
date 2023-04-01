# Worker node in k8s cluster
- Main component is worker servers or nodes
- Each has multiple pods in it
- Worker node does the actrual node
- Three processes that must be installed in every node:
	- **Container Runtime** : To run container
	- **kublets** : interacts with both container and node; starts the pod with container inside; assigning resources from node to container.
	- **kube proxy** forward requests; inteligent forwarding logic to make sure communication works with low overheads
- Interaction with a cluster,  and the foloowing function are done by **master node**:
	- Schedule pod
	- Monitor
	- re-schedule/re-start the pod
	- Join a new node



# Master Node
4 process run on every master node:
	- **Api server** 
		- Cluster gateway
		- Act as gatekeeper for authentication
	- **Scheduler**:
		- Intelligent way of deciding where to schedule the new pod
		- recives scheduling info from API
		- Decide which node a pod should go. The **kublet** starts the process within the node.
	- **Controller Manager**:
		-  Detects cluster state changes like *death of a pod*
		- Then the scheduler decides which node should restart the pod
	- **etcd**:
		- key value storer of a cluster state
		- *Cluster brain*: Cluster changes gets stored in a key value store
		- Scheduler Manager and controler manager works using etcd.
		- The **actual application data is not stored** in etcd


![worker_node_process](worker_node_process.svg)

![master_node_process](master_node_process.svg)