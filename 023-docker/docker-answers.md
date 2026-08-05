# Q1. What is Docker?

## Answer

Docker is a containerization platform that packages an application along with all its dependencies into a portable unit called a **container**, so it runs consistently across different environments.

The main problem Docker solves is the classic **"it works on my machine"** issue. Instead of relying on the host machine's installed libraries or configurations, the application carries everything it needs except the host OS kernel.

Unlike Virtual Machines, Docker containers share the host kernel, making them much lighter and faster to start. This allows higher resource utilization and quicker deployments.

In a typical backend project, developers build a Docker image, push it to a registry, and deploy the same image across development, testing, staging, and production, ensuring consistency.

### Production Considerations

* Build immutable images and deploy the same image across all environments.
* Keep images small using multi-stage builds.
* Run containers as a non-root user for better security.

### Expected Follow-up Questions

* Why was Docker introduced?
* How is Docker different from a Virtual Machine?
* What is a Docker image?
* What is a container?
* How does Docker achieve isolation?

### Common Mistakes

* Saying Docker is a Virtual Machine.
* Assuming Docker includes its own operating system.
* Confusing images with containers.

### Important Interview Keywords

* Containerization
* Docker Engine
* Image
* Container
* OCI
* Isolation
* Portability
* Shared Kernel
* Immutable Infrastructure

---

# Q2. What is containerization?

## Answer

Containerization is the process of packaging an application along with its runtime, libraries, dependencies, and configuration into a **container**, so it can run consistently across different environments.

Instead of depending on software installed on the host machine, the container includes everything the application needs except the host operating system kernel.

Containers provide process isolation using Linux features like **namespaces** and **cgroups**, while sharing the host kernel. This makes them much lighter and faster than Virtual Machines.

For backend applications, containerization simplifies development, testing, deployment, scaling, and rollback because the same container image can be used everywhere.

### Production Considerations

* Use immutable container images.
* Externalize configuration using environment variables or secrets.
* Avoid storing persistent data inside containers.

### Expected Follow-up Questions

* How is containerization different from virtualization?
* What is a container runtime?
* What are namespaces and cgroups?
* Why are containers lightweight?

### Common Mistakes

* Assuming containers contain a full operating system.
* Treating containers as persistent environments.

### Important Interview Keywords

* Container
* Image
* Isolation
* Namespaces
* cgroups
* Portability
* Immutable Images

---

# Q3. Container vs Virtual Machine

## Answer

The biggest difference is that **containers share the host operating system kernel**, whereas **Virtual Machines run a complete guest operating system on top of a hypervisor**.

| Container                 | Virtual Machine              |
| ------------------------- | ---------------------------- |
| Shares host kernel        | Has its own guest OS         |
| Lightweight               | Heavyweight                  |
| Starts in seconds         | Takes minutes                |
| Low resource usage        | Higher CPU and memory usage  |
| Higher deployment density | Lower deployment density     |
| Best for microservices    | Best for strong OS isolation |

Because containers don't boot an operating system, they consume fewer resources and start much faster.

Virtual Machines provide stronger isolation because each VM has its own kernel, making them suitable for running different operating systems or highly isolated workloads.

### Trade-offs

**Choose Containers when:**

* Building microservices
* CI/CD pipelines
* Cloud-native applications
* Fast scaling is required

**Choose Virtual Machines when:**

* Different operating systems are needed
* Stronger isolation is required
* Running legacy applications

### Expected Follow-up Questions

* Why are containers lightweight?
* Do containers provide security comparable to VMs?
* Can Docker run Windows containers on Linux?

### Common Mistakes

* Saying containers are always more secure than VMs.
* Ignoring that containers share the host kernel.

### Important Interview Keywords

* Hypervisor
* Guest OS
* Shared Kernel
* Isolation
* Startup Time
* Resource Utilization

---

# Q4. Benefits of containers

## Answer

The major benefits of containers are **portability, consistency, fast startup, efficient resource utilization, and easy scalability**.

Since the application and its dependencies are packaged together, the same container runs consistently across development, testing, and production.

Containers share the host kernel, so they start in seconds and consume much less CPU and memory than Virtual Machines.

They also fit well with CI/CD pipelines because images are immutable, making deployments and rollbacks predictable.

For microservices, containers allow each service to be packaged, deployed, and scaled independently.

### Production Considerations

* Enables rolling deployments and quick rollbacks.
* Improves infrastructure utilization by running more workloads on the same hardware.
* Simplifies deployment across cloud providers.

### Expected Follow-up Questions

* Why are containers faster than VMs?
* How do containers help CI/CD?
* Why are containers popular for microservices?

### Common Mistakes

* Assuming containers solve persistence automatically.
* Believing containers eliminate all deployment issues.

### Important Interview Keywords

* Portability
* Consistency
* Scalability
* Immutable Images
* CI/CD
* Microservices
* Resource Efficiency

---

# Q5. Disadvantages of containers

## Answer

Containers are not a perfect solution. Their main limitations are **shared kernel dependency, weaker isolation than Virtual Machines, challenges with persistent storage, and added orchestration complexity at scale**.

Since containers share the host kernel, a kernel vulnerability can potentially affect multiple containers.

Containers are also designed to be ephemeral, so storing application data inside them is not recommended. Persistent data requires volumes or external storage.

Managing a few containers is simple, but operating hundreds of containers requires orchestration tools like Kubernetes.

Debugging distributed containerized applications can also become more challenging due to networking, logging, and monitoring requirements.

### Production Considerations

* Use volumes for persistent data.
* Apply resource limits.
* Scan images for vulnerabilities.
* Use orchestration for large-scale deployments.

### Expected Follow-up Questions

* Why shouldn't data be stored inside containers?
* How are persistent volumes managed?
* Why is Kubernetes commonly used with Docker?

### Common Mistakes

* Treating containers as long-lived servers.
* Running stateful databases without proper persistent storage.

### Important Interview Keywords

* Ephemeral
* Volumes
* Shared Kernel
* Kubernetes
* Resource Limits
* Security

---

# Q6. What is a container image?

## Answer

A **container image** is a **read-only template** that contains the application, runtime, libraries, dependencies, and configuration required to create a container.

An image itself does not execute. When Docker runs an image, it creates a writable container layer on top of the image, and that running instance is called a **container**.

Docker images are built in layers using a Dockerfile. Because layers are cached and shared, image builds become faster and storage is optimized.

