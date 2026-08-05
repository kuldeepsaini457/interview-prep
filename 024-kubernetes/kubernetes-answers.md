# Q1. What is Kubernetes?

**Answer**

Kubernetes is a container orchestration platform that automates the deployment, scaling, networking, and management of containerized applications across a cluster of machines.

Instead of managing individual containers, Kubernetes manages the desired state of the application. For example, if I specify that my application should always have 5 running instances, Kubernetes continuously monitors the cluster and automatically recreates failed Pods, schedules them on healthy nodes, and performs rolling updates when a new version is deployed.

It becomes especially useful for microservices where manually managing hundreds of containers is impractical.

**Production Considerations**

* Use Deployments for stateless applications.
* Configure health probes, resource requests/limits, and autoscaling.
* Use Ingress and Services for traffic management.

### Expected Follow-up Questions

* Why was Kubernetes introduced?
* What problems does it solve?
* How is it different from Docker?

### Important Interview Keywords

* Container Orchestration
* Desired State
* Self-Healing
* Auto Scaling
* Rolling Updates
* Scheduling

---

# Q2. What is container orchestration?

**Answer**

Container orchestration is the automated management of containers throughout their lifecycle.

It handles tasks like scheduling containers on machines, scaling applications, service discovery, load balancing, health monitoring, rolling updates, and recovering failed containers without manual intervention.

Without orchestration, these tasks become difficult as the number of containers grows. Kubernetes is the most widely used container orchestration platform.

### Expected Follow-up Questions

* Why is orchestration needed?
* Can Docker manage containers without Kubernetes?
* What orchestration features does Kubernetes provide?

### Important Interview Keywords

* Scheduling
* Scaling
* Self-Healing
* Load Balancing
* Service Discovery
* Rolling Updates

---

# Q3. Docker vs Kubernetes

**Answer**

Docker and Kubernetes solve different problems.

* **Docker** is used to build, package, and run containers.
* **Kubernetes** is used to orchestrate and manage containers at scale.

Docker creates the container image and runs containers, while Kubernetes decides where containers should run, how many replicas should exist, how they communicate, and how failures are handled.

| Docker                        | Kubernetes                             |
| ----------------------------- | -------------------------------------- |
| Creates and runs containers   | Manages containers across a cluster    |
| Runs on a single machine      | Manages multiple machines              |
| No built-in auto-healing      | Automatically recreates failed Pods    |
| Limited scaling               | Automatic scaling using HPA            |
| No native rolling deployments | Supports rolling updates and rollbacks |

They are commonly used together. Docker (or another container runtime) builds the container image, and Kubernetes orchestrates its deployment.

### Expected Follow-up Questions

* Can Kubernetes work without Docker?
* What is a container runtime?
* What is CRI?

### Common Mistake

Saying Docker and Kubernetes are competitors. They are complementary technologies.

### Important Interview Keywords

* Container Runtime
* Orchestration
* CRI
* Pods
* Deployment
* Scaling

---

# Q4. Benefits of Kubernetes

**Answer**

The biggest benefit of Kubernetes is that it automates application management in production.

Key benefits include:

* Automatic scheduling of Pods across worker nodes.
* Self-healing by restarting or recreating failed Pods.
* Horizontal scaling based on demand.
* Rolling updates and easy rollbacks with minimal downtime.
* Built-in service discovery and load balancing.
* Declarative infrastructure using YAML manifests.
* Works across on-premises and cloud environments.

These features make Kubernetes well-suited for running large-scale microservices.

### Production Considerations

* Combine Kubernetes with monitoring, logging, and autoscaling for production workloads.
* Define resource requests and limits to improve cluster utilization.

### Expected Follow-up Questions

* What is self-healing?
* How does rolling update work?
* How does Kubernetes perform service discovery?

### Important Interview Keywords

* Self-Healing
* Auto Scaling
* Rolling Updates
* Service Discovery
* Desired State
* Declarative Configuration

---

# Q5. Disadvantages of Kubernetes

**Answer**

Kubernetes is powerful, but it also introduces operational complexity.

Some common disadvantages are:

* Steep learning curve due to many concepts like Pods, Services, Deployments, Ingress, and networking.
* More operational overhead compared to running a few Docker containers.
* Debugging distributed applications can be more challenging.
* Requires proper monitoring, logging, and security configuration.
* Can be overkill for small applications or simple deployments.

For a small application running on a single server, Docker Compose is often a simpler choice.

### Trade-off

Kubernetes increases operational complexity but provides scalability, resilience, and automation for production systems.

### Expected Follow-up Questions

* When should Kubernetes not be used?
* Is Kubernetes suitable for startups?
* Docker Compose vs Kubernetes?

### Important Interview Keywords

* Operational Complexity
* Learning Curve
* Cluster Management
* Overhead
* Scalability

---

# Q6. What is a Kubernetes cluster?

**Answer**

A Kubernetes cluster is a group of machines that work together to run containerized applications.

A cluster consists of:

* **Control Plane** – manages the cluster and makes scheduling decisions.
* **Worker Nodes** – run the application Pods.

When an application is deployed, the control plane decides where Pods should run, and worker nodes execute them. This architecture enables high availability, scalability, and centralized management.

### Expected Follow-up Questions

* What is inside the control plane?
* What is a worker node?
* How are Pods scheduled?

### Important Interview Keywords

* Control Plane
* Worker Node
* Cluster
* Scheduling
* Pods

---

# Q7. Control Plane vs Worker Node

**Answer**

The **Control Plane** manages the Kubernetes cluster, while **Worker Nodes** run the application workloads.

