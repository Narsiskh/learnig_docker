# Learning Docker

## What Is Docker?
* A virtualization software
* Makes **developing** and **deploying** applications much easier
* Packages application into something called **container** that has everything the application needs to run like all the necessary dependencies, configuration , system tools and runtime.

## What Problems Docker Solves ?
### Development Process Before Containers :
* Each developer needs to **install and configure** all services **directly on their OS** on their local machine.
* **Installation process different** for each OS environment
* **Many steps**, where something can go wrong 
* If your app uses services, each developer needs to install these services.
<br>
* Development team would produce an application artifact or a package together with a sort of instructions of how to install and configure app on the server.
* Artifact and instructions handed over to Ops team
* Ops team handles installing and configuring apps and its dependencies
<br>
So, installations and configuration done directly on the server`s OS with problems like dependency version conflicts, miscommunications, human errors, back and forth communication.
### Development Process With Containers :
* Own isolated environment
* Postgres packaged with all dependencies and configs
* Start service as a Docker container using a **1 Docker command**
* Command same for all OS 
* Command same for all services
<br>
So Docker **standardizes process** of running any service on any local dev environment
* **Easy to run different versions** of same app without any conflicts.
<br>
* Docker artifact includes everything the app needs
* No configurations needed on the server (except Docker runtime)
* Less room for errors
<br>
So, the only thing now that operations team need to do in this case is to:
* Install Docker runtime on the server
* Run Docker command to fetch and run the Docker artifacts

## Virtual Machine VS Docker
### How an OS is made up?
Operating systems have two main layers :
1. OS Applications Layer 
2. OS Kernel : Kernel is the part that communicates with the hardware components like CPU, memory, storage etc.

### What parts of the OS do they virtualize?
It is actually the main difference between Docker and virtual machine.
* Docker virtualize the applications layer. This means when you run a Docker container, it actually contains the applications layer of the OS, and some other services and applications installed on top of that layer
* Virtual machine has the applications layer and its own kernel. So, it virtualizes the complete operating system, which means that when you download a virtual machine image on your host, it does not use the host kernel. It actually puts up its own.

### What affects has this difference?

|               | Docker                                |         Virtual Machine        |
|---------------|---------------------------------------|--------------------------------|
| Size of Image | MB                                    |               GB               |
| Speed         | Containers take **seconds** to start. | VMs take **minutes** to start. |
| Compability   | Only with Linux                       |             All OS             |
|               |                                       |                                |
|               |                                       |                                |


<br>

- Most containers are **Linux** based.
- Docker was originally built for **Linux OS**.

#### Docker Desktop :
- Docker desktop makes it possible to run Linux containers on Windows or MacOS.
- It uses a **Hypervisor layer** with a lightweight Linux distro.

## Install Docker

### What is included in Docker Desktop?

* Docker Engine
* Docker CLI client
* Docker Scout (additional subscription may apply)
* Docker Build
* Docker Extensions
* Docker Compose
* Docker Content Trust
* Kubernetes
* Credential Helper

### Docker Engine
* A **server** with a long-running daemon process "dockerd"
* Manage images & containers