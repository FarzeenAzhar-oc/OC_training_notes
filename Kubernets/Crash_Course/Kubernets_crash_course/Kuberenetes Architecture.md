- **Node** Virtual or Physical machine
- **Kublet** primary node agent, a kubernetes process that makes it possible for the cluster to talk to each other, and communicate
# The structure
- Has atleast one **master node**
- And connected to it we have a couple of **worker node**
- Each node has a **kublet** process running through it
- Each **worker node** has containers and actual work happens here
- The **master node** or control Plane has:
	- Importan K8s processes are running :
		- Api server
		- Controller Manager
		- Scheduller
		- etcd
		- Virtual Network
	- E.g : An **api server** which is a container. It acts as the entry point to K8s cluster. UI, APLI, CLI will all talk to this api
	- **Controller Manager** runs in master to keep track of whats happenening in the cluster.
	- **Scheduler** ensures pod replacement, scheduler decides on which Node new Pod should be scheduled.
	- **etcd** Kuberbetes backing store
	- **Virtual Network** Creates one unified machine
-  Multiple Master nodes are used as backup

**Next** [Kuberenetes Components](Kuberenetes%20Components.md)