| Control Plane          | Worker Node                        |
| ---------------------- | ---------------------------------- |
| Manages cluster state  | Runs application Pods              |
| Schedules Pods         | Executes containers                |
| Exposes Kubernetes API | Runs Kubelet and container runtime |
| Monitors desired state | Reports node status                |

The control plane decides **what should happen**, while worker nodes **execute those decisions**.

### Expected Follow-up Questions

* What are the components of the control plane?
* What does Kubelet do?
* What is Kube Proxy?

### Important Interview Keywords

* API Server
* Scheduler
* Controller Manager
* Kubelet
* Worker Node

---

# Q8. Container runtime in Kubernetes

**Answer**

A container runtime is the software responsible for running containers on a worker node.

Kubernetes communicates with the runtime through the **Container Runtime Interface (CRI)** instead of interacting with it directly.

Common container runtimes include:

* containerd
* CRI-O

The runtime is responsible for pulling images, starting containers, stopping containers, and managing their lifecycle.

### Expected Follow-up Questions

* What is CRI?
* Does Kubernetes require Docker?
* Why was Docker removed as a runtime?

### Common Mistake

Assuming Kubernetes directly uses Docker. Modern Kubernetes communicates with CRI-compatible runtimes such as containerd or CRI-O.

### Important Interview Keywords

* Container Runtime
* CRI
* containerd
* CRI-O
* Image Pull
* Container Lifecycle

---

# Q9. When should Kubernetes be used?

**Answer**

Kubernetes should be used when applications need scalability, high availability, automation, and centralized management.

Typical use cases include:

* Microservices architectures.
* Applications requiring automatic scaling.
* High-availability production systems.
* Frequent deployments with rolling updates.
* Multi-node or multi-cloud environments.

For production systems with many services, Kubernetes significantly reduces operational effort through automation.

### Production Considerations

* Ensure proper monitoring, logging, security, and resource management before adopting Kubernetes.

### Expected Follow-up Questions

* When should Kubernetes not be used?
* Can a monolith run on Kubernetes?
* Is Kubernetes necessary for every application?

### Important Interview Keywords

* Microservices
* High Availability
* Auto Scaling
* Rolling Updates
* Cluster Management

---

# Q10. When should Kubernetes NOT be used?

**Answer**

Kubernetes should not be used when its operational complexity outweighs its benefits.

Examples include:

* Small applications running on a single server.
* Development or prototype projects.
* Applications with very low traffic.
* Teams without the operational expertise to manage Kubernetes.
* Simple deployments where Docker Compose or a VM is sufficient.

In these cases, Kubernetes adds unnecessary infrastructure and maintenance overhead.

### Trade-off

Kubernetes provides excellent scalability and resilience, but it requires additional operational effort. For simple workloads, a lighter deployment approach is often more appropriate.

### Expected Follow-up Questions

* Docker Compose vs Kubernetes?
* When would you migrate to Kubernetes?
* Is Kubernetes suitable for monolithic applications?

### Common Mistake

Assuming Kubernetes is the right solution for every application. It should be adopted only when its operational benefits justify the added complexity.

### Important Interview Keywords

* Operational Overhead
* Docker Compose
* Simplicity
* Scalability
* Cost-Benefit Analysis

# Q11. Explain Kubernetes architecture.

**Answer**

Kubernetes follows a **Control Plane + Worker Node** architecture.

* The **Control Plane** manages the cluster and maintains its desired state.
* The **Worker Nodes** run the application workloads (Pods).

**Main Control Plane components:**

* **API Server** – Entry point for all Kubernetes operations.
* **etcd** – Stores the cluster's state.
* **Scheduler** – Assigns Pods to suitable worker nodes.
* **Controller Manager** – Ensures the actual state matches the desired state.

**Worker Node components:**

* **Kubelet** – Manages Pods on the node.
* **Container Runtime** – Runs containers (e.g., containerd).
* **Kube Proxy** – Handles Service networking and load balancing.

**Flow:**

1. User submits a Deployment to the API Server.
2. API Server stores the desired state in etcd.
3. Scheduler assigns Pods to worker nodes.
4. Kubelet starts the containers.
5. Controller Manager continuously ensures the desired state is maintained.

### Expected Follow-up Questions

* What does the API Server do?
* Why is etcd required?
* How does scheduling work?

### Important Interview Keywords

* Control Plane
* Worker Node
* API Server
* Scheduler
* etcd
* Kubelet
* Desired State

---

# Q12. API Server.

**Answer**

The **API Server** is the central entry point of the Kubernetes Control Plane. Every component communicates with the cluster through the API Server.

Its responsibilities include:

* Accepting REST API requests from users and components.
* Authenticating and authorizing requests.
* Validating Kubernetes objects.
* Persisting cluster state in etcd.
* Serving as the communication hub between all control plane components.

Neither the Scheduler nor Controller Manager directly access etcd—they interact through the API Server.

**Production Considerations**

* Deploy multiple API Server instances behind a load balancer for high availability.
* Secure access using RBAC and TLS.

### Expected Follow-up Questions

* How does the API Server communicate with etcd?
* Is the API Server stateless?
* What happens if the API Server goes down?

### Common Mistake

Saying components directly communicate with etcd. They communicate through the API Server.

### Important Interview Keywords

* REST API
* Authentication
* Authorization
* Admission Control
* etcd
* Stateless

---

# Q13. etcd.

**Answer**

**etcd** is Kubernetes' distributed key-value database. It stores the entire cluster state.

It stores information such as:

* Pods
* Deployments
* Services
* Secrets
* ConfigMaps
* Node information
* Cluster configuration

Whenever a resource is created or updated, the API Server persists that information in etcd.

