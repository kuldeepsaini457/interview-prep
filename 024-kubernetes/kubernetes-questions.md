# Kubernetes Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Google, Uber, LinkedIn, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** Kubernetes, Docker, Java, Spring Boot, Microservices, Cloud, DevOps
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Kubernetes has become the industry standard for container orchestration. SDE-2 interviews frequently cover Kubernetes architecture, Pods, Deployments, Services, Ingress, ConfigMaps, Secrets, StatefulSets, Autoscaling, Scheduling, Networking, Storage, Security, and production troubleshooting.

---

# Table of Contents

1. Kubernetes Fundamentals
2. Kubernetes Architecture
3. Pods
4. ReplicaSets & Deployments
5. Services
6. Ingress
7. ConfigMaps & Secrets
8. Volumes & Persistent Storage
9. Scheduling
10. Stateful Applications
11. Autoscaling
12. Networking
13. Security
14. Monitoring & Troubleshooting
15. Kubernetes Best Practices
16. Advanced Kubernetes Concepts
17. Scenario-Based Questions
18. Production Experience
19. Why Questions
20. Trade-offs
21. Common Follow-up Questions

---

# 1. Kubernetes Fundamentals

## Basic

### Q1.
What is Kubernetes?

**Follow-ups**
- Why was Kubernetes introduced?
- What problems does it solve?

---

### Q2.
What is container orchestration?

---

### Q3.
Docker vs Kubernetes.

---

### Q4.
Benefits of Kubernetes.

---

### Q5.
Disadvantages of Kubernetes.

---

### Q6.
What is a Kubernetes cluster?

---

### Q7.
Control Plane vs Worker Node.

---

### Q8.
Container runtime in Kubernetes.

---

### Q9.
When should Kubernetes be used?

---

### Q10.
When should Kubernetes NOT be used?

---

# 2. Kubernetes Architecture

## Intermediate

### Q11.
Explain Kubernetes architecture.

---

### Q12.
API Server.

---

### Q13.
etcd.

---

### Q14.
Scheduler.

---

### Q15.
Controller Manager.

---

### Q16.
Cloud Controller Manager.

---

### Q17.
Kubelet.

---

### Q18.
Kube Proxy.

---

### Q19.
Container Runtime Interface (CRI).

---

### Q20.
Control Plane communication.

---

### Q21.
Worker node responsibilities.

---

### Q22.
Cluster lifecycle.

---

### Q23.
High Availability control plane.

---

### Q24.
Cluster bootstrapping.

---

### Q25.
Production architecture.

---

# 3. Pods

## Highest Priority

### Q26.
What is a Pod?

---

### Q27.
Why is Pod the smallest deployable unit?

---

### Q28.
Single-container vs Multi-container Pods.

---

### Q29.
Init Containers.

---

### Q30.
Sidecar Containers.

---

### Q31.
Pod lifecycle.

---

### Q32.
Pod phases.

---

### Q33.
Pod restart policies.

---

### Q34.
Pod resource requests.

---

### Q35.
Pod resource limits.

---

### Q36.
Liveness probes.

---

### Q37.
Readiness probes.

---

### Q38.
Startup probes.

---

### Q39.
Pod eviction.

---

### Q40.
Pod best practices.

---

# 4. ReplicaSets & Deployments

### Q41.
What is a ReplicaSet?

---

### Q42.
Deployment.

---

### Q43.
Deployment strategies.

---

### Q44.
Rolling Updates.

---

### Q45.
Recreate strategy.

---

### Q46.
Blue-Green deployments.

---

### Q47.
Canary deployments.

---

### Q48.
Deployment rollback.

---

### Q49.
Revision history.

---

### Q50.
Production recommendations.

---

# 5. Services

### Q51.
Why are Services needed?

---

### Q52.
ClusterIP.

---

### Q53.
NodePort.

---

### Q54.
LoadBalancer.

---

### Q55.
ExternalName.

---

### Q56.
Headless Service.

---

### Q57.
Service discovery.

---

