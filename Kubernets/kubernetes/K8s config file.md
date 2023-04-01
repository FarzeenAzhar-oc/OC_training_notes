
Top 2 parts are apiVersion and kind, declaring what we are trying to create
# 3 parts
1. **metadata** includes name
2.  **spec** specification, about what we are creating
3. **status** automatically created by k8s
	- K8s automatically compares what the desired state is and what the actual state is
	- If desired and actual doesn't match it will try to fix it
	- It gets status data **etcd** 

# Yaml format
- human friendly
- Strict intentaion
- These are stored usually with application code
---

# Blueprint for pods
- the pod data is fiven under **template** in deployment
- **pod** will have its own metadata and spec

# Connecting components
- connection established using labels and selectors
- Any-key-value pair for components, that label sticks to component
- This label is matched by selector
![Pasted image 20221212130410](Pasted%20image%2020221212130410.png)

### ports
 - Service has a port were service itself is accecable
 - Sevice need to know which port to send request and which port its listening, which is targetPort, which should match the container port.

![Pasted image 20221212130748](Pasted%20image%2020221212130748.png)

# Status
To see status  use
`kubectl get deploy -oyaml -n <namespace>`