The same image can be used to create multiple identical containers, ensuring consistent deployments.

### Production Considerations

* Version images using immutable tags.
* Store images in a secure registry.
* Scan images before deployment.

### Expected Follow-up Questions

* What are image layers?
* Image vs Container?
* How does Docker cache image layers?

### Common Mistakes

* Confusing images with running containers.
* Modifying containers and expecting image changes automatically.

### Important Interview Keywords

* Read-only
* Layers
* Dockerfile
* Registry
* Writable Layer
* Immutable Image

---

# Q7. What is a container runtime?

## Answer

A **container runtime** is the software responsible for creating and running containers.

It takes a container image, sets up the required isolation using Linux namespaces and cgroups, prepares the filesystem, and starts the application process inside the container.

In Docker, **containerd** manages the container lifecycle, while **runc** is the low-level runtime that actually creates and starts containers according to the OCI specification.

As a backend engineer, I typically interact with Docker rather than directly with the runtime, but understanding this architecture helps when troubleshooting container startup issues.

### Expected Follow-up Questions

* What is containerd?
* What is runc?
* What happens when `docker run` is executed?
* What is the OCI specification?

### Common Mistakes

* Assuming Docker itself is the runtime.
* Confusing Docker Engine with `containerd` or `runc`.

### Important Interview Keywords

* containerd
* runc
* OCI
* Namespaces
* cgroups
* Container Lifecycle

---

# Q8. Docker vs Hypervisor

## Answer

Docker is a **containerization platform**, while a **hypervisor** is a virtualization technology used to run multiple Virtual Machines on the same physical hardware.

Docker containers share the host operating system kernel, making them lightweight and fast.

A hypervisor allocates virtual hardware to each Virtual Machine, and every VM runs its own operating system. This provides stronger isolation but increases resource usage and startup time.

In modern cloud environments, it's common to run Docker containers inside Virtual Machines, combining the security of VMs with the efficiency of containers.

### Trade-offs

**Docker**

* Faster startup
* Lower resource usage
* Better for microservices

**Hypervisor**

* Stronger isolation
* Supports multiple operating systems
* Better for legacy or highly isolated workloads

### Expected Follow-up Questions

* Type 1 vs Type 2 Hypervisors?
* Why are containers faster?
* Can Docker replace Virtual Machines?

### Common Mistakes

* Comparing Docker directly with Virtual Machines instead of the hypervisor.
* Saying Docker provides the same isolation as a hypervisor.

### Important Interview Keywords

* Hypervisor
* Virtualization
* Containerization
* Shared Kernel
* Guest OS
* Isolation

---

# Q9. When should Docker be used?

## Answer

Docker should be used when the goal is **consistent deployments, portability, scalability, and efficient resource utilization**.

It is particularly well-suited for:

* Microservices
* Spring Boot applications
* CI/CD pipelines
* Cloud-native applications
* Development environments requiring dependency isolation
* Running multiple services consistently across different machines

For backend development, Docker allows developers, testers, and production systems to use the same image, reducing environment-specific issues.

### Production Considerations

* Use immutable image tags.
* Build optimized images.
* Manage configuration externally.
* Apply resource limits and health checks.

### Expected Follow-up Questions

* When should Docker not be used?
* Why is Docker popular for microservices?
* How does Docker improve CI/CD?

### Important Interview Keywords

* Portability
* CI/CD
* Microservices
* Immutable Images
* Scalability
* Environment Consistency

---

# Q10. When should Docker NOT be used?

## Answer

Docker should not be used when the workload requires **strong OS-level isolation, different operating systems, or direct access to specialized host hardware that containers cannot easily support**.

Examples include:

* Running applications that require different operating system kernels.
* Highly security-sensitive workloads where Virtual Machines provide stronger isolation.
* Applications with heavy GUI requirements.
* Certain low-level system software that needs unrestricted access to the host.
* Very small scripts or utilities where containerization adds unnecessary complexity.

Docker is also not ideal if the application depends on storing data inside the container. In such cases, persistent storage should be handled using volumes or external storage.

### Trade-offs

Docker is excellent for stateless, cloud-native applications, but Virtual Machines are often a better choice when complete OS isolation or different operating systems are required.

### Expected Follow-up Questions

* Can databases run inside Docker?
* Why are containers considered ephemeral?
* When should Virtual Machines be preferred?

### Common Mistakes

* Saying Docker should never be used for databases. It can be used, but production deployments require proper persistent storage and operational planning.
* Assuming every application benefits from containerization.

### Important Interview Keywords

* Shared Kernel
* Ephemeral Containers
* Persistent Storage
* Virtual Machines
* OS Isolation
* Volumes

# Q11. Explain Docker architecture.

## Answer

Docker follows a **client-server architecture**.

The main components are:

* **Docker Client** – Accepts commands like `docker build` and `docker run`.
* **Docker Daemon (`dockerd`)** – Processes those commands, builds images, manages containers, networks, and volumes.
* **Container Runtime (`containerd` + `runc`)** – Responsible for actually creating and running containers.
* **Docker Registry** – Stores Docker images, for example Docker Hub or a private registry.

When I run `docker run nginx`, the flow is:

1. Docker Client sends the request to the Docker Daemon through the Docker API.
2. Docker Daemon checks if the image exists locally.
3. If not, it pulls the image from the registry.
4. The daemon asks **containerd** to create the container.
5. **containerd** invokes **runc**, which creates the container using Linux namespaces and cgroups.
6. The application process starts inside the container.

### Production Considerations

* Developers interact with the Docker Client, while orchestration platforms like Kubernetes communicate with the Docker runtime.
* Images are typically pulled from private registries in production.

### Expected Follow-up Questions

* What is Docker Engine?
* What is containerd?
* What is runc?
* What happens internally when `docker run` is executed?

### Common Mistakes

* Saying Docker itself runs containers directly.
* Ignoring the roles of `containerd` and `runc`.

### Important Interview Keywords

* Docker Client
* Docker Daemon
* Docker Engine
* Docker API
* containerd
* runc
* Registry
* OCI

---

# Q12. Docker Client

## Answer

The **Docker Client** is the command-line interface or API through which users interact with Docker.

Whenever I execute commands like:

```bash
docker build
docker run
docker pull
docker ps
```

the Docker Client sends these requests to the **Docker Daemon** using the Docker REST API over a Unix socket or TCP.