Since etcd contains the cluster's source of truth, losing it means losing the cluster state.

**Production Considerations**

* Run an odd number of etcd nodes (typically 3 or 5) for quorum.
* Take regular backups since disaster recovery depends on them.
* Use SSD storage and low-latency networking.

### Expected Follow-up Questions

* Why does etcd require quorum?
* How is etcd backed up?
* What happens if etcd fails?

### Common Mistake

Treating etcd as a general application database. It is only for Kubernetes cluster metadata.

### Important Interview Keywords

* Distributed Key-Value Store
* Cluster State
* Source of Truth
* Quorum
* Backup

---

# Q14. Scheduler.

**Answer**

The **Scheduler** decides which worker node should run a newly created Pod.

It watches for Pods without an assigned node and selects the best node based on factors such as:

* Resource availability (CPU and memory)
* Node affinity/anti-affinity
* Taints and tolerations
* Topology spread constraints
* Resource requests

After selecting a node, the Scheduler updates the Pod assignment through the API Server. The Kubelet on that node then starts the Pod.

### Production Considerations

* Define resource requests accurately for better scheduling decisions.
* Use affinity rules only when necessary to avoid unnecessary scheduling constraints.

### Expected Follow-up Questions

* How does the Scheduler select a node?
* What are taints and tolerations?
* What is node affinity?

### Common Mistake

Assuming the Scheduler starts containers. It only assigns Pods to nodes.

### Important Interview Keywords

* Scheduling
* Resource Requests
* Node Affinity
* Taints
* Tolerations
* Topology Spread

---

# Q15. Controller Manager.

**Answer**

The **Controller Manager** runs controllers that continuously ensure the cluster's actual state matches the desired state.

Some important controllers include:

* **Deployment Controller** – Maintains Deployments.
* **ReplicaSet Controller** – Ensures the required number of replicas exist.
* **Node Controller** – Detects failed nodes.
* **Job Controller** – Manages Jobs.
* **Endpoints Controller** – Updates Service endpoints.

For example, if a Pod crashes, the ReplicaSet Controller detects that the desired replica count is no longer met and creates a replacement Pod.

### Expected Follow-up Questions

* What is a controller?
* How does ReplicaSet maintain replicas?
* What happens when a node fails?

### Important Interview Keywords

* Reconciliation Loop
* Desired State
* ReplicaSet Controller
* Deployment Controller
* Node Controller

---

# Q16. Cloud Controller Manager.

**Answer**

The **Cloud Controller Manager (CCM)** integrates Kubernetes with cloud provider services.

It separates cloud-specific logic from the core Kubernetes components.

Typical responsibilities include:

* Creating cloud load balancers.
* Managing cloud storage volumes.
* Synchronizing node information.
* Managing cloud networking resources.

For example, creating a `LoadBalancer` Service on AWS results in the CCM provisioning an AWS Load Balancer automatically.

If Kubernetes is running on-premises, the Cloud Controller Manager may not be used.

### Expected Follow-up Questions

* What services does the CCM manage?
* Why was CCM introduced?
* Is CCM required for on-premises clusters?

### Important Interview Keywords

* Cloud Integration
* LoadBalancer
* Cloud Provider
* Node Management
* Storage

---

# Q17. Kubelet.

**Answer**

The **Kubelet** is the primary agent running on every worker node.

Its responsibilities include:

* Receiving Pod specifications from the API Server.
* Instructing the container runtime to create and manage containers.
* Running health checks.
* Reporting node and Pod status back to the API Server.

The Kubelet ensures that the containers defined for the assigned Pods are actually running.

### Production Considerations

* If the Kubelet stops, existing containers may continue running, but the node is no longer managed by Kubernetes.

### Expected Follow-up Questions

* How does the Kubelet communicate with the API Server?
* Does the Kubelet schedule Pods?
* What happens if the Kubelet crashes?

### Common Mistake

Confusing the Kubelet with the Scheduler. The Scheduler assigns Pods; the Kubelet runs them.

### Important Interview Keywords

* Node Agent
* Pod Lifecycle
* Container Runtime
* Health Checks
* Node Status

---

# Q18. Kube Proxy.

**Answer**

**Kube Proxy** manages network traffic for Kubernetes Services on each worker node.

Its responsibilities include:

* Routing Service traffic to backend Pods.
* Providing load balancing across Pod replicas.
* Maintaining networking rules using iptables or IPVS.

When a request reaches a Service, Kube Proxy forwards it to one of the healthy Pods associated with that Service.

### Production Considerations

* IPVS mode generally offers better performance than iptables in large clusters.
* Kube Proxy routes traffic only to Pods marked as ready.

### Expected Follow-up Questions

* How does Service load balancing work?
* What is IPVS?
* How does Kube Proxy differ from Ingress?

### Common Mistake

Assuming Kube Proxy is a reverse proxy like NGINX. It primarily manages network forwarding rules.

### Important Interview Keywords

* Service
* Load Balancing
* iptables
* IPVS
* Endpoint

---

# Q19. Container Runtime Interface (CRI).

**Answer**

The **Container Runtime Interface (CRI)** is a standard interface that allows Kubernetes to work with different container runtimes.

Instead of depending on a specific runtime like Docker, Kubernetes communicates through CRI with runtimes such as:

* containerd
* CRI-O

This abstraction makes Kubernetes runtime-independent and allows organizations to choose the runtime that best fits their environment.

### Expected Follow-up Questions

* Why was CRI introduced?
* Does Kubernetes require Docker?
* What is containerd?

### Common Mistake

Thinking CRI is a container runtime. It is an interface between Kubernetes and the runtime.

