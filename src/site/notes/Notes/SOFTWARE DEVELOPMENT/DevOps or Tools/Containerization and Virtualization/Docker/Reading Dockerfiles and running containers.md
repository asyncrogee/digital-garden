---
{"dg-publish":true,"permalink":"/notes/software-development/dev-ops-or-tools/containerization-and-virtualization/docker/reading-dockerfiles-and-running-containers/","tags":["docker","kubernetes","containerization","virtualization","orchestration"],"created":"2025-07-23T02:00:53.212+08:00"}
---


---

#### Format of a Dockerfile
```dockerfile
# Define the image on which to build
FROM python:3.10
```

![Pasted image 20250723020337.png](/img/user/Misc/attachments/Pasted%20image%2020250723020337.png)![Pasted image 20250723020342.png](/img/user/Misc/attachments/Pasted%20image%2020250723020342.png)
![Pasted image 20250723020347.png](/img/user/Misc/attachments/Pasted%20image%2020250723020347.png)

#### Sequential order in Dockerfiles
- Execution in sequential order
- Start of a Dockerfile:
	- Metadata
	- Comments
	- Arguments
	- `FROM` instruction

---
### Overview of Docker instructions
Important Docker instructions
- `FROM`
	- __Specifies an existing Docker image__
		- Defines the image we are building on "_Starting point_"
	- Syntax:`FROM <name_of_image>`
	- Example: `FROM python:3.10`
- `COPY`
	- Copies files or directories
		- From source (\<source>)  to destination (\<destination>)
		- Files that are needed in following Docker instructions
	- Syntax: `COPY \<source> <destination>`
	- Example: `COPY ..`
- `RUN`
	- Runs a command within a container
		- can be __any command__ that could be run in a CLI
	- Syntax: `RUN <command>`
	- Example: `RUN pip install -r requirements.txt`
- `ENTRYPOINT`
	- Defines the __container's default behavior__
		- Specifies command to run at __initiation__
		- The primary purpose of the container
	- Syntax: `ENTRYPOINT ["command", "argument"]`
	- Example: `ENTRYPOINT ["python"m "hello_world.py"]`

---
### Assembling instruction to Dockerfile
```dockerfile
# Define the image on which to build
FROM python:3.10

# Copy files/folders to the main folder of the container
COPY ..

# Install the application's dependencies
RUN pip install -r requirements.txt

# Run the script when the container starts
ENTRYPOINT ["python", "hello_world.py"]
```


### Docker build command
Builds Docker image from a `Dockerfile`
- Dockerfile needs to be located in build's context (`<context>`)
- Executed as command with Docker client via CLI

Syntax:
```
docker build <context>
```


### Docker run command
Creates and runs Docker container from Docker image
- Docker image needs to be specified as argument (`<name_of_image>`)
- Executed as command with Docker client via CLI

Syntax:
```
docker run <name_of_image>
```