### Q58.
DNS in Kubernetes.

---

### Q59.
EndpointSlices.

---

### Q60.
Service best practices.

---

# 6. Ingress

### Q61.
What is Ingress?

---

### Q62.
Ingress Controller.

---

### Q63.
Ingress vs LoadBalancer.

---

### Q64.
Host-based routing.

---

### Q65.
Path-based routing.

---

### Q66.
TLS termination.

---

### Q67.
SSL certificates.

---

### Q68.
NGINX Ingress Controller.

---

### Q69.
Ingress annotations.

---

### Q70.
Gateway API.

---

# 7. ConfigMaps & Secrets

### Q71.
ConfigMap.

---

### Q72.
Secret.

---

### Q73.
Environment variables.

---

### Q74.
Volume mounts.

---

### Q75.
Secret encryption.

---

### Q76.
Secret rotation.

---

### Q77.
External Secrets.

---

### Q78.
Configuration management.

---

### Q79.
Spring Boot configuration.

---

### Q80.
Best practices.

---

# 8. Volumes & Persistent Storage

### Q81.
Why are volumes required?

---

### Q82.
PersistentVolume (PV).

---

### Q83.
PersistentVolumeClaim (PVC).

---

### Q84.
StorageClass.

---

### Q85.
Dynamic provisioning.

---

### Q86.
CSI (Container Storage Interface).

---

### Q87.
Access modes.

---

### Q88.
Reclaim policies.

---

### Q89.
Volume snapshots.

---

### Q90.
Production storage.

---

# 9. Scheduling

### Q91.
How does Kubernetes scheduling work?

---

### Q92.
Node Selector.

---

### Q93.
Node Affinity.

---

### Q94.
Pod Affinity.

---

### Q95.
Pod Anti-Affinity.

---

### Q96.
Taints.

---

### Q97.
Tolerations.

---

### Q98.
Priority Classes.

---

### Q99.
Topology Spread Constraints.

---

### Q100.
Scheduling optimization.

---

# 10. Stateful Applications

### Q101.
StatefulSet.

---

### Q102.
Deployment vs StatefulSet.

---

### Q103.
Persistent identities.

---

### Q104.
Ordered deployment.

---

### Q105.
Ordered termination.

---

### Q106.
Stateful storage.

---

### Q107.
Headless Services.

---

### Q108.
Databases on Kubernetes.

---

### Q109.
ZooKeeper/Kafka deployment.

---

### Q110.
Production considerations.

---

# 11. Autoscaling

### Q111.
Horizontal Pod Autoscaler (HPA).

---

### Q112.
Vertical Pod Autoscaler (VPA).

---

### Q113.
Cluster Autoscaler.

---

### Q114.
Scaling metrics.

---

### Q115.
CPU utilization.

---

### Q116.
Memory utilization.

---

### Q117.
Custom metrics.

---

### Q118.
Scaling policies.

---

### Q119.
KEDA.

---

### Q120.
Autoscaling best practices.

---

# 12. Networking

### Q121.
Kubernetes networking model.

---

### Q122.
CNI (Container Network Interface).

---

### Q123.
Calico.

---

### Q124.
Flannel.

---

### Q125.
Cilium.

---

### Q126.
Network Policies.

---

### Q127.
Pod-to-Pod communication.

---

### Q128.
Pod-to-Service communication.

---

### Q129.
Ingress networking.

---

### Q130.
Network troubleshooting.

---

# 13. Security

## Advanced

### Q131.
RBAC.

---

### Q132.
Service Accounts.

---

### Q133.
Security Context.

---

### Q134.
Pod Security Standards.

---

### Q135.
Network Policies.

---

### Q136.
Admission Controllers.

---

### Q137.
OPA Gatekeeper.

---

### Q138.
Image security.

---

### Q139.
Secrets security.

---

### Q140.
Production security checklist.

---

# 14. Monitoring & Troubleshooting

### Q141.
kubectl debugging.

---

### Q142.
Logs.

---

### Q143.
Events.

---

