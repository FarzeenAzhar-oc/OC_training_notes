- **Service** Permanant ip address given to each pod
- Lifecycle of service and pod is not connected.
- External service open to outside
- Internal only for internal
- Usually external service is not practicle, since it's just ip address
- **Ingress** Forwards or route netwerk to services
- To see another functionality of service see [Deployment and Stateful Set](Deployment%20and%20Stateful%20Set.md)

# Make external service
- In service mention type as load balancer (LoadBalancer): assigns the service an external ip adddress
- Mention nodePort in service, between 30k and 32676