# Docker Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Google, Uber, LinkedIn, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** Docker, Java, Spring Boot, Kubernetes, CI/CD, Microservices, Cloud
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Docker is one of the most frequently asked DevOps topics in backend interviews. Interviewers expect candidates to understand containerization, Docker architecture, images, containers, networking, storage, Docker Compose, security, optimization, and deploying production-ready microservices.

---

# Table of Contents

1. Containerization Fundamentals
2. Docker Architecture
3. Docker Images
4. Docker Containers
5. Dockerfile
6. Docker Volumes & Storage
7. Docker Networking
8. Docker Compose
9. Docker Registry
10. Docker Security
11. Docker Performance & Optimization
12. Docker in CI/CD
13. Docker with Spring Boot
14. Docker Best Practices
15. Advanced Docker Concepts
16. Scenario-Based Questions
17. Production Experience
18. Why Questions
19. Trade-offs
20. Common Follow-up Questions

---

# 1. Containerization Fundamentals

## Basic

### Q1.
What is Docker?

**Follow-ups**
- Why was Docker introduced?
- What problems does Docker solve?

---

### Q2.
What is containerization?

---

### Q3.
Container vs Virtual Machine.

---

### Q4.
Benefits of containers.

---

### Q5.
Disadvantages of containers.

---

### Q6.
What is a container image?

---

### Q7.
What is a container runtime?

---

### Q8.
Docker vs Hypervisor.

---

### Q9.
When should Docker be used?

---

### Q10.
When should Docker NOT be used?

---

# 2. Docker Architecture

## Intermediate

### Q11.
Explain Docker architecture.

---

### Q12.
Docker Client.

---

### Q13.
Docker Daemon.

---

### Q14.
Docker Engine.

---

### Q15.
Docker API.

---

### Q16.
Container Runtime.

---

### Q17.
containerd.

---

### Q18.
runc.

---

### Q19.
Namespaces.

---

### Q20.
Control Groups (cgroups).

---

### Q21.
Union File System.

---

### Q22.
OverlayFS.

---

### Q23.
Image layers.

---

### Q24.
Container lifecycle.

---

### Q25.
Docker architecture in production.

---

# 3. Docker Images

### Q26.
What is a Docker image?

---

### Q27.
Image layers.

---

### Q28.
Image caching.

---

### Q29.
Image tagging.

---

### Q30.
Image digest.

---

### Q31.
Base images.

---

### Q32.
Alpine vs Ubuntu images.

---

### Q33.
Scratch image.

---

### Q34.
Image pull policy.

---

### Q35.
Image best practices.

---

# 4. Docker Containers

### Q36.
Container lifecycle.

---

### Q37.
Container states.

---

### Q38.
Container isolation.

---

### Q39.
Container restart policies.

---

### Q40.
Container logs.

---

### Q41.
Environment variables.

---

### Q42.
Container health checks.

---

### Q43.
Container resource limits.

---

### Q44.
Container cleanup.

---

### Q45.
Production container management.

---

# 5. Dockerfile

## Highest Priority

### Q46.
What is a Dockerfile?

---

### Q47.
Common Dockerfile instructions.

---

### Q48.
FROM.

---

### Q49.
RUN.

---

### Q50.
COPY vs ADD.

---

### Q51.
CMD vs ENTRYPOINT.

---

### Q52.
EXPOSE.

---

### Q53.
WORKDIR.

---

### Q54.
ENV.

---

### Q55.
ARG.

---

### Q56.
LABEL.

---

### Q57.
USER.

---

### Q58.
HEALTHCHECK.

---

### Q59.
ONBUILD.

---

### Q60.
Multi-stage builds.

---

### Q61.
Layer caching.

---

### Q62.
Build context.

---

### Q63.
.dockerignore.

---

### Q64.
Image optimization.

---

### Q65.
Dockerfile best practices.

---

# 6. Docker Volumes & Storage

### Q66.
Why are Docker volumes required?

---

### Q67.
Named volumes.

---

### Q68.
Bind mounts.

---

### Q69.
tmpfs mounts.

---

### Q70.
Volume lifecycle.

---

### Q71.
Persistent storage.

---

### Q72.
Sharing volumes.

---

### Q73.
Volume backup.

---

### Q74.
Storage drivers.

---

### Q75.
Production recommendations.

---

# 7. Docker Networking

### Q76.
Docker networking overview.

---

### Q77.
Bridge network.

---

### Q78.
Host network.

---

### Q79.
Overlay network.

---

### Q80.
None network.

---

### Q81.
Container DNS.

---

### Q82.
Port mapping.

---

### Q83.
Inter-container communication.

---

### Q84.
Service discovery.

---

### Q85.
Network troubleshooting.

---

# 8. Docker Compose

### Q86.
What is Docker Compose?

---

### Q87.
docker-compose.yml structure.

---

### Q88.
Multiple services.

---

### Q89.
Networks in Compose.

---

### Q90.
Volumes in Compose.

---

### Q91.
Environment variables.

