# 🐳 Docker

![alt text](images/docker-architecture.jpg)

## Install Docker Desktop
https://www.docker.com/products/docker-desktop/

## Once installed:
### In a terminal window, run docker --version, and paste the output in the chat. From v20 onwards is fine.

```bash
docker --version
# Docker version 27.2.0, build 3ab4256
```

### Run Docker Desktop application and check the bottom left for the status.
### Note:
- Status should be green and the newer versions also state "Engine running".
- If the status is not green, you will need to troubleshoot to get it running.
:warning: Warning! When starting Docker Desktop in Windows, you will likely need to choose to "Run as Administrator". If you don't, you will get an error.

![alt text](<images/Screenshot 2024-11-04 162654.jpg>)

### Create an account on Docker Hub. Doesn't matter the OS you are using on your local machine.
### In Docker Desktop, login using the account you created on Docker Hub.


# Task: Research microservices, containers and Docker

### Research and document...

# Differences between virtualisation and containerisation

1. 🖥️ **Virtualization**:

    - Virtualization is the process of creating multiple simulated environments (virtual machines) on a single physical machine using a hypervisor.
    - Each virtual machine (VM) has its own operating system (guest OS) and resources, independent of the host OS.

2. 📦 **Containerization**:

    - Containerization involves creating isolated environments (containers) on a shared operating system. Containers share the host OS kernel and are more lightweight than VMs.
    - Containers package applications with their dependencies but do not include a full OS, making them faster to deploy and consume fewer resources.

3. ⚖️ **Key Differences**:

    - **OS Requirements**: VMs require a full OS per VM, while containers share the host OS.
    - **Resource Efficiency**: Containers are more lightweight and resource-efficient than VMs.
    - **Isolation**: VMs provide stronger isolation as each VM runs its OS, whereas containers share the host OS, potentially reducing isolation.

### What is usually included in a container vs virtual machine?

1. **Container**:

    - Application code and binaries
    - Libraries and dependencies specific to the application
    - Shared OS kernel with the host (no separate OS for each container)

2. **Virtual Machine (VM)**:

    - Application code and binaries
    - Full guest OS (including its own kernel, libraries, and dependencies)
    - Hardware resources are virtualized (CPU, memory, storage, and network interface)

### Benefits of each, especially a virtual machine over the traditional architecture

1. **Virtualization Benefits**:

    - 🛡️ **Strong Isolation**/**security**: Each VM runs its OS, offering robust security and isolation.
    - 📋 **Compatibility**: VMs can run different OSes on the same hardware, making it ideal for running legacy or different applications.
    - ⚙️ **Scalability and Flexibility**: Virtualized environments can be scaled horizontally and vertically, adapting to workload requirements.

2. **Containerization Benefits**:

    - 💽 **Resource Efficiency**: Containers are lightweight and start quickly, allowing high-density application deployment.
    - 🌍 **Portability**: Containers include all dependencies, making applications portable across environments (e.g., from development to production).
    - ⚡ **Fast Scaling and Deployment**: Containers can be spun up or down quickly, making them ideal for microservices and agile environments.

# 🏗️ Microservices
### What are they?
- Microservices is an architectural style where an application is built as a collection of loosely coupled, independent services, each responsible for a specific business functionality.

### How are they made possible?
- 📡 **APIs**: Microservices architecture relies on APIs for communication between services.
- 📦 **Containers**:  such as those created with Docker, enable isolated, lightweight, and easily scalable environments for each microservice.
- 🚀 **DevOps and CI/CD** : DevOps practices, continuous integration/continuous deployment (CI/CD), and orchestration tools like Kubernetes support the management and deployment of microservices.
  
### Benefits
- 📈 **Scalability**: Services can be scaled independently, allowing resources to be allocated based on each service’s demand.
- 🔄 **Flexibility in Development**: Teams can work on different services simultaneously and in different languages.
- 🛡️ **Resilience**: Failure in one microservice doesn’t bring down the whole application, enhancing fault tolerance.
- 🚢 **Ease of Deployment**: Microservices allow for continuous deployment as services can be updated independently.


# 🐳 Docker

### ❓ What is it
- Docker is an open-source platform for developing, shipping, and running applications in containers. Docker allows applications to run consistently across different environments.

### 🔄 Alternatives
- 🐧 **Podman**: Docker-compatible container engine that can run without a daemon, ideal for rootless containers.
- ☸️ **Kubernetes** (with CRI-O or Containerd): While primarily an orchestration tool, Kubernetes supports container engines like CRI-O and Containerd.
- 📦 **LXC/LXD**: Linux Containers offer system containers with full OS, closer to lightweight VMs.
- 🛡️**rkt**(Rocket): A container runtime focused on security, though development is now discontinued.

### ⚙️ How it works (Docker architecture/API)
- 🖥️ **Docker Engine**: Core component that runs on the host OS to create and manage containers.
- 🔧 **Docker Daemon**: The background service that manages Docker objects (images, containers, networks).
- 💻 **Docker CLI**: Command-line interface to interact with Docker Daemon for executing commands (e.g., docker run).
- 🖼️ **Docker Images**: A blueprint for containers, containing application code and dependencies.
- 📂 **Docker Containers**: Instances created from Docker images.
- 🌐**Docker Registry**: Centralized repository (like Docker Hub) to store and share Docker images.
- 📡**Docker API**: Provides an interface for interacting with the Docker daemon programmatically, enabling automation.

### 💡 Success story using Docker
- **ADP (Automatic Data Processing)**: ADP migrated to a microservices architecture powered by Docker containers to modernize its application deployment. Docker allowed ADP to deploy new features faster, isolate applications, and improve infrastructure efficiency. This move to Docker helped ADP achieve significant savings in time and resources while improving scalability and resilience in production environments.