The client itself does not build images or run containers. It only acts as the interface between the user and the Docker Daemon.

The Docker Client can also communicate with a **remote Docker host**, which is useful in CI/CD pipelines or remote build servers.

### Expected Follow-up Questions

* How does the client communicate with the daemon?
* Can the client connect to a remote Docker host?
* What is Docker API?

### Common Mistakes

* Thinking the client performs container operations.
* Confusing Docker CLI with Docker Engine.

### Important Interview Keywords

* Docker CLI
* Docker API
* Unix Socket
* Remote Docker Host
* Client-Server Architecture

---

# Q13. Docker Daemon

## Answer

The **Docker Daemon (`dockerd`)** is the background service responsible for managing Docker resources.

It listens for requests from the Docker Client and performs operations such as:

* Building images
* Running containers
* Managing networks
* Managing volumes
* Pulling and pushing images
* Monitoring container lifecycle

The daemon does not directly create containers. Instead, it delegates that responsibility to **containerd**, which further uses **runc** to create and start containers.

Without the Docker Daemon, Docker commands cannot perform any operations.

### Production Considerations

* The daemon should be secured because it has privileged access to the host.
* Exposing the Docker daemon over TCP without authentication is a major security risk.

### Expected Follow-up Questions

* What is Docker Engine?
* Difference between Docker Daemon and Docker Client?
* How does Docker Daemon use containerd?

### Common Mistakes

* Saying the daemon directly launches processes.
* Confusing the daemon with Docker Engine.

### Important Interview Keywords

* dockerd
* Docker Engine
* Docker API
* containerd
* Image Management
* Container Lifecycle

---

# Q14. Docker Engine

## Answer

**Docker Engine** is the complete Docker runtime environment used to build, run, and manage containers.

It mainly consists of:

* Docker Client
* Docker Daemon (`dockerd`)
* Docker REST API
* Container Runtime (`containerd` and `runc`)

In simple terms, the Docker Engine provides everything required to build images, manage containers, networks, and volumes.

When people install Docker on Linux or Windows, they are typically installing Docker Engine.

### Expected Follow-up Questions

* Docker Engine vs Docker Daemon?
* What components make up Docker Engine?
* What is containerd?

### Common Mistakes

* Saying Docker Engine is only the daemon.
* Ignoring the client and runtime components.

### Important Interview Keywords

* Docker Engine
* Docker Client
* Docker Daemon
* Docker API
* containerd
* OCI

---

# Q15. Docker API

## Answer

The **Docker API** is a REST API that allows clients to communicate with the Docker Daemon.

Although we usually use the Docker CLI, every CLI command is internally translated into API requests sent to the daemon.

For example:

```bash
docker run nginx
```

is converted into API calls that instruct the daemon to pull the image if needed and create the container.

The API can also be used by automation tools, CI/CD systems, and IDEs to manage Docker programmatically.

### Production Considerations

* Secure the Docker API using TLS if exposed remotely.
* Avoid exposing it publicly because it provides administrative control over the host.

### Expected Follow-up Questions

* Docker CLI vs Docker API?
* How does Kubernetes communicate with Docker?
* Unix socket vs TCP?

### Common Mistakes

* Assuming the Docker Client communicates directly with containers.
* Exposing the Docker API without authentication.

### Important Interview Keywords

* REST API
* Unix Socket
* TCP
* Docker Daemon
* Automation

---

# Q16. Container Runtime

## Answer

A **container runtime** is responsible for creating and running containers.

After Docker prepares the container configuration, it delegates execution to the runtime.

In Docker:

* **containerd** manages the container lifecycle.
* **runc** performs the low-level work of creating the container using Linux kernel features like namespaces and cgroups.

The runtime sets up the filesystem, networking, resource limits, and finally starts the application process inside the container.

### Expected Follow-up Questions

* What is containerd?
* What is runc?
* What is OCI?

### Common Mistakes

* Thinking Docker itself is the runtime.
* Confusing `containerd` with `runc`.

### Important Interview Keywords

* OCI
* containerd
* runc
* Namespaces
* cgroups
* Container Lifecycle

---

# Q17. containerd

## Answer

**containerd** is the high-level container runtime used by Docker to manage the complete lifecycle of containers.

Its responsibilities include:

* Pulling images
* Managing image storage
* Creating containers
* Starting and stopping containers
* Managing snapshots
* Monitoring container execution

When Docker receives a request, it passes container management tasks to **containerd**, which then invokes **runc** to create the actual container.

Today, Kubernetes can communicate directly with **containerd** without requiring the Docker Daemon.

### Expected Follow-up Questions

* How is containerd different from runc?
* Why did Kubernetes move to containerd?
* What is CRI?

### Common Mistakes

* Saying containerd directly creates Linux namespaces.
* Confusing container lifecycle management with low-level container creation.

### Important Interview Keywords

* containerd
* CRI
* OCI
* Image Management
* Container Lifecycle

---

# Q18. runc

## Answer

**runc** is the low-level OCI-compliant runtime responsible for actually creating and starting containers.

It performs tasks such as:

* Creating Linux namespaces
* Configuring cgroups
* Mounting the container filesystem
* Starting the container's main process

It receives the container specification from **containerd**, creates the isolated environment, starts the application, and then exits.

Because of this, **runc** is a lightweight runtime focused only on container creation.

### Expected Follow-up Questions

* runc vs containerd?
* What is OCI?
* What are namespaces?

### Common Mistakes

* Assuming runc manages the complete lifecycle of containers.
* Confusing runc with Docker Daemon.

### Important Interview Keywords

* OCI
* runc
* Namespaces
* cgroups
* Low-level Runtime

---

# Q19. Namespaces

## Answer

**Namespaces** are Linux kernel features that provide isolation between containers by giving each container its own view of system resources.

Different namespaces isolate different resources:

* **PID Namespace** – Processes
* **Network Namespace** – Network interfaces, IP addresses, routing
* **Mount Namespace** – Filesystem mounts
* **IPC Namespace** – Inter-process communication
* **UTS Namespace** – Hostname and domain name
* **User Namespace** – User and group IDs

Because of namespaces, processes inside one container cannot directly see or interfere with processes in another container.

Namespaces provide **isolation**, while **cgroups** provide **resource control**.

### Expected Follow-up Questions

* What are cgroups?
* Which namespaces does Docker use?
* How do namespaces differ from cgroups?