---

### Q92.
depends_on.

---

### Q93.
Profiles.

---

### Q94.
Compose overrides.

---

### Q95.
Production limitations.

---

# 9. Docker Registry

### Q96.
Docker Hub.

---

### Q97.
Private registries.

---

### Q98.
Image repositories.

---

### Q99.
Image tagging strategy.

---

### Q100.
Image signing.

---

### Q101.
Image scanning.

---

### Q102.
Registry authentication.

---

### Q103.
Versioning images.

---

### Q104.
Artifact repositories.

---

### Q105.
Production best practices.

---

# 10. Docker Security

## Advanced

### Q106.
Container security.

---

### Q107.
Running as non-root.

---

### Q108.
Least privilege.

---

### Q109.
Image vulnerabilities.

---

### Q110.
Secrets management.

---

### Q111.
Read-only filesystem.

---

### Q112.
Capabilities.

---

### Q113.
Seccomp.

---

### Q114.
AppArmor.

---

### Q115.
SELinux.

---

### Q116.
Image signing.

---

### Q117.
Supply chain security.

---

### Q118.
Rootless Docker.

---

### Q119.
Security scanning.

---

### Q120.
Production security checklist.

---

# 11. Docker Performance & Optimization

### Q121.
Reducing image size.

---

### Q122.
Layer optimization.

---

### Q123.
Build cache optimization.

---

### Q124.
Multi-stage builds.

---

### Q125.
Startup optimization.

---

### Q126.
Container resource tuning.

---

### Q127.
CPU limits.

---

### Q128.
Memory limits.

---

### Q129.
OOMKilled.

---

### Q130.
Performance monitoring.

---

# 12. Docker in CI/CD

### Q131.
Docker in CI pipelines.

---

### Q132.
Docker in CD pipelines.

---

### Q133.
Build automation.

---

### Q134.
Image versioning.

---

### Q135.
Immutable deployments.

---

### Q136.
Rolling deployments.

---

### Q137.
Blue-Green deployments.

---

### Q138.
Canary deployments.

---

### Q139.
Artifact promotion.

---

### Q140.
Pipeline best practices.

---

# 13. Docker with Spring Boot

### Q141.
Dockerizing a Spring Boot application.

---

### Q142.
Optimizing JVM inside Docker.

---

### Q143.
JDK vs JRE images.

---

### Q144.
Spring Boot layered jars.

---

### Q145.
Externalized configuration.

---

### Q146.
Environment profiles.

---

### Q147.
Actuator health checks.

---

### Q148.
Graceful shutdown.

---

### Q149.
Logging.

---

### Q150.
Production recommendations.

---

# 14. Docker Best Practices

### Q151.
Keep images small.

---

### Q152.
One process per container.

---

### Q153.
Immutable infrastructure.

---

### Q154.
Avoid storing secrets.

---

### Q155.
Use official images.

---

### Q156.
Pin image versions.

---

### Q157.
Use non-root users.

---

### Q158.
Optimize build cache.

---

### Q159.
Health checks.

---

### Q160.
Production checklist.

---

# 15. Advanced Docker Concepts

### Q161.
Docker BuildKit.

---

### Q162.
Buildx.

---

### Q163.
Multi-platform images.

---

### Q164.
Rootless Docker.

---

### Q165.
Docker Swarm.

---

### Q166.
Swarm vs Kubernetes.

---

### Q167.
Docker plugins.

---

### Q168.
Container runtimes.

---

### Q169.
OCI standards.

---

### Q170.
Future of Docker.

---

# 16. Scenario-Based Questions

### Q171.
Your Docker image is 2 GB. How would you reduce its size?

---

### Q172.
A Spring Boot container takes two minutes to start. How would you investigate?

---

### Q173.
A container repeatedly exits immediately after startup. How would you debug it?

---

### Q174.
Your application loses uploaded files after container restart. How would you fix it?

---

### Q175.
A Java application is OOMKilled inside Docker. How would you investigate?

---

### Q176.
Your Docker build is very slow in CI. How would you optimize it?

---

### Q177.
How would you dockerize a microservice that depends on PostgreSQL, Redis, and Kafka for local development?

---

### Q178.
A vulnerability scanner reports critical CVEs in your image. What steps would you take?

---

### Q179.
How would you securely pass database credentials to a Docker container?

---

### Q180.
How would you prepare a Docker image for deployment to Kubernetes?

---

### Q181.
How would you troubleshoot networking issues between two containers?

---

### Q182.
How would you migrate from Docker Compose to Kubernetes?

---

### Q183.
A production container becomes unhealthy intermittently. How would you investigate?

---

### Q184.
How would you implement zero-downtime deployment for Dockerized services?

---

### Q185.
How would you review a teammate's Dockerfile during a code review?

---

# 17. Production Experience Questions

### Q186.
Have you containerized Spring Boot applications?

---

### Q187.
How do you optimize Docker images?

---

### Q188.
How do you manage secrets in production?

---

### Q189.
How do you monitor Docker containers?