### Important Interview Keywords

* CRI
* containerd
* CRI-O
* Runtime Abstraction
* Container Runtime

---

# Q20. Control Plane communication.

**Answer**

The API Server is the communication hub of the Kubernetes Control Plane.

The communication flow is:

1. Users or CI/CD tools send requests to the API Server.
2. The API Server validates the request and stores the desired state in etcd.
3. The Scheduler watches the API Server for unscheduled Pods and assigns them to nodes.
4. The Controller Manager watches the API Server and reconciles the cluster state.
5. Kubelets watch the API Server for Pods assigned to their nodes and start them using the container runtime.
6. Kubelets continuously report node and Pod status back to the API Server.

Most Kubernetes components communicate **through the API Server**, rather than directly with each other.

### Expected Follow-up Questions

* Why is the API Server the central communication point?
* Which components interact with etcd?
* How do controllers watch for changes?

### Common Mistake

Assuming Scheduler, Kubelet, and Controller Manager communicate directly with each other or directly modify etcd.

### Important Interview Keywords

* API Server
* Watch API
* etcd
* Desired State
* Reconciliation Loop

# Q21. Worker node responsibilities.

**Answer**

A **Worker Node** is responsible for running application workloads assigned by the Control Plane.

Its main responsibilities are:

* Running Pods and containers.
* Executing Pods assigned by the Scheduler.
* Managing containers through the container runtime (e.g., containerd).
* Reporting node and Pod health to the API Server via the Kubelet.
* Handling Service networking through Kube Proxy.

The worker node does **not** make scheduling decisions; it simply executes the workload assigned to it.

### Expected Follow-up Questions

* What components run on a worker node?
* What is the role of Kubelet?
* What happens if a worker node fails?

### Common Mistake

Saying worker nodes schedule Pods. Scheduling is handled by the Scheduler in the Control Plane.

### Important Interview Keywords

* Kubelet
* Kube Proxy
* Container Runtime
* Pods
* Worker Node

---

# Q22. Cluster lifecycle.

**Answer**

The Kubernetes cluster lifecycle starts from cluster creation and continues until workloads are deployed, managed, upgraded, and eventually decommissioned.

A typical lifecycle is:

1. Provision Control Plane and Worker Nodes.
2. Bootstrap the cluster.
3. Worker nodes join the cluster.
4. Deploy applications using Deployments, Services, and other resources.
5. Continuously monitor and scale workloads.
6. Perform rolling updates and cluster upgrades.
7. Decommission workloads or the entire cluster when no longer needed.

Throughout the lifecycle, Kubernetes continuously reconciles the actual state with the desired state.

### Production Considerations

* Upgrade worker nodes gradually to minimize disruption.
* Regularly back up etcd before cluster upgrades.

### Expected Follow-up Questions

* How is a cluster bootstrapped?
* How are cluster upgrades performed?
* What happens during node upgrades?

### Important Interview Keywords

* Bootstrap
* Desired State
* Rolling Upgrade
* Reconciliation
* Cluster Management

---

# Q23. High Availability control plane.

**Answer**

A **High Availability (HA) Control Plane** ensures the cluster remains operational even if one control plane node fails.

A typical HA setup includes:

* Multiple API Server instances behind a load balancer.
* Multiple Controller Manager instances.
* Multiple Scheduler instances.
* An HA etcd cluster (usually 3 or 5 nodes).

If one control plane node becomes unavailable, the remaining nodes continue serving requests without interrupting workload execution.

**Production Considerations**

* Use an odd number of etcd nodes to maintain quorum.
* Deploy API Servers behind a highly available load balancer.
* Regularly back up etcd.

### Expected Follow-up Questions

* Why does etcd need quorum?
* What happens if one API Server fails?
* Can workloads continue if the Control Plane is temporarily unavailable?

### Common Mistake

Assuming only the API Server needs high availability. The entire Control Plane, especially etcd, should be highly available.

### Important Interview Keywords

* High Availability
* Load Balancer
* Quorum
* etcd
* Control Plane

---

# Q24. Cluster bootstrapping.

**Answer**

Cluster bootstrapping is the process of initializing a Kubernetes cluster and allowing worker nodes to join it.

The high-level steps are:

1. Initialize the Control Plane.
2. Start core components like the API Server, Scheduler, Controller Manager, and etcd.
3. Configure networking.
4. Join worker nodes to the cluster.
5. Install essential add-ons such as DNS and a CNI plugin.
6. Deploy applications.

Tools like **kubeadm** are commonly used to bootstrap Kubernetes clusters.

### Production Considerations

* Automate cluster creation using Infrastructure as Code.
* Secure node join tokens and certificates.

### Expected Follow-up Questions

* What is kubeadm?
* How do worker nodes join the cluster?
* What is a CNI plugin?

### Important Interview Keywords

* kubeadm
* Node Join
* Certificates
* Bootstrap
* CNI

---

# Q25. Production architecture.

**Answer**

A production Kubernetes architecture should be highly available, scalable, secure, and observable.

A typical setup includes:

* Multiple Control Plane nodes.
* Multiple Worker Nodes across availability zones.
* HA etcd cluster.
* Ingress Controller for external traffic.
* CNI plugin for networking.
* Monitoring with Prometheus and Grafana.
* Centralized logging.
* RBAC, Secrets, and Network Policies for security.
* Autoscaling using HPA and Cluster Autoscaler.

The objective is to eliminate single points of failure while supporting rolling deployments and automatic recovery.

### Expected Follow-up Questions

* How do you make Kubernetes highly available?
* Which monitoring tools are commonly used?
* How is external traffic routed?