### Common Mistakes

* Mixing up namespaces and cgroups.
* Thinking namespaces limit CPU or memory usage.

### Important Interview Keywords

* PID Namespace
* Network Namespace
* Mount Namespace
* IPC
* UTS
* User Namespace
* Isolation

---

# Q20. Control Groups (cgroups)

## Answer

**Control Groups (cgroups)** are Linux kernel features that control and limit the resources a container can use.

While **namespaces provide isolation**, **cgroups provide resource management**.

Using cgroups, Docker can limit:

* CPU usage
* Memory usage
* Disk I/O
* Block I/O
* Number of processes

For example, we can configure a container to use a maximum of **2 CPUs and 2 GB RAM**, preventing it from consuming excessive host resources.

This improves stability by ensuring one container cannot starve others of CPU or memory.

### Production Considerations

* Always define CPU and memory limits for production containers.
* Proper limits help prevent noisy-neighbor issues and unexpected resource exhaustion.

### Expected Follow-up Questions

* Namespaces vs cgroups?
* What happens if memory limits are exceeded?
* What is OOMKilled?

### Common Mistakes

* Confusing cgroups with namespaces.
* Running production containers without resource limits.

### Important Interview Keywords

* cgroups
* CPU Limits
* Memory Limits
* Resource Isolation
* OOMKilled
* QoS

# Q21. Union File System

## Answer

A **Union File System (UnionFS)** is a filesystem that allows multiple directories or layers to be combined into a single unified view.

Docker uses this concept to build images in **layers**. Each instruction in a Dockerfile (like `RUN`, `COPY`, or `ADD`) creates a new read-only layer. When a container starts, Docker adds a thin writable layer on top of these image layers.

This layered approach provides several benefits:

* Images share common layers, reducing disk usage.
* Builds are faster because unchanged layers are reused from the cache.
* Only modified layers need to be downloaded when pulling images.

Modern Docker implementations commonly use **OverlayFS (overlay2)** as the storage driver to implement this layered filesystem.

### Expected Follow-up Questions

* What are image layers?
* What is OverlayFS?
* How does Docker layer caching work?

### Common Mistakes

* Thinking every image stores all files independently.
* Assuming containers modify image layers directly.

### Important Interview Keywords

* UnionFS
* Layered Filesystem
* Read-only Layers
* Writable Layer
* OverlayFS
* Layer Caching

---

# Q22. OverlayFS

## Answer

**OverlayFS** is a Linux filesystem that Docker commonly uses through the **overlay2 storage driver** to implement image layering.

It works by combining multiple **read-only image layers** with a **writable container layer** into a single unified filesystem.

When a file is modified inside a container, OverlayFS uses a **copy-on-write** mechanism:

* If the file hasn't been modified before, it is copied from the lower read-only layer to the writable layer.
* Subsequent changes are made only to the writable copy.

This improves storage efficiency because unchanged files are shared across multiple containers.

### Production Considerations

* `overlay2` is the recommended storage driver for most Linux distributions.
* It provides good performance and efficient disk utilization.

### Expected Follow-up Questions

* What is copy-on-write?
* Why is overlay2 recommended?
* OverlayFS vs UnionFS?

### Common Mistakes

* Assuming image layers are modified directly.
* Confusing OverlayFS with Docker volumes.

### Important Interview Keywords

* OverlayFS
* overlay2
* Copy-on-Write (CoW)
* Image Layers
* Storage Driver

---

# Q23. Image layers

## Answer

A Docker image is made up of multiple **read-only layers**, where each layer represents a filesystem change introduced by a Dockerfile instruction.

For example:

```dockerfile
FROM eclipse-temurin:21-jre
WORKDIR /app
COPY app.jar .
RUN apt-get update
```

Each instruction creates a separate layer (except some metadata instructions).

During image build:

* Docker reuses unchanged layers from the build cache.
* During image pull, only missing layers are downloaded.
* Multiple images can share common base layers.

When a container starts, Docker adds a **writable layer** on top of these read-only image layers.

### Production Considerations

* Place stable instructions before frequently changing ones to maximize cache reuse.
* Combine related `RUN` commands where appropriate to reduce unnecessary layers.

### Expected Follow-up Questions

* How does layer caching work?
* What creates a new image layer?
* Why should Dockerfiles be ordered carefully?

### Common Mistakes

* Believing containers modify image layers.
* Ignoring instruction ordering, which reduces cache efficiency.

### Important Interview Keywords

* Read-only Layers
* Writable Layer
* Layer Cache
* Copy-on-Write
* Dockerfile

---

# Q24. Container lifecycle

## Answer

A Docker container goes through several states from creation to removal.

The typical lifecycle is:

1. **Created** – Container exists but hasn't started.
2. **Running** – Application process is executing.
3. **Paused** – Processes are temporarily suspended.
4. **Stopped/Exited** – Main application process has finished or the container was stopped.
5. **Restarted** – Container starts again based on user action or restart policy.
6. **Removed** – Container is deleted.

A container continues running only while its **main process (PID 1)** is alive. If that process exits, the container stops.

### Production Considerations

* Configure appropriate restart policies.
* Use health checks to detect unhealthy containers.
* Monitor container exit codes for troubleshooting.

### Expected Follow-up Questions

* Why does a container stop immediately?
* What are restart policies?
* What is PID 1?

### Common Mistakes

* Assuming containers behave like Virtual Machines and run continuously.
* Running background processes without keeping the main process alive.

### Important Interview Keywords

* Running
* Exited
* Restart Policy
* PID 1
* Lifecycle

---

# Q25. Docker architecture in production

## Answer

In production, Docker is typically part of a larger deployment ecosystem rather than being used alone.

A common architecture is:

```
Developer
      ↓
CI/CD Pipeline
      ↓
Build Docker Image
      ↓
Push to Private Registry
      ↓
Kubernetes / Container Platform
      ↓
Production Containers
```

The Docker image is built once, scanned for vulnerabilities, stored in a registry, and deployed consistently across environments.

Container orchestration platforms like Kubernetes handle scheduling, scaling, service discovery, rolling updates, and self-healing.

### Production Considerations

* Use immutable image tags.
* Store images in private registries.
* Apply health checks and resource limits.
* Scan images before deployment.

### Expected Follow-up Questions

* Docker vs Kubernetes?
* Why use private registries?
* How are images deployed in CI/CD?