### Q144.
Metrics Server.

---

### Q145.
Prometheus.

---

### Q146.
Grafana.

---

### Q147.
Loki.

---

### Q148.
Jaeger.

---

### Q149.
CrashLoopBackOff.

---

### Q150.
ImagePullBackOff.

---

### Q151.
Pending Pods.

---

### Q152.
OOMKilled.

---

### Q153.
Node failures.

---

### Q154.
Control Plane troubleshooting.

---

### Q155.
Production debugging workflow.

---

# 15. Kubernetes Best Practices

### Q156.
Resource requests and limits.

---

### Q157.
Health probes.

---

### Q158.
Rolling updates.

---

### Q159.
Immutable containers.

---

### Q160.
Namespace strategy.

---

### Q161.
Resource quotas.

---

### Q162.
LimitRanges.

---

### Q163.
GitOps.

---

### Q164.
Helm.

---

### Q165.
Production checklist.

---

# 16. Advanced Kubernetes Concepts

### Q166.
Custom Resource Definitions (CRDs).

---

### Q167.
Operators.

---

### Q168.
Admission Webhooks.

---

### Q169.
API Aggregation.

---

### Q170.
Custom Scheduler.

---

### Q171.
Service Mesh.

---

### Q172.
Istio.

---

### Q173.
Linkerd.

---

### Q174.
Multi-cluster Kubernetes.

---

### Q175.
Multi-tenancy.

---

### Q176.
Cluster Federation.

---

### Q177.
Helm Charts.

---

### Q178.
Kustomize.

---

### Q179.
GitOps with ArgoCD.

---

### Q180.
Production architecture evolution.

---

# 17. Scenario-Based Questions

### Q181.
A Pod is stuck in Pending state. How would you troubleshoot it?

---

### Q182.
A Deployment rollout fails midway. How would you recover?

---

### Q183.
Pods are restarting continuously with CrashLoopBackOff. How would you investigate?

---

### Q184.
How would you deploy a highly available Spring Boot application on Kubernetes?

---

### Q185.
A service is unreachable inside the cluster. What debugging steps would you take?

---

### Q186.
How would you deploy PostgreSQL on Kubernetes?

---

### Q187.
How would you deploy Kafka on Kubernetes?

---

### Q188.
Your application requires zero-downtime deployments. How would you configure Kubernetes?

---

### Q189.
A node becomes unavailable unexpectedly. What happens?

---

### Q190.
How would you migrate Docker Compose applications to Kubernetes?

---

### Q191.
How would you scale an event-driven application based on Kafka lag?

---

### Q192.
Your application requires persistent storage across restarts. How would you design it?

---

### Q193.
A cluster upgrade is required with minimal downtime. How would you approach it?

---

### Q194.
How would you secure secrets in a production Kubernetes cluster?

---

### Q195.
How would you review Kubernetes manifests during a code review?

---

# 18. Production Experience Questions

### Q196.
Have you deployed Spring Boot applications on Kubernetes?

---

### Q197.
How do you monitor Kubernetes clusters?

---

### Q198.
How do you troubleshoot production Pods?

---

### Q199.
How do you manage configuration across environments?

---

### Q200.
How do you perform rolling upgrades?

---

### Q201.
How do you manage Kubernetes manifests?

---

### Q202.
Have you used Helm?

---

### Q203.
How do you implement autoscaling?

---

### Q204.
How do you secure production clusters?

---

### Q205.
What Kubernetes-related production incident taught you the most?

---

# 19. "Why" Questions

### Q206.
Why are Pods ephemeral?

---

### Q207.
Why should Deployments be preferred over directly creating Pods?

---

### Q208.
Why are resource requests important?

---

### Q209.
Why should readiness probes be configured separately from liveness probes?

---

### Q210.
Why should StatefulSets be used for databases?

---

### Q211.
Why should ConfigMaps and Secrets be separated?

---

### Q212.
Why is RBAC essential?

---

### Q213.
Why are Network Policies important?

---

### Q214.
Why should images be immutable?

---