### Important Interview Keywords

* High Availability
* Ingress
* CNI
* Monitoring
* Autoscaling
* RBAC

---

# Q26. What is a Pod?

**Answer**

A **Pod** is the smallest deployable unit in Kubernetes. It represents one or more containers that are deployed and managed together.

Containers within the same Pod:

* Share the same network namespace (same IP and port space).
* Share storage volumes.
* Are scheduled on the same worker node.
* Have the same lifecycle.

Most application Pods contain a single container, while multi-container Pods are used when containers need to work very closely together.

### Production Considerations

* Keep Pods focused on a single application whenever possible.
* Use Deployments to manage Pods instead of creating Pods directly.

### Expected Follow-up Questions

* Why is a Pod needed?
* Why not deploy containers directly?
* What is a multi-container Pod?

### Common Mistake

Thinking a Pod is the same as a container. A Pod is a wrapper around one or more containers.

### Important Interview Keywords

* Smallest Deployable Unit
* Shared Network
* Shared Storage
* Pod IP
* Lifecycle

---

# Q27. Why is Pod the smallest deployable unit?

**Answer**

A Pod is the smallest deployable unit because Kubernetes manages resources at the Pod level, not at the individual container level.

Scheduling, networking, storage, health checks, and lifecycle management all happen for the entire Pod.

If multiple containers must always run together and share networking or storage, Kubernetes groups them into a single Pod instead of managing each container independently.

### Expected Follow-up Questions

* Why can't Kubernetes deploy a container directly?
* What resources are shared inside a Pod?
* When should multiple containers be placed in one Pod?

### Common Mistake

Assuming Kubernetes schedules containers individually. It always schedules Pods.

### Important Interview Keywords

* Scheduling Unit
* Shared Network Namespace
* Shared Volumes
* Pod Lifecycle

---

# Q28. Single-container vs Multi-container Pods.

**Answer**

The default approach is to use **single-container Pods**. Multi-container Pods should only be used when containers are tightly coupled.

| Single-container Pod      | Multi-container Pod                      |
| ------------------------- | ---------------------------------------- |
| One application container | Multiple tightly coupled containers      |
| Easier to manage          | Slightly more complex                    |
| Most common approach      | Used for helper containers like sidecars |
| Independent scaling       | Containers always scale together         |

Examples of multi-container Pods include:

* Logging sidecars.
* Service mesh proxies.
* Monitoring agents.

If two services need independent scaling or deployment, they should be deployed as separate Pods.

### Expected Follow-up Questions

* What is a sidecar?
* What is an init container?
* When should multi-container Pods be avoided?

### Common Mistake

Putting unrelated microservices into the same Pod.

### Important Interview Keywords

* Sidecar
* Shared Network
* Shared Volume
* Tight Coupling

---

# Q29. Init Containers.

**Answer**

An **Init Container** is a special container that runs **before** the main application containers start.

It is used for one-time initialization tasks such as:

* Waiting for a dependency to become available.
* Downloading configuration or files.
* Performing database migrations.
* Preparing shared volumes.

Each init container must complete successfully before the next init container or the main application container starts.

### Production Considerations

* Keep init containers lightweight and idempotent.
* Avoid long-running initialization logic.

### Expected Follow-up Questions

* How are init containers different from sidecars?
* What happens if an init container fails?
* Can there be multiple init containers?

### Common Mistake

Using init containers for continuously running background tasks. They exit after completing their work.

### Important Interview Keywords

* Initialization
* Sequential Execution
* Dependency Check
* Database Migration
* Shared Volume

---

# Q30. Sidecar Containers.

**Answer**

A **Sidecar Container** is a helper container that runs alongside the main application container in the same Pod.

Both containers:

* Start as part of the same Pod.
* Share networking and storage.
* Have independent processes but the same lifecycle as the Pod.

Common use cases include:

* Log collection.
* Metrics export.
* Service mesh proxies (e.g., Envoy).
* Configuration synchronization.

The sidecar extends the functionality of the main application without modifying its code.

### Production Considerations

* Use sidecars only for tightly coupled supporting functionality.
* Monitor resource usage because all containers in a Pod share the node's resources.

### Expected Follow-up Questions

* Sidecar vs Init Container?
* Why do sidecars share the Pod?
* What are common sidecar use cases?

### Common Mistake

Using sidecars for unrelated business logic that should run as a separate service.

### Important Interview Keywords

* Sidecar Pattern
* Shared Network
* Shared Volume
* Service Mesh
* Log Collection

# Q31. Pod lifecycle.

**Answer**

A Pod goes through several stages from creation until termination.

The typical lifecycle is:

1. **Pod is created** and stored in the API Server.
2. **Scheduler** assigns it to a worker node.
3. **Kubelet** pulls the container image and starts the containers.
4. **Init Containers** (if any) run first.
5. **Application containers** start.
6. **Health probes** (startup, liveness, readiness) monitor the Pod.
7. If the Pod is deleted or fails, Kubernetes terminates it gracefully and may create a replacement depending on the controller (e.g., Deployment).

Pods are **ephemeral**. They are meant to be replaced rather than repaired.

### Production Considerations

* Configure `terminationGracePeriodSeconds` for graceful shutdown.
* Use readiness probes so traffic is removed before termination.

### Expected Follow-up Questions

* What are Pod phases?
* What happens during Pod termination?
* What is graceful shutdown?

### Common Mistake

Assuming a failed Pod is repaired. Kubernetes typically replaces it with a new Pod.

### Important Interview Keywords

* Ephemeral
* Graceful Shutdown
* Init Containers
* Health Probes
* Kubelet