### Common Mistakes

* Building images directly on production servers.
* Using the `latest` tag in production.

### Important Interview Keywords

* CI/CD
* Registry
* Immutable Images
* Kubernetes
* Rolling Deployment
* Health Checks

---

# Q26. What is a Docker image?

## Answer

A **Docker image** is a **read-only, immutable template** used to create containers.

It contains everything needed to run an application, including:

* Application code
* Runtime
* Libraries
* Dependencies
* Configuration
* Metadata

An image itself does not execute. When Docker runs an image, it creates a container by adding a writable layer on top of the image.

The same image can be used to create multiple identical containers, ensuring consistent deployments.

### Production Considerations

* Version images using immutable tags.
* Store images in trusted registries.
* Scan images for vulnerabilities before deployment.

### Expected Follow-up Questions

* Image vs Container?
* How are images built?
* What are image layers?

### Common Mistakes

* Confusing images with running containers.
* Assuming images are writable.

### Important Interview Keywords

* Immutable
* Read-only
* Dockerfile
* Layers
* Registry

---

# Q27. Image layers

## Answer

Docker images are built as a stack of **read-only layers**, where each layer represents a filesystem change created by a Dockerfile instruction.

For example:

```dockerfile
FROM eclipse-temurin:21-jre
COPY app.jar /app/
RUN chmod +x /app/app.jar
```

Each step adds a new layer.

Docker caches these layers, so if only the application code changes, unchanged layers like the base image can be reused, making builds significantly faster.

When a container runs, Docker adds a thin writable layer on top of the image layers.

### Production Considerations

* Arrange Dockerfile instructions to maximize cache hits.
* Avoid unnecessary layers to reduce image size.

### Expected Follow-up Questions

* Layer caching?
* Copy-on-write?
* Dockerfile optimization?

### Common Mistakes

* Believing every Dockerfile instruction rebuilds from scratch.
* Modifying containers expecting image changes.

### Important Interview Keywords

* Layer Cache
* Read-only Layer
* Writable Layer
* Copy-on-Write
* Dockerfile

---

# Q28. Image caching

## Answer

Docker uses **layer caching** to avoid rebuilding unchanged parts of an image.

During a build, Docker checks each Dockerfile instruction:

* If the instruction and its inputs haven't changed, Docker reuses the cached layer.
* If a layer changes, all subsequent layers must be rebuilt.

For example:

```dockerfile
FROM eclipse-temurin:21-jre
COPY pom.xml .
RUN mvn dependency:resolve
COPY src ./src
RUN mvn package
```

If only the source code changes, the dependency layer can still be reused, making builds much faster.

### Production Considerations

* Place infrequently changing instructions first.
* Copy dependency files before application source to maximize cache efficiency.
* Use BuildKit for improved caching.

### Expected Follow-up Questions

* How can Docker builds be optimized?
* What invalidates the cache?
* What is BuildKit?

### Common Mistakes

* Copying the entire project before installing dependencies.
* Ignoring Dockerfile instruction order.

### Important Interview Keywords

* Layer Cache
* Cache Invalidation
* BuildKit
* Dockerfile Optimization

---

# Q29. Image tagging

## Answer

An **image tag** is a human-readable identifier used to reference a specific version of a Docker image.

For example:

```bash
my-service:1.2.0
my-service:v5
my-service:latest
```

A tag makes it easy to pull and deploy a particular version.

In production, it's recommended to use **versioned or immutable tags** instead of `latest`, because immutable tags make deployments reproducible and simplify rollbacks.

It's important to note that **tags can be reassigned**, so they are not guaranteed to uniquely identify an image.

### Production Considerations

* Use semantic versioning or commit SHA-based tags.
* Avoid relying on `latest` in production deployments.

### Expected Follow-up Questions

* What is an image digest?
* Why is `latest` discouraged?
* How should images be versioned?

### Common Mistakes

* Assuming `latest` always represents the newest deployed version.
* Treating tags as immutable identifiers.

### Important Interview Keywords

* Tag
* Semantic Versioning
* Immutable Tags
* latest
* Registry

---

# Q30. Image digest

## Answer

An **image digest** is a cryptographic **SHA-256 hash** that uniquely identifies the exact contents of a Docker image.

Unlike tags, a digest is **immutable**. If any layer of the image changes, the digest also changes.

For example:

```text
my-service@sha256:8f3d9d...
```

Using a digest guarantees that every deployment uses the exact same image, regardless of how tags are updated.

### Production Considerations

* Use image digests for highly reproducible deployments.
* Many Kubernetes production environments pin images using digests instead of tags.

### Expected Follow-up Questions

* Digest vs Tag?
* Why are digests immutable?
* How are image digests generated?

### Common Mistakes

* Confusing tags with digests.
* Assuming tags uniquely identify image contents.

### Important Interview Keywords

* SHA-256
* Image Digest
* Immutable
* Image Integrity
* Reproducible Deployments

# Q31. Base images

## Answer

A **base image** is the starting point of a Docker image. It is specified using the `FROM` instruction in a Dockerfile.

For example:

```dockerfile
FROM eclipse-temurin:21-jre
```

Every Docker image is built on top of a base image. The base image provides the operating system files, runtime, or language environment required by the application.

Common types of base images include:

* **Ubuntu** – General-purpose Linux distribution
* **Alpine** – Lightweight Linux distribution
* **Language-specific images** – `eclipse-temurin`, `python`, `node`, `golang`
* **Scratch** – Empty base image for minimal containers

Choosing the right base image impacts image size, security, startup time, and compatibility.

### Production Considerations

* Prefer official and well-maintained images.
* Pin specific versions instead of using floating tags.
* Regularly update base images to receive security patches.

### Expected Follow-up Questions

* Alpine vs Ubuntu?
* What is a Scratch image?
* Why use official images?

### Common Mistakes

* Using `latest` as the base image.
* Choosing a full OS image when a smaller runtime image is sufficient.

### Important Interview Keywords

* FROM
* Base Image
* Official Images
* Runtime Image
* Image Size

---

# Q32. Alpine vs Ubuntu images

## Answer

The main difference is that **Alpine focuses on minimal size**, while **Ubuntu focuses on compatibility and ease of use**.

