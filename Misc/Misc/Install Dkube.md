#cmmand
- Makes it easy to manage kubernetics clusters
- **Final Aim** -> Create cluster, install dkube, Run tests
## Prereuisites
1. To ssh to a cluster in OC `ssh dkube@192.168.200.<node>`
1. Download Docker

## High level overview
*Rancher cluster manager is the server that lets you manage different clusters, not an official name trademark pending ip is `192.168.200.117` and follow [QA cheathseet doc](https://docs.google.com/document/d/1mPn2z5mIzIEqJ0cf5W_51J1nNO8gg23cyhurF2bgJMI/edit#heading=h.50gjhhgldmpu)*


1. Rancher Cluster Manager add the nodes, one as master  rest as slave
2. Add kube-api in Rancher Cluster Manager's yml file
3. Copy paste the docker commands in Rancher Cluster Manager to nodes
4. Create .kube directory, add .kube/config file with sudo obly in master
	1. Copy paste cube config file from Rancher Cluster Manager to .kube/config
5.  Install kubernetics using [this](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/) to both master and slave.
	**From now everything is for MASTER ONLY**
6. Install Helm to get dkube
7. Follow [dkube installation using helm doc](https://docs.google.com/document/d/11pBmb4d-FUkzLqPxjRl9hF9Y0SBY0HImPtl8v_jwf9M/edit)


# References
[QA cheathseet doc](https://docs.google.com/document/d/1mPn2z5mIzIEqJ0cf5W_51J1nNO8gg23cyhurF2bgJMI/edit#heading=h.50gjhhgldmpu)