---

### Q190.
How do you debug production containers?

---

### Q191.
Have you used Docker Compose in development?

---

### Q192.
How do you build Docker images in CI/CD?

---

### Q193.
How do you version container images?

---

### Q194.
How do you secure Docker images?

---

### Q195.
What Docker-related production incident taught you the most?

---

# 18. "Why" Questions

### Q196.
Why are containers more lightweight than virtual machines?

---

### Q197.
Why should Docker images be immutable?

---

### Q198.
Why is multi-stage build recommended?

---

### Q199.
Why should containers run as non-root?

---

### Q200.
Why should COPY generally be preferred over ADD?

---

### Q201.
Why is CMD different from ENTRYPOINT?

---

### Q202.
Why should images be as small as possible?

---

### Q203.
Why should secrets never be baked into images?

---

### Q204.
Why should image tags be immutable?

---

### Q205.
Why is Docker Compose not commonly used in production at scale?

---

# 19. Trade-off Questions

### Q206.
Container vs Virtual Machine.

---

### Q207.
Docker Compose vs Kubernetes.

---

### Q208.
Alpine vs Ubuntu images.

---

### Q209.
COPY vs ADD.

---

### Q210.
CMD vs ENTRYPOINT.

---

### Q211.
Bind Mount vs Named Volume.

---

### Q212.
Docker Swarm vs Kubernetes.

---

### Q213.
JDK Image vs JRE Image.

---

### Q214.
Single-stage vs Multi-stage Docker Build.

---

### Q215.
Official Image vs Custom Base Image.

---

# 20. Common Interview Follow-up Questions

## If you mention Docker
- Container?
- Image?
- Daemon?
- Runtime?
- Namespaces?

---

## If you mention Dockerfile
- COPY?
- ADD?
- CMD?
- ENTRYPOINT?
- Multi-stage?

---

## If you mention Volumes
- Bind mounts?
- Named volumes?
- Persistence?
- Backup?
- Storage drivers?

---

## If you mention Networking
- Bridge?
- Host?
- Overlay?
- DNS?
- Port mapping?

---

## If you mention Security
- Non-root?
- Secrets?
- Vulnerabilities?
- Seccomp?
- Rootless Docker?

---

## If you mention CI/CD
- Image versioning?
- Registry?
- Rolling deployment?
- Build cache?
- Immutable images?

---

# Staff Engineer Discussion Questions

### Q216.
How would you standardize Docker image creation across hundreds of microservices?

---

### Q217.
How would you optimize Docker build pipelines for a large engineering organization?

---

### Q218.
How would you establish secure container image governance?

---

### Q219.
How would you migrate a legacy VM-based deployment platform to Docker containers?

---

### Q220.
How would you review Dockerfiles for security and performance?

---

### Q221.
How would you minimize container startup time across an enterprise platform?

---

### Q222.
How would you prepare Dockerized services for Kubernetes deployment?

---

### Q223.
What organization-wide Docker best practices would you enforce?

---

### Q224.
Which Docker metrics would you continuously monitor in production?

---

### Q225.
If you were designing a container platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Docker
- [ ] Containers
- [ ] Images
- [ ] Docker Engine
- [ ] Container Runtime

## Dockerfile
- [ ] FROM
- [ ] RUN
- [ ] COPY
- [ ] CMD vs ENTRYPOINT
- [ ] Multi-stage Builds

## Storage
- [ ] Volumes
- [ ] Bind Mounts
- [ ] Persistent Storage
- [ ] Storage Drivers
- [ ] Backup Strategy

## Networking
- [ ] Bridge Network
- [ ] Host Network
- [ ] Overlay Network
- [ ] DNS
- [ ] Port Mapping

## Security
- [ ] Non-root Containers
- [ ] Secrets Management
- [ ] Vulnerability Scanning
- [ ] Image Signing
- [ ] Rootless Docker

## Performance
- [ ] Layer Caching
- [ ] Image Optimization
- [ ] Resource Limits
- [ ] Multi-stage Builds
- [ ] BuildKit

## Production
- [ ] Docker Compose
- [ ] CI/CD Integration
- [ ] Monitoring
- [ ] Logging
- [ ] Troubleshooting

## Interview Readiness
- [ ] Can explain Docker architecture from image build to container execution.
- [ ] Can write production-ready Dockerfiles with multi-stage builds.
- [ ] Can troubleshoot container startup, networking, storage, and resource issues.
- [ ] Can discuss Docker security, optimization, and CI/CD integration.
- [ ] Can confidently compare Docker with VMs and Kubernetes.

---

**Total Questions:** 225

**Recommended Time:** 5–6 Days

**Interview Weight:** ⭐⭐⭐⭐☆ (Very High)

**Most Frequently Asked Topics:** Docker Architecture, Dockerfile, Multi-stage Builds, Images vs Containers, Volumes, Networking, Docker Compose, Security, Resource Limits, Docker with Spring Boot, CI/CD Integration, Docker Best Practices