| Alpine                  | Ubuntu                       |
| ----------------------- | ---------------------------- |
| Very small (~5–10 MB)   | Much larger (~70–100+ MB)    |
| Faster downloads        | Larger download size         |
| Smaller attack surface  | Better package compatibility |
| Uses `musl` libc        | Uses `glibc`                 |
| Limited debugging tools | Rich ecosystem and tooling   |

For simple microservices, Alpine can significantly reduce image size.

However, some Java libraries and native dependencies expect **glibc**, so Ubuntu or Debian-based images are often a safer choice for enterprise applications.

### Trade-offs

**Choose Alpine when:**

* Image size is critical.
* Dependencies are fully compatible.

**Choose Ubuntu/Debian when:**

* Maximum compatibility is required.
* Native libraries depend on `glibc`.
* Easier debugging is important.

### Expected Follow-up Questions

* Why is Alpine smaller?
* What is `musl` vs `glibc`?
* Which image do you use for Spring Boot?

### Common Mistakes

* Assuming Alpine is always the best choice.
* Ignoring compatibility issues with native libraries.

### Important Interview Keywords

* Alpine
* Ubuntu
* musl
* glibc
* Image Size
* Compatibility

---

# Q33. Scratch image

## Answer

`scratch` is the **smallest possible Docker base image**. It is an empty image with no operating system, shell, package manager, or utilities.

Example:

```dockerfile
FROM scratch
COPY app /
CMD ["/app"]
```

Since nothing is included, the application must be a **fully self-contained executable**, typically a statically compiled binary.

Using `scratch` produces extremely small images with a minimal attack surface.

### Trade-offs

**Advantages**

* Smallest possible image.
* Better security due to fewer installed components.
* Faster image download.

**Disadvantages**

* No shell for debugging.
* No package manager.
* Not suitable for applications that require OS libraries, such as most Java applications.

### Expected Follow-up Questions

* Can Spring Boot use `scratch`?
* Scratch vs Alpine?
* Why is `scratch` more secure?

### Common Mistakes

* Trying to run applications that depend on OS libraries.
* Expecting to SSH or open a shell inside a scratch container.

### Important Interview Keywords

* Scratch
* Minimal Image
* Static Binary
* Attack Surface

---

# Q34. Image pull policy

## Answer

An **image pull policy** determines **when Docker or a container orchestrator should pull an image from a registry** before starting a container.

The common behaviors are:

* **Always** – Pull the image every time before starting the container.
* **IfNotPresent** – Pull only if the image doesn't exist locally.
* **Never** – Use only the local image and never contact the registry.

Choosing the appropriate policy balances deployment consistency and startup speed.

### Production Considerations

* During development, `IfNotPresent` reduces unnecessary downloads.
* In production, immutable image tags combined with an appropriate pull policy help ensure consistent deployments.

### Expected Follow-up Questions

* Why avoid `latest`?
* What pull policy does Kubernetes use?
* What happens if the image isn't available locally?

### Common Mistakes

* Assuming Docker always downloads the latest image.
* Relying on mutable tags with cached images.

### Important Interview Keywords

* Image Pull Policy
* Registry
* IfNotPresent
* Always
* Immutable Tags

---

# Q35. Image best practices

## Answer

A production-ready Docker image should be **small, secure, reproducible, and immutable**.

Some important best practices are:

* Use official and trusted base images.
* Pin specific image versions instead of `latest`.
* Keep images as small as possible.
* Use multi-stage builds.
* Run containers as a non-root user.
* Remove unnecessary tools and packages.
* Scan images for known vulnerabilities.
* Keep configuration outside the image using environment variables or secrets.

These practices improve security, reduce deployment time, and make builds more reproducible.

### Production Considerations

* Regularly update base images for security patches.
* Sign and scan images before deployment.
* Store images in a secure private registry when appropriate.

### Expected Follow-up Questions

* How do you reduce image size?
* What are multi-stage builds?
* Why avoid `latest`?

### Common Mistakes

* Baking secrets into images.
* Installing unnecessary packages.
* Using oversized base images.

### Important Interview Keywords

* Multi-stage Build
* Non-root User
* Immutable Images
* Image Scanning
* Official Images

---

# Q36. Container lifecycle

## Answer

A Docker container moves through several states during its lifetime:

1. **Created** – The container is created but not yet running.
2. **Running** – The application's main process is executing.
3. **Paused** – Processes are temporarily suspended.
4. **Stopped/Exited** – The main process has finished or the container was stopped.
5. **Restarted** – The container starts again if manually restarted or due to a restart policy.
6. **Removed** – The container is deleted.

A container remains alive only while its **PID 1** process is running.

### Production Considerations

* Configure appropriate restart policies.
* Use health checks to detect unhealthy containers.
* Monitor exit codes for troubleshooting.

### Expected Follow-up Questions

* Why do containers stop immediately?
* What is PID 1?
* What are restart policies?

### Common Mistakes

* Treating containers like long-running Virtual Machines.
* Running applications in the background, causing PID 1 to exit.

### Important Interview Keywords

* PID 1
* Running
* Exited
* Restart Policy
* Lifecycle

---

# Q37. Container states

## Answer

A Docker container can be in different states depending on its lifecycle.

The common states are:

* **Created** – Container exists but hasn't started.
* **Running** – Application is executing.
* **Paused** – Execution is temporarily suspended.
* **Restarting** – Docker is attempting to restart the container.
* **Exited** – The main process has terminated.
* **Dead** – The container could not be cleaned up properly.
* **Removed** – Container has been deleted.

The current state can be checked using:

```bash
docker ps
docker ps -a
```

### Expected Follow-up Questions

* Difference between Exited and Dead?
* Why does a container enter the Restarting state?
* How do you inspect a stopped container?

### Common Mistakes

* Assuming an Exited container is still consuming CPU.
* Ignoring exit codes while troubleshooting.

### Important Interview Keywords

* Running
* Exited
* Restarting
* Dead
* docker ps

---

# Q38. Container isolation

## Answer

Docker containers achieve isolation using Linux kernel features, primarily **namespaces** and **cgroups**.

* **Namespaces** isolate resources such as processes, networking, filesystems, and hostnames.
* **cgroups** control resource usage like CPU and memory.

Because containers share the host kernel, they are isolated from each other but not as strongly as Virtual Machines.

This approach provides lightweight isolation while maintaining high performance.

### Production Considerations

* Run containers as non-root users.
* Apply resource limits.
* Use additional security mechanisms like seccomp or AppArmor where required.

