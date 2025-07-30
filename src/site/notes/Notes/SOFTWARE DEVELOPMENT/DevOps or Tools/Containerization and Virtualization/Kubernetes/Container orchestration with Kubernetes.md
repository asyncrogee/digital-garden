---
{"dg-publish":true,"permalink":"/notes/software-development/dev-ops-or-tools/containerization-and-virtualization/kubernetes/container-orchestration-with-kubernetes/","tags":["docker","kubernetes","containerization","virtualization","orchestration"],"created":"2025-07-23T01:48:02.299+08:00"}
---

---
> [!abstract] Introducing Kubernetes
> - Abbreviation: __K8s__
> - Developed by Google, open-sources in 2014
> - 96% of organizations use/evaluate using Kubernetes
> - Grouping containers into logical units
> - Operates as a distributed system, various components are spread across different machines (physical, virtual, cloud, or on-premise).

### Overview of Kubernetes components:
Most important Kubernetes components:
- Pods
	- smallest deployable unit
	- consisting of 1 or more containers that _share the same computing resources_.
	- ![Pasted image 20250723015412.png](/img/user/Misc/attachments/Pasted%20image%2020250723015412.png)
- Nodes
	- One or More __Pods__ are grouped into a node
	- each node serves as the host on which pods run.
	- ![Pasted image 20250723015614.png](/img/user/Misc/attachments/Pasted%20image%2020250723015614.png)
- Control Plane
	- A specific __pod__ doesn't run on the same ___node___
	- Manages nodes and pods and ensured efficient resource allocation
	- BRAIN of the _CLUSTER_
	- ![Pasted image 20250723015626.png](/img/user/Misc/attachments/Pasted%20image%2020250723015626.png)
- Cluster
	- includes all previously mentioned components
	- a group of up to multiple thousands of nodes.
	- ![Pasted image 20250723015806.png](/img/user/Misc/attachments/Pasted%20image%2020250723015806.png)