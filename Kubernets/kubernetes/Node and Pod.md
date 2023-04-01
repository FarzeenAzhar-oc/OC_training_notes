- **Node**  Worker machine
- **Pod**:
	- Smallest unit of K8s
	- Abstraction over containers
	- You only interact with K8s  layer
	- Usually 1 application per pod.
- K8s provide out of the box ip address for each of the pod
- But pod components are **effemeral**, they die easly. And new ones are created in it's place.
- This is inconveneant, and to help with this we use the concept of **service**
	[service and ingress](service%20and%20ingress.md).