### Expected Follow-up Questions

* Namespaces vs cgroups?
* Why are containers less isolated than VMs?
* What is rootless Docker?

### Common Mistakes

* Saying containers have their own kernel.
* Confusing isolation with resource management.

### Important Interview Keywords

* Namespaces
* cgroups
* Shared Kernel
* Isolation
* Security

---

# Q39. Container restart policies

## Answer

Restart policies define how Docker should handle a container when it exits.

The commonly used policies are:

* **no** – Never restart the container.
* **on-failure** – Restart only if the container exits with a non-zero status.
* **always** – Always restart the container whenever it stops.
* **unless-stopped** – Restart automatically unless it was explicitly stopped by the user.

These policies improve application availability without requiring manual intervention.

### Production Considerations

* Use `on-failure` for batch jobs.
* Use `unless-stopped` or `always` for long-running backend services, depending on operational requirements.

### Expected Follow-up Questions

* Difference between `always` and `unless-stopped`?
* Does a restart policy fix application crashes?
* How do restart policies work after host reboot?

### Common Mistakes

* Using restart policies instead of fixing the root cause.
* Assuming restart policies guarantee application health.

### Important Interview Keywords

* Restart Policy
* on-failure
* always
* unless-stopped
* High Availability

---

# Q40. Container logs

## Answer

Docker captures the **standard output (stdout)** and **standard error (stderr)** streams of the application's main process and stores them as container logs.

Logs can be viewed using:

```bash
docker logs <container-id>
```

or streamed in real time:

```bash
docker logs -f <container-id>
```

For backend applications, it's a best practice to write application logs to stdout/stderr instead of log files inside the container. This allows Docker and orchestration platforms to collect and aggregate logs centrally.

### Production Considerations

* Configure log rotation to prevent excessive disk usage.
* Forward logs to centralized logging systems such as ELK, Loki, or Splunk.
* Avoid storing logs inside the container filesystem.

### Expected Follow-up Questions

* Where does Docker store logs?
* How do you rotate container logs?
* Why log to stdout instead of files?

### Common Mistakes

* Writing logs only to files inside the container.
* Ignoring log rotation, leading to disk space issues.

### Important Interview Keywords

* stdout
* stderr
* `docker logs`
* Log Driver
* Centralized Logging

# Q41. Environment variables

## Answer

Environment variables are a standard way to **pass configuration to a container at runtime** without modifying the Docker image.

Typical examples include:

* Database URL
* Database username
* API endpoints
* Spring profiles
* Application ports

You can pass them while starting the container:

```bash
docker run -e SPRING_PROFILES_ACTIVE=prod \
           -e DB_HOST=postgres \
           my-app
```

Or define them in a Dockerfile:

```dockerfile
ENV APP_PORT=8080
```

However, values set with `docker run -e` override those defined using `ENV`.

This approach follows the **externalized configuration** principle, allowing the same image to be deployed across different environments.

### Production Considerations

* Store sensitive values like passwords in secrets, not environment variables when possible.
* Use environment variables for environment-specific configuration.
* Keep the Docker image immutable.

### Expected Follow-up Questions

* `ENV` vs `ARG`?
* How are environment variables passed in Docker Compose?
* How should secrets be managed?

### Common Mistakes

* Hardcoding environment-specific values into the image.
* Storing sensitive credentials in the Dockerfile.

### Important Interview Keywords

* Environment Variables
* Externalized Configuration
* `-e`
* `ENV`
* Runtime Configuration

---

# Q42. Container health checks

## Answer

A **health check** allows Docker to determine whether an application inside a container is actually healthy, instead of just checking whether the process is running.

For example:

```dockerfile
HEALTHCHECK CMD curl --fail http://localhost:8080/actuator/health || exit 1
```

Docker periodically executes the health check command.

A container can have three states:

* **starting**
* **healthy**
* **unhealthy**

This is useful because a process may still be running even though the application cannot serve requests, for example if the database connection is broken.

### Production Considerations

* For Spring Boot applications, use the Actuator health endpoint.
* Keep health checks lightweight.
* Distinguish between startup, readiness, and liveness checks when using Kubernetes.

### Expected Follow-up Questions

* How does Docker health check work?
* Health check vs Kubernetes liveness probe?
* What happens when a container becomes unhealthy?

### Common Mistakes

* Checking only whether the process exists.
* Making health checks expensive or slow.

### Important Interview Keywords

* HEALTHCHECK
* Healthy
* Unhealthy
* Spring Boot Actuator
* Liveness
* Readiness

---

# Q43. Container resource limits

## Answer

Container resource limits prevent a container from consuming excessive host resources.

Docker allows limiting resources such as:

* CPU
* Memory
* Number of processes
* Block I/O

Example:

```bash
docker run \
  --memory=2g \
  --cpus=2 \
  my-app
```

These limits are enforced using **Linux cgroups**.

Without limits, one container can consume excessive CPU or memory and negatively affect other applications running on the same host.

### Production Considerations

* Always configure CPU and memory limits for production workloads.
* Monitor actual resource usage and adjust limits based on application behavior.
* Set realistic limits to avoid unnecessary throttling or OOM kills.

### Expected Follow-up Questions

* What are cgroups?
* What happens if memory is exceeded?
* What is OOMKilled?

### Common Mistakes

* Running production containers without resource limits.
* Setting limits too low without performance testing.

### Important Interview Keywords

* cgroups
* CPU Limits
* Memory Limits
* Resource Isolation
* OOMKilled

---

# Q44. Container cleanup

## Answer

Container cleanup refers to removing **unused containers, images, networks, volumes, and build cache** to reclaim disk space.

Common commands include:

```bash
docker container prune
docker image prune
docker volume prune
docker network prune
docker system prune
```

Over time, stopped containers and unused images accumulate, especially in development and CI/CD environments, consuming significant disk space.

Regular cleanup helps keep Docker hosts healthy and avoids storage-related issues.

### Production Considerations

* Be cautious when removing volumes because they may contain persistent data.
* Automate cleanup for CI/CD runners where many temporary images and containers are created.
* Verify resources are unused before pruning.

### Expected Follow-up Questions

* What does `docker system prune` remove?
* Does pruning remove running containers?
* Can Docker volumes be recovered after deletion?

### Common Mistakes

* Accidentally deleting persistent volumes.
* Running cleanup commands blindly in production.

