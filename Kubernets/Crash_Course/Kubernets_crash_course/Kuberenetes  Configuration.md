- Configuration in k8s cluster goes through the master node via an api server.
- The request is either in yaml format or jason format
- Configuration is declaratice form `Is == Should`

# Parts of configuration File


- Metadata
	1. name
- Specification `specs`
- First two line are declaring what you want to create

Three parts are:
1. Metadata
2. Specification
3. Status - automatically generated by k8s
	- Desired state? = Actual state? if not k8s tries to fix it
	- Gets from etcd

Configuration are usually stored with your application code.(infrastructure as code)
or dedicated github repo for it