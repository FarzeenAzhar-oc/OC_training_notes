- using [minikube](https://minikube.sigs.k8s.io/docs/)
- When configuring secret, one have to encode it as a base64 text
- Deployment and services are grouped to gether since all deployment needs  services
# Deployment
- teplate is used to configure the pod
- **labels** are given to k8s components:
	- keyvalue pairs meaningful to the user
	- replicas of pods will have diferent names but same label.
- **Selector** matches the pods that have similar label, for both deployment and service
- Both service targetPort and containerPort should be same
- Env variables are set using env attributes
- Use valueFrom to refer to secret and service
- In services:
	- CluterIp is the default , which is internal
	- Nodeport is for external service
		- NodePort range is defined in k8s 30000- some value

Next see [k8s commands](k8s%20commands.md) 