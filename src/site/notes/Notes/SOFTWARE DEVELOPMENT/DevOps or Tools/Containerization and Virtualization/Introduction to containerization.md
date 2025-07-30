---
{"dg-publish":true,"permalink":"/notes/software-development/dev-ops-or-tools/containerization-and-virtualization/introduction-to-containerization/","tags":["docker","kubernetes","containerization","virtualization"],"created":"2025-07-21T16:56:54.463+08:00"}
---

---

> [!info] Environments in computing
> - Environment: System surrounding an IT application
> ![Pasted image 20250721165826.png](/img/user/Misc/attachments/Pasted%20image%2020250721165826.png)

#### OS-level virtualization
- Virtualizing the Operating System(OS)
- Not virtualized:
	- Hardware
	- OS kernel
- Virtualized:
	- Isolated user spaces

> [!tip] Introducing containers
> - OS-level virtualization = containerization
> - Isolated user spaces = containers
> - Containers
> 	- Isolated environment
> 	- Includes application and all dependencies
> ![Pasted image 20250721180918.png](/img/user/Misc/attachments/Pasted%20image%2020250721180918.png)

#### Definition of containerization
- Virtualization at OS-level
- Packaging an application and its dependencies into a container

##### Characteristics when using containers
- Reliably running multiple applications on a single host
- Each application in its own container
- Overview of application dependencies
![Pasted image 20250721181336.png](/img/user/Misc/attachments/Pasted%20image%2020250721181336.png)

> [!Abstract] Benefits of containers
> - Isolation between applications
> - Portability & reproducibility
> - Fast startup times

#####  Software tools for containerization
 - Container management: [[https://www.docker.com/ \| Docker]]
 - Container orchestration: [[https://kubernetes.io/ \| Kubernetes]]

> [!example] Use-cases of containerization
> - Microservice architecture
> - Container orchestration