### Q215.
Why is Kubernetes declarative rather than imperative?

---

# 20. Trade-off Questions

### Q216.
Deployment vs StatefulSet.

---

### Q217.
Pod vs Container.

---

### Q218.
ReplicaSet vs Deployment.

---

### Q219.
ConfigMap vs Secret.

---

### Q220.
ClusterIP vs NodePort vs LoadBalancer.

---

### Q221.
Ingress vs API Gateway.

---

### Q222.
HPA vs VPA.

---

### Q223.
Helm vs Kustomize.

---

### Q224.
Docker Compose vs Kubernetes.

---

### Q225.
Service Mesh vs Traditional Networking.

---

# 21. Common Interview Follow-up Questions

## If you mention Pods
- Init Containers?
- Sidecars?
- Probes?
- Lifecycle?
- Resources?

---

## If you mention Deployments
- Rolling updates?
- Rollback?
- ReplicaSet?
- Canary?
- Blue-Green?

---

## If you mention Services
- ClusterIP?
- NodePort?
- LoadBalancer?
- DNS?
- EndpointSlices?

---

## If you mention Storage
- PV?
- PVC?
- StorageClass?
- CSI?
- Snapshots?

---

## If you mention Security
- RBAC?
- Service Accounts?
- Network Policies?
- Secrets?
- Pod Security?

---

## If you mention Scaling
- HPA?
- VPA?
- Cluster Autoscaler?
- Metrics?
- KEDA?

---

# Staff Engineer Discussion Questions

### Q226.
How would you design a Kubernetes platform for hundreds of microservices?

---

### Q227.
How would you standardize Kubernetes deployments across engineering teams?

---

### Q228.
How would you migrate thousands of Docker workloads to Kubernetes?

---

### Q229.
How would you design a secure multi-tenant Kubernetes platform?

---

### Q230.
How would you establish Kubernetes governance across the organization?

---

### Q231.
How would you optimize cluster utilization and reduce infrastructure cost?

---

### Q232.
How would you prepare Kubernetes clusters for disaster recovery?

---

### Q233.
How would you implement GitOps organization-wide?

---

### Q234.
Which Kubernetes metrics would you continuously monitor?

---

### Q235.
If you were designing an enterprise Kubernetes platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Kubernetes
- [ ] Cluster
- [ ] Control Plane
- [ ] Worker Nodes
- [ ] Container Runtime

## Core Resources
- [ ] Pods
- [ ] Deployments
- [ ] ReplicaSets
- [ ] Services
- [ ] Ingress

## Configuration
- [ ] ConfigMaps
- [ ] Secrets
- [ ] Environment Variables
- [ ] Health Probes
- [ ] Resource Limits

## Storage
- [ ] PV
- [ ] PVC
- [ ] StorageClass
- [ ] CSI
- [ ] StatefulSets

## Scheduling
- [ ] Affinity
- [ ] Anti-Affinity
- [ ] Taints
- [ ] Tolerations
- [ ] Priority Classes

## Security
- [ ] RBAC
- [ ] Service Accounts
- [ ] Network Policies
- [ ] Pod Security
- [ ] Admission Controllers

## Operations
- [ ] Autoscaling
- [ ] Monitoring
- [ ] Helm
- [ ] GitOps
- [ ] Troubleshooting

## Interview Readiness
- [ ] Can explain Kubernetes architecture from first principles.
- [ ] Can design highly available deployments with proper networking and storage.
- [ ] Can troubleshoot common production failures such as CrashLoopBackOff and Pending Pods.
- [ ] Can discuss Kubernetes security, autoscaling, and observability.
- [ ] Can confidently design production-ready Kubernetes platforms for microservices.

---

**Total Questions:** 235

**Recommended Time:** 7–8 Days

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** Kubernetes Architecture, Pods, Deployments, Services, Ingress, ConfigMaps, Secrets, StatefulSets, Persistent Volumes, Scheduling, Autoscaling, RBAC, Network Policies, Helm, GitOps, Production Troubleshooting