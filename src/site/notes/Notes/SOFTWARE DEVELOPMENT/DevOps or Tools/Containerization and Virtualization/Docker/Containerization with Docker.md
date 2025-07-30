---
{"dg-publish":true,"permalink":"/notes/software-development/dev-ops-or-tools/containerization-and-virtualization/docker/containerization-with-docker/","tags":["docker","kubernetes","containerization","virtualization","orchestration"],"created":"2025-07-21T18:46:44.594+08:00"}
---


---


> [!example] Overview of Docker components:
> - Most important Docker components:
> 	- Docker Desktop
> 	- Docker Engine
> 		- Docker Client
> 		- Docker Daemon
> 	- Docker Objects
> 		- Docker Images
> 		- Docker Containers
> 	- Docker Registries

![Pasted image 20250723012659.png](/img/user/Misc/attachments/Pasted%20image%2020250723012659.png)
- Docker Engine acts as a client-server application
- Client requests are received by the __Docker Daemon__
	- Docker Daemon: core service responsible for building, running, and managing _Docker Objects_.
- Two main _Docker Objects_: Images & Containers

Sharing containers via registries:
![Pasted image 20250723012742.png](/img/user/Misc/attachments/Pasted%20image%2020250723012742.png)- Docker Hub is a popular docker registry.