---

# Q32. Pod phases.

**Answer**

A Pod's **phase** represents its high-level lifecycle state.

The main Pod phases are:

* **Pending** – Pod has been accepted but containers haven't started yet. This may be due to image pulling or scheduling.
* **Running** – Pod is scheduled, and at least one container is running.
* **Succeeded** – All containers completed successfully and won't restart.
* **Failed** – One or more containers terminated with failure, and the Pod won't recover.
* **Unknown** – Kubernetes cannot determine the Pod's state, usually due to communication issues with the node.

These phases describe the Pod's overall status, not the health of individual containers.

### Expected Follow-up Questions

* What causes a Pod to remain in Pending?
* Difference between Running and Ready?
* What is CrashLoopBackOff?

### Common Mistake

Confusing **Pod Phase** with **Container State** or **Pod Conditions**.

### Important Interview Keywords

* Pending
* Running
* Succeeded
* Failed
* Unknown

---

# Q33. Pod restart policies.

**Answer**

The **restartPolicy** defines how Kubernetes restarts containers when they exit.

The available policies are:

* **Always** *(default)* – Always restart the container. Used by Deployments.
* **OnFailure** – Restart only if the container exits with a non-zero status. Common for Jobs.
* **Never** – Never restart the container.

For long-running applications, `Always` is the expected choice.

### Production Considerations

* Use `Always` for web services.
* Use `OnFailure` for batch jobs.
* Avoid `Never` unless there's a specific requirement.

### Expected Follow-up Questions

* Which restart policy does a Deployment use?
* What restart policy is used for Jobs?
* What is CrashLoopBackOff?

### Common Mistake

Thinking Deployments support all restart policies. Deployments use `Always`.

### Important Interview Keywords

* restartPolicy
* Always
* OnFailure
* Never
* Deployment
* Job

---

# Q34. Pod resource requests.

**Answer**

**Resource requests** specify the minimum CPU and memory that a Pod requires.

The Scheduler uses these values to decide where a Pod can be placed.

For example:

* Request: **500m CPU**
* Request: **512Mi Memory**

The Scheduler places the Pod only on a node that has at least these resources available.

Without requests, scheduling decisions become less predictable and can lead to resource contention.

### Production Considerations

* Always define CPU and memory requests.
* Base requests on actual application usage rather than guesses.

### Expected Follow-up Questions

* Requests vs limits?
* How does the Scheduler use requests?
* What happens if requests are omitted?

### Common Mistake

Confusing requests with resource limits.

### Important Interview Keywords

* CPU Request
* Memory Request
* Scheduler
* Resource Allocation
* Guaranteed Resources

---

# Q35. Pod resource limits.

**Answer**

**Resource limits** define the maximum CPU and memory a Pod is allowed to use.

Examples:

* Limit: **1 CPU**
* Limit: **1Gi Memory**

Behavior differs by resource:

* If CPU usage exceeds the limit, the container is **throttled**.
* If memory usage exceeds the limit, the container is typically **OOMKilled**.

Limits prevent a single Pod from consuming excessive node resources.

### Production Considerations

* Configure both requests and limits.
* Set realistic memory limits to avoid unnecessary OOMKills.

### Expected Follow-up Questions

* Requests vs limits?
* What is OOMKilled?
* What happens when CPU limits are exceeded?

### Common Mistake

Setting memory limits too low, causing frequent container restarts.

### Important Interview Keywords

* Resource Limits
* CPU Throttling
* OOMKilled
* Memory Limit
* QoS

---

# Q36. Liveness probes.

**Answer**

A **liveness probe** checks whether a container is still functioning correctly.

If the probe repeatedly fails, Kubernetes assumes the application is stuck or unhealthy and **restarts the container**.

Common probe types are:

* HTTP
* TCP
* Exec

Liveness probes are useful for recovering from deadlocks or hung processes.

### Production Considerations

* Configure appropriate initial delays and failure thresholds.
* Avoid aggressive settings that cause unnecessary restarts.

### Expected Follow-up Questions

* Liveness vs Readiness?
* Which probe types are available?
* What happens when a liveness probe fails?

### Common Mistake

Using a liveness probe to determine whether traffic should reach the Pod. That's the role of a readiness probe.

### Important Interview Keywords

* Liveness Probe
* Self-Healing
* HTTP Probe
* TCP Probe
* Exec Probe

---

# Q37. Readiness probes.

**Answer**

A **readiness probe** determines whether a Pod is ready to receive traffic.

If the readiness probe fails:

* The Pod continues running.
* Kubernetes removes it from the Service endpoints.
* No new requests are routed to it until the probe succeeds again.

This is useful during application startup, deployments, or temporary dependency failures.

### Production Considerations

* Configure readiness probes for all production services.
* Ensure the readiness endpoint verifies critical dependencies required to serve requests.

### Expected Follow-up Questions

* Readiness vs Liveness?
* What happens during rolling updates?
* Does a readiness probe restart the container?

### Common Mistake

Expecting readiness probe failures to restart the container. They only stop traffic routing.

### Important Interview Keywords

* Readiness Probe
* Service Endpoints
* Traffic Routing
* Rolling Updates
* Availability

---

# Q38. Startup probes.

**Answer**

A **startup probe** is designed for applications that take a long time to start.

While the startup probe is failing:

* Kubernetes does **not** execute liveness or readiness probes.
* Once it succeeds, normal liveness and readiness checks begin.

This prevents slow-starting applications from being restarted prematurely.

### Production Considerations

* Use startup probes for applications with long initialization times, such as Spring Boot services with heavy startup logic.
* Configure generous failure thresholds based on expected startup time.

