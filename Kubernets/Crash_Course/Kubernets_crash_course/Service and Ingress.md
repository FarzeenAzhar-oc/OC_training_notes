# Service 
- When a pod dies, it gets new ip
- So we have service which helps to solve this problem
- A service is a permanent (static) IP address, that can be attached to each pod
- Life cycle of pod and service not connected. i.e. If pod dies , service remains
- **External services** can be opened from outside the network and **Internal service** can be run in internal browsers.

# Ingress
- Ingress forwards requests to a service, example a url used by a user

![Service](Service.svg)