### Important Interview Keywords

* docker system prune
* Image Cleanup
* Container Cleanup
* Volume Prune
* Disk Management

---

# Q45. Production container management

## Answer

In production, container management focuses on **reliability, scalability, security, and observability**, rather than simply running containers.

Common practices include:

* Use an orchestrator like Kubernetes for scheduling and scaling.
* Deploy immutable, versioned images.
* Configure health checks and restart policies.
* Set CPU and memory limits.
* Centralize logging and monitoring.
* Store configuration externally using environment variables or secrets.
* Regularly scan images for vulnerabilities.

These practices make deployments more predictable and simplify scaling and recovery.

### Expected Follow-up Questions

* Why use Kubernetes?
* How are containers monitored?
* How are secrets managed?
* How are rolling deployments performed?

### Common Mistakes

* Using mutable image tags like `latest`.
* Running containers as the root user.
* Not monitoring resource usage or health.

### Important Interview Keywords

* Kubernetes
* Health Checks
* Resource Limits
* Logging
* Monitoring
* Immutable Images

---

# Q46. What is a Dockerfile?

## Answer

A **Dockerfile** is a text file containing instructions to build a Docker image.

Docker executes these instructions sequentially to create image layers.

Example:

```dockerfile
FROM eclipse-temurin:21-jre
WORKDIR /app
COPY app.jar .
ENTRYPOINT ["java", "-jar", "app.jar"]
```

Instead of manually configuring a container every time, the Dockerfile provides a repeatable and version-controlled way to build images.

### Production Considerations

* Keep Dockerfiles simple and deterministic.
* Use multi-stage builds to reduce image size.
* Order instructions to maximize layer caching.

### Expected Follow-up Questions

* What are the common Dockerfile instructions?
* What is `FROM`?
* `CMD` vs `ENTRYPOINT`?
* What are multi-stage builds?

### Common Mistakes

* Installing unnecessary packages.
* Creating large images.
* Ignoring layer caching.

### Important Interview Keywords

* Dockerfile
* Image Build
* Layers
* Multi-stage Build
* Docker Build

---

# Q47. Common Dockerfile instructions

## Answer

The most commonly used Dockerfile instructions are:

| Instruction   | Purpose                                       |
| ------------- | --------------------------------------------- |
| `FROM`        | Specifies the base image                      |
| `RUN`         | Executes commands during image build          |
| `COPY`        | Copies files from host to image               |
| `ADD`         | Copies files and supports URLs/tar extraction |
| `WORKDIR`     | Sets the working directory                    |
| `ENV`         | Defines environment variables                 |
| `ARG`         | Defines build-time variables                  |
| `EXPOSE`      | Documents the application port                |
| `USER`        | Specifies the user for running the container  |
| `CMD`         | Provides the default command                  |
| `ENTRYPOINT`  | Defines the main executable                   |
| `HEALTHCHECK` | Configures container health monitoring        |
| `LABEL`       | Adds image metadata                           |

These instructions are executed from top to bottom while building the image.

### Expected Follow-up Questions

* `COPY` vs `ADD`?
* `CMD` vs `ENTRYPOINT`?
* `ENV` vs `ARG`?
* What creates a new image layer?

### Common Mistakes

* Using `ADD` unnecessarily.
* Confusing build-time and runtime instructions.

### Important Interview Keywords

* FROM
* RUN
* COPY
* ENTRYPOINT
* CMD
* ENV
* ARG

---

# Q48. FROM

## Answer

The `FROM` instruction specifies the **base image** on which the Docker image is built.

Example:

```dockerfile
FROM eclipse-temurin:21-jre
```

It is typically the first instruction in a Dockerfile and provides the operating system files and runtime required by the application.

A Dockerfile can also contain multiple `FROM` instructions when using **multi-stage builds**.

### Production Considerations

* Use official and trusted base images.
* Pin specific versions instead of using `latest`.
* Keep the base image updated with security patches.

### Expected Follow-up Questions

* What is a base image?
* What are multi-stage builds?
* Alpine vs Ubuntu?

### Common Mistakes

* Using floating tags like `latest`.
* Choosing unnecessarily large base images.

### Important Interview Keywords

* FROM
* Base Image
* Multi-stage Build
* Official Images

---

# Q49. RUN

## Answer

The `RUN` instruction executes commands **during image build** and creates a new image layer.

For example:

```dockerfile
RUN apt-get update && apt-get install -y curl
```

The command runs only while building the image. Once the image is created, the result is stored in a layer and reused through Docker's build cache if nothing changes.

`RUN` is commonly used for:

* Installing packages
* Creating directories
* Downloading dependencies
* Performing build steps

### Production Considerations

* Combine related commands into a single `RUN` instruction where appropriate to reduce unnecessary layers.
* Clean up temporary files in the same `RUN` command to keep images small.

### Expected Follow-up Questions

* `RUN` vs `CMD`?
* Does every `RUN` create a layer?
* How does layer caching work?

### Common Mistakes

* Confusing build-time commands with runtime commands.
* Creating many unnecessary layers.

### Important Interview Keywords

* RUN
* Build Layer
* Layer Cache
* Docker Build

---

# Q50. COPY vs ADD

## Answer

For most cases, **`COPY` should be preferred** because it has a simpler and more predictable behavior.

| COPY                               | ADD                                                              |
| ---------------------------------- | ---------------------------------------------------------------- |
| Copies local files and directories | Copies local files, remote URLs, and extracts local tar archives |
| Simple and predictable             | Additional features can introduce unintended behavior            |
| Recommended for most use cases     | Use only when its extra capabilities are actually needed         |

Example:

```dockerfile
COPY app.jar /app/
```

Use `ADD` only when you specifically need automatic extraction of a local tar archive or other supported features. Otherwise, `COPY` is considered a best practice because it makes the Dockerfile easier to understand and maintain.

### Production Considerations

* Prefer `COPY` for clarity and security.
* Avoid downloading remote files using `ADD`; fetch dependencies explicitly during the build if required.

### Expected Follow-up Questions

* Why is `COPY` recommended?
* When should `ADD` be used?
* Does `COPY` create an image layer?

### Common Mistakes

* Using `ADD` for every file copy.
* Assuming `COPY` and `ADD` are completely identical.

### Important Interview Keywords

* COPY
* ADD
* Dockerfile Best Practices
* Image Layers
* Predictability