### Expected Follow-up Questions

* Startup vs Liveness?
* When should startup probes be used?
* Can all three probes be configured together?

### Common Mistake

Using only a liveness probe for slow-starting applications, which may cause restart loops.

### Important Interview Keywords

* Startup Probe
* Slow Startup
* Initialization
* Health Checks
* Probe Lifecycle

---

# Q39. Pod eviction.

**Answer**

**Pod eviction** is the process of removing a Pod from a node when Kubernetes determines it can no longer safely remain there.

Common reasons include:

* Memory pressure.
* Disk pressure.
* Node becoming unavailable.
* Node maintenance or drain.

If the Pod is managed by a Deployment or ReplicaSet, Kubernetes schedules a replacement Pod on another suitable node.

### Production Considerations

* Configure resource requests to reduce eviction due to resource pressure.
* Distribute replicas across multiple nodes for better availability.

### Expected Follow-up Questions

* What triggers eviction?
* What happens during node drain?
* How is eviction different from deletion?

### Common Mistake

Assuming eviction always indicates an application failure. It is often triggered by node-level resource conditions.

### Important Interview Keywords

* Eviction
* Node Pressure
* Node Drain
* ReplicaSet
* Rescheduling

---

# Q40. Pod best practices.

**Answer**

For production workloads, I generally follow these best practices:

* Use **Deployments** instead of creating Pods directly.
* Keep Pods focused on a single application container unless there's a valid sidecar use case.
* Configure **CPU and memory requests/limits**.
* Define **readiness, liveness, and startup probes** where appropriate.
* Use **ConfigMaps** and **Secrets** for configuration instead of hardcoding values.
* Use **graceful shutdown** with an appropriate termination grace period.
* Avoid running containers as root and follow security best practices.
* Design applications assuming Pods are **ephemeral**.

These practices improve reliability, scalability, and maintainability in production.

### Expected Follow-up Questions

* Why should Pods be treated as ephemeral?
* Why use Deployments instead of Pods?
* How should configuration be managed?

### Common Mistake

Creating standalone Pods for production applications instead of managing them through higher-level controllers like Deployments.

### Important Interview Keywords

* Deployments
* Resource Requests
* Resource Limits
* Health Probes
* ConfigMaps
* Secrets
* Ephemeral Pods

# Q41. What is a ReplicaSet?

**Answer**

A **ReplicaSet** ensures that a specified number of identical Pod replicas are always running.

For example, if a ReplicaSet is configured with **3 replicas** and one Pod crashes, it automatically creates a new Pod to maintain the desired count.

ReplicaSets continuously compare the desired state with the actual state and reconcile any differences.

In practice, we usually don't create ReplicaSets directly—they are managed by **Deployments**.

### Expected Follow-up Questions

* Deployment vs ReplicaSet?
* How does a ReplicaSet identify Pods?
* What happens if a Pod is deleted manually?

### Common Mistake

Creating ReplicaSets directly for application deployments. In production, Deployments should manage ReplicaSets.

### Important Interview Keywords

* Desired State
* Replica
* Reconciliation Loop
* Pod Selector
* Self-Healing

---

# Q42. Deployment.

**Answer**

A **Deployment** is the recommended Kubernetes resource for managing stateless applications.

A Deployment manages ReplicaSets and provides features such as:

* Declarative application deployment.
* Scaling replicas up or down.
* Rolling updates.
* Rollbacks to previous versions.
* Self-healing through ReplicaSets.

For example, if I update the container image version in a Deployment, Kubernetes performs a rolling update by gradually replacing old Pods with new ones while keeping the application available.

### Production Considerations

* Use Deployments instead of creating Pods or ReplicaSets directly.
* Configure readiness probes to achieve zero or minimal downtime during updates.

### Expected Follow-up Questions

* How does a Deployment perform rolling updates?
* How does rollback work?
* Deployment vs StatefulSet?

### Common Mistake

Using standalone Pods for production workloads instead of Deployments.

### Important Interview Keywords

* Deployment
* ReplicaSet
* Rolling Update
* Rollback
* Desired State

---

# Q43. Deployment strategies.

**Answer**

A Deployment strategy defines **how a new application version is released**.

The most common strategies are:

1. **Rolling Update** *(default)* – Gradually replaces old Pods with new ones while keeping the application available.
2. **Recreate** – Terminates all old Pods before starting new ones, causing downtime.
3. **Blue-Green Deployment** – Runs two environments simultaneously and switches traffic after validation.
4. **Canary Deployment** – Sends a small percentage of traffic to the new version before a full rollout.

The strategy depends on the application's availability requirements and deployment risk.

### Production Considerations

* Rolling Update is suitable for most applications.
* Blue-Green and Canary typically require additional traffic management using Ingress, Service Mesh, or deployment tools.

### Expected Follow-up Questions

* Rolling Update vs Recreate?
* Blue-Green vs Canary?
* Which strategy does Kubernetes support natively?

### Important Interview Keywords

* Rolling Update
* Recreate
* Blue-Green
* Canary
* Zero Downtime

---

# Q44. Rolling Updates.

**Answer**

A **Rolling Update** gradually replaces old Pods with new Pods without bringing down the application.

The process is:

1. Create a few new Pods.
2. Wait until they become Ready.
3. Remove an equal number of old Pods.
4. Repeat until all Pods are updated.

This ensures the application remains available during deployment.

Kubernetes controls this behavior using parameters like:

* **maxUnavailable**
* **maxSurge**

### Production Considerations

* Configure readiness probes correctly.
* Tune `maxUnavailable` and `maxSurge` based on availability requirements.

### Expected Follow-up Questions

* What are maxSurge and maxUnavailable?
* How does rollback work?
* What happens if the rollout fails?

### Common Mistake

Assuming Pods receive traffic immediately after starting. Only Ready Pods receive traffic.

### Important Interview Keywords

* Rolling Update
* maxSurge
* maxUnavailable
* Readiness Probe
* Zero Downtime

---

# Q45. Recreate strategy.

**Answer**

The **Recreate** strategy deletes all existing Pods before creating new ones.

The deployment flow is:

1. Stop all old Pods.
2. Create new Pods with the updated version.

This approach causes downtime but guarantees that old and new versions never run simultaneously.

It is generally used when different application versions cannot coexist, such as applications with incompatible database schemas or exclusive resource requirements.

### Trade-off

* **Advantage:** Simple and avoids version conflicts.
* **Disadvantage:** Causes application downtime.

### Expected Follow-up Questions

* When should Recreate be used?
* Recreate vs Rolling Update?
* Does Recreate support zero downtime?

### Common Mistake

Using Recreate for user-facing applications where high availability is expected.

### Important Interview Keywords

* Recreate
* Downtime
* Version Compatibility
* Deployment Strategy

---

# Q46. Blue-Green deployments.

**Answer**

In a **Blue-Green deployment**, two identical environments are maintained:

* **Blue** – Current production version.
* **Green** – New application version.

The Green environment is deployed and tested while Blue continues serving traffic. Once validated, traffic is switched from Blue to Green.

If issues are found, traffic can quickly be switched back to Blue.

### Production Considerations

* Requires additional infrastructure because both versions run simultaneously.
* Commonly implemented using Services, Ingress, or cloud load balancers.

### Trade-off

* **Advantage:** Very fast rollback with minimal downtime.
* **Disadvantage:** Higher infrastructure cost.

### Expected Follow-up Questions

* Blue-Green vs Canary?
* How is traffic switched?
* How is rollback performed?

### Important Interview Keywords

* Blue-Green
* Traffic Switching
* Rollback
* High Availability

---

# Q47. Canary deployments.

**Answer**

A **Canary deployment** releases a new version to a small percentage of users before rolling it out to everyone.

A typical rollout is:

* 5% traffic → Monitor.
* 20% traffic → Monitor.
* 50% traffic → Monitor.
* 100% traffic if everything is healthy.

This minimizes the impact of defects because only a subset of users is exposed initially.

Traffic splitting is usually handled by an Ingress Controller, Service Mesh, or progressive delivery tools.

### Trade-off

* **Advantage:** Lower deployment risk.
* **Disadvantage:** More complex traffic management.

### Expected Follow-up Questions

* Canary vs Blue-Green?
* How is traffic split?
* What metrics should be monitored during a Canary rollout?

### Important Interview Keywords

* Canary
* Progressive Delivery
* Traffic Splitting
* Monitoring
* Rollout

---

# Q48. Deployment rollback.

**Answer**

A **rollback** restores a Deployment to a previous stable version if the current rollout fails.

Kubernetes maintains Deployment revisions through ReplicaSets. If the new version becomes unhealthy, we can roll back to an earlier revision, and Kubernetes performs another rolling update to restore the previous version.

Rollbacks are useful when application errors are detected after deployment.

### Production Considerations

* Verify readiness probes before completing a rollout.
* Monitor deployment health so failures are detected quickly.

### Expected Follow-up Questions

* How does Kubernetes maintain revision history?
* What triggers a rollback?
* How do rolling updates and rollbacks work together?

### Common Mistake

Assuming Kubernetes automatically rolls back every failed deployment. Rollback behavior depends on deployment configuration and operational practices.

### Important Interview Keywords

* Rollback
* ReplicaSet
* Revision
* Rolling Update
* Deployment History

---

# Q49. Revision history.

**Answer**

Kubernetes maintains a **revision history** of Deployments using ReplicaSets.

Each time the Deployment specification changes, Kubernetes creates a new ReplicaSet while retaining previous ones according to the configured revision history.

This enables:

* Viewing deployment history.
* Rolling back to previous versions.
* Tracking deployment changes.

The number of retained revisions can be controlled using the **revisionHistoryLimit** field.

### Production Considerations

* Keep a reasonable revision history to support rollbacks without consuming unnecessary resources.

### Expected Follow-up Questions

* What is revisionHistoryLimit?
* How does rollback use ReplicaSets?
* Where is deployment history stored?

### Important Interview Keywords

* Revision History
* ReplicaSet
* revisionHistoryLimit
* Rollback

---

# Q50. Production recommendations.

**Answer**

For production Kubernetes deployments, I generally follow these practices:

* Use **Deployments** for stateless applications.
* Configure **Rolling Updates** instead of Recreate for user-facing services.
* Set appropriate **CPU and memory requests/limits**.
* Configure **readiness, liveness, and startup probes**.
* Use **ConfigMaps** and **Secrets** for configuration management.
* Maintain multiple replicas for high availability.
* Enable monitoring, logging, and alerting.
* Use **RBAC** and follow security best practices.
* Keep container images immutable and versioned.
* Regularly test deployment rollback procedures.

These practices improve reliability, scalability, and operational safety in production.

### Expected Follow-up Questions

* How do you achieve zero-downtime deployments?
* How do you monitor deployments?
* How do you roll back a failed release?

### Common Mistake

Focusing only on application deployment while ignoring health checks, resource management, observability, and rollback planning.

### Important Interview Keywords

* Deployment
* Rolling Update
* Health Probes
* High Availability
* RBAC
* Monitoring
* Immutable Images
