# Microservices Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Uber, LinkedIn, Google, Atlassian, Walmart Global Tech, Adobe, Salesforce, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Architecture Focus:** Spring Boot, Spring Cloud, Docker, Kubernetes, Kafka, REST, gRPC, Distributed Systems
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Microservices is one of the most heavily tested backend topics. Interviewers expect candidates to understand not only what microservices are, but also service decomposition, communication, resiliency, distributed transactions, observability, deployment, scaling, data consistency, and production trade-offs.

---

# Table of Contents

1. Microservices Fundamentals
2. Monolith vs Microservices
3. Service Decomposition
4. Service Communication
5. API Gateway
6. Service Discovery
7. Configuration Management
8. Distributed Transactions
9. Data Management
10. Resilience & Fault Tolerance
11. Circuit Breakers & Retries
12. Observability
13. Security
14. Deployment & Scaling
15. Spring Cloud
16. Advanced Microservices Patterns
17. Scenario-Based Questions
18. Production Experience
19. Why Questions
20. Trade-offs
21. Common Follow-up Questions

---

# 1. Microservices Fundamentals

## Basic

### Q1.
What are Microservices?

**Follow-ups**
- Why were Microservices introduced?
- What problems do they solve?

---

### Q2.
What are the characteristics of a Microservice architecture?

---

### Q3.
Monolithic Architecture vs Microservices.

---

### Q4.
Advantages of Microservices.

---

### Q5.
Disadvantages of Microservices.

---

### Q6.
When should Microservices NOT be used?

---

### Q7.
What is a bounded context?

---

### Q8.
What is Domain-Driven Design (DDD) and how does it influence Microservices?

---

### Q9.
Business capability decomposition.

---

### Q10.
What makes a "good" microservice?

---

### Q11.
How big should a microservice be?

---

### Q12.
Single Responsibility Principle in Microservices.

---

### Q13.
What is database-per-service?

---

### Q14.
Shared database vs database-per-service.

---

### Q15.
How do you identify service boundaries?

---

# 2. Monolith vs Microservices

### Q16.
When would you choose a monolith over microservices?

---

### Q17.
Why do many organizations start with a monolith?

---

### Q18.
Distributed Monolith.

---

### Q19.
Signs that a monolith should be split.

---

### Q20.
Common mistakes while migrating from a monolith.

---

### Q21.
Microservices vs Modular Monolith.

---

### Q22.
Operational complexity comparison.

---

### Q23.
Deployment comparison.

---

### Q24.
Scalability comparison.

---

### Q25.
Cost comparison.

---

# 3. Service Decomposition

## Intermediate

### Q26.
Decomposition by Business Capability.

---

### Q27.
Decomposition by Subdomain.

---

### Q28.
Event Storming.

---

### Q29.
Identifying aggregates.

---

### Q30.
Shared libraries across services.

---

### Q31.
How do you avoid tight coupling?

---

### Q32.
How do you split a User Service?

---

### Q33.
How would you decompose an E-commerce platform?

---

### Q34.
How do you prevent chatty communication?

---

### Q35.
How do you evolve service boundaries?

---

# 4. Service Communication

### Q36.
Synchronous communication.

---

### Q37.
Asynchronous communication.

---

### Q38.
REST vs gRPC.

---

### Q39.
REST vs Messaging.

---

### Q40.
Kafka vs RabbitMQ.

---

### Q41.
Event-driven architecture.

---

### Q42.
Command vs Event.

---

### Q43.
Request-Reply pattern.

---

### Q44.
Message ordering.

---

### Q45.
Message durability.

---

### Q46.
Idempotent consumers.

---

### Q47.
Exactly-once vs At-least-once.

---

### Q48.
Dead Letter Queue (DLQ).

---

### Q49.
Schema evolution.

---

### Q50.
Communication best practices.

---

# 5. API Gateway

### Q51.
What is an API Gateway?

---

### Q52.
Why use an API Gateway?

---

### Q53.
Gateway responsibilities.

---

### Q54.
Routing.

---

### Q55.
Authentication.

---

### Q56.
Rate limiting.

---

### Q57.
Request aggregation.

---

### Q58.
API Gateway vs Load Balancer.

---

### Q59.
Gateway failure handling.

---

### Q60.
Gateway anti-patterns.

---

# 6. Service Discovery

### Q61.
Why is Service Discovery needed?

---

### Q62.
Client-side discovery.

---

### Q63.
Server-side discovery.

---

### Q64.
Eureka.

---

### Q65.
Consul.

---

### Q66.
Kubernetes Service Discovery.

---

### Q67.
DNS-based discovery.

---

### Q68.
Health checks.

---

### Q69.
Load balancing.

---

### Q70.
Production considerations.

---

# 7. Configuration Management

### Q71.
Externalized configuration.

---

### Q72.
Spring Cloud Config.

---

### Q73.
Config Server.

---

### Q74.
Configuration refresh.

---

### Q75.
Secrets management.

---

### Q76.
Vault integration.

---

### Q77.
Kubernetes ConfigMaps.

---

### Q78.
Kubernetes Secrets.

---

### Q79.
Configuration versioning.

---

### Q80.
Best practices.

---

# 8. Distributed Transactions

## Advanced

### Q81.
Why are distributed transactions difficult?

---

### Q82.
Saga Pattern.

---

### Q83.
Orchestration Saga.

---

### Q84.
Choreography Saga.

---

### Q85.
Compensating Transactions.

---

### Q86.
Outbox Pattern.

---

### Q87.
Inbox Pattern.

---

### Q88.
Transactional Messaging.

---

### Q89.
Two-Phase Commit (2PC).

---

### Q90.
Why is 2PC rarely used?

---

### Q91.
Eventual Consistency.

---

### Q92.
Idempotency in distributed systems.

---

### Q93.
Duplicate event handling.

---

### Q94.
Distributed rollback.

---

### Q95.
Production transaction strategies.

---

# 9. Data Management

### Q96.
Database-per-service.

---

### Q97.
Shared database anti-pattern.

---

### Q98.
CQRS.

---

### Q99.
Event Sourcing.

---

### Q100.
Read Models.

---

### Q101.
Materialized Views.

---

### Q102.
Data replication.

---

### Q103.
Data synchronization.

---

### Q104.
Cross-service joins.

---

### Q105.
Reporting across services.

---

# 10. Resilience & Fault Tolerance

### Q106.
Fault tolerance.

---

### Q107.
Bulkhead Pattern.

---

### Q108.
Timeouts.

---

### Q109.
Retries.

---

### Q110.
Fallbacks.

---

### Q111.
Graceful degradation.

---

### Q112.
Fail Fast.

---

### Q113.
Load shedding.

---

### Q114.
Backpressure.

---

### Q115.
Chaos Engineering.

---

# 11. Circuit Breakers & Retries

### Q116.
Circuit Breaker Pattern.

---

### Q117.
Open state.

---

### Q118.
Half-open state.

---

### Q119.
Closed state.

---

### Q120.
Retry Pattern.

---

### Q121.
Exponential Backoff.

---

### Q122.
Jitter.

---

### Q123.
Retry storms.

---

### Q124.
Resilience4j.

---

### Q125.
Hystrix (legacy).

---

# 12. Observability

### Q126.
Logging.

---

### Q127.
Centralized logging.

---

### Q128.
Correlation IDs.

---

### Q129.
Distributed tracing.

---

### Q130.
OpenTelemetry.

---

### Q131.
Zipkin.

---

### Q132.
Jaeger.

---

### Q133.
Prometheus.

---

### Q134.
Grafana.

---

### Q135.
Health checks.

---

### Q136.
Liveness probes.

---

### Q137.
Readiness probes.

---

### Q138.
Metrics.

---

### Q139.
SLIs, SLOs, SLAs.

---

### Q140.
Production monitoring.

---

# 13. Security

### Q141.
JWT authentication.

---

### Q142.
OAuth2 in microservices.

---

### Q143.
API Gateway authentication.

---

### Q144.
Service-to-service authentication.

---

### Q145.
mTLS.

---

### Q146.
Zero Trust Architecture.

---

### Q147.
Secret management.

---

### Q148.
Least privilege.

---

### Q149.
Rate limiting.

---

### Q150.
Security best practices.

---

# 14. Deployment & Scaling

### Q151.
Docker.

---

### Q152.
Containerization.

---

### Q153.
Kubernetes.

---

### Q154.
Horizontal scaling.

---

### Q155.
Vertical scaling.

---

### Q156.
Rolling deployments.

---

### Q157.
Blue-Green deployments.

---

### Q158.
Canary deployments.

---

### Q159.
Auto Scaling.

---

### Q160.
Resource limits.

---

### Q161.
Readiness probes.

---

### Q162.
Liveness probes.

---

### Q163.
Pod disruption.

---

### Q164.
Service Mesh.

---

### Q165.
Istio overview.

---

# 15. Spring Cloud

### Q166.
Spring Cloud overview.

---

### Q167.
Spring Cloud Gateway.

---

### Q168.
Spring Cloud Config.

---

### Q169.
Spring Cloud Bus.

---

### Q170.
OpenFeign.

---

### Q171.
Feign Client.

---

### Q172.
LoadBalancer.

---

### Q173.
Circuit Breaker integration.

---

### Q174.
Service Discovery integration.

---

### Q175.
Spring Cloud architecture.

---

# 16. Advanced Microservices Patterns

### Q176.
Strangler Fig Pattern.

---

### Q177.
Anti-Corruption Layer.

---

### Q178.
Backend for Frontend (BFF).

---

### Q179.
Sidecar Pattern.

---

### Q180.
Ambassador Pattern.

---

### Q181.
Adapter Pattern.

---

### Q182.
Aggregator Pattern.

---

### Q183.
API Composition.

---

### Q184.
Database-per-service pattern.

---

### Q185.
Event-carried State Transfer.

---

### Q186.
Claim Check Pattern.

---

### Q187.
Transactional Outbox.

---

### Q188.
Inbox Pattern.

---

### Q189.
Competing Consumers.

---

### Q190.
Consumer Groups.

---

# 17. Scenario-Based Questions

### Q191.
How would you split a monolith into microservices?

---

### Q192.
Your Order Service must update Inventory and Payment atomically. How would you design the workflow?

---

### Q193.
A downstream service becomes unavailable. How would your service respond?

---

### Q194.
Your API Gateway becomes a bottleneck. How would you scale it?

---

### Q195.
One microservice frequently fails and causes cascading failures. How would you solve it?

---

### Q196.
How would you design a notification system using event-driven architecture?

---

### Q197.
Your services frequently call each other in long synchronous chains. How would you improve the architecture?

---

### Q198.
You need to deploy a breaking change without downtime. What deployment strategy would you choose?

---

### Q199.
How would you migrate from a shared database to database-per-service?

---

### Q200.
A Kafka consumer processes duplicate events. How would you guarantee correctness?

---

# 18. Production Experience Questions

### Q201.
Have you designed microservices from scratch?

---

### Q202.
How did you identify service boundaries?

---

### Q203.
How did you handle distributed transactions?

---

### Q204.
Have you implemented Saga or Outbox patterns?

---

### Q205.
How did you debug production issues across multiple services?

---

### Q206.
How do you monitor microservices?

---

### Q207.
How do you secure service-to-service communication?

---

### Q208.
Have you used Spring Cloud components?

---

### Q209.
How do you review microservice designs?

---

### Q210.
What production incident taught you the most about distributed systems?

---

# 19. "Why" Questions

### Q211.
Why should each microservice own its own database?

---

### Q212.
Why is synchronous communication dangerous at scale?

---

### Q213.
Why are distributed transactions avoided?

---

### Q214.
Why is Saga preferred over XA transactions?

---

### Q215.
Why is eventual consistency acceptable?

---

### Q216.
Why should services communicate through events?

---

### Q217.
Why should API Gateways remain lightweight?

---

### Q218.
Why are circuit breakers important?

---

### Q219.
Why should microservices be independently deployable?

---

### Q220.
Why shouldn't every module become a separate microservice?

---

# 20. Trade-off Questions

### Q221.
Monolith vs Microservices.

---

### Q222.
REST vs gRPC.

---

### Q223.
REST vs Kafka.

---

### Q224.
Orchestration Saga vs Choreography Saga.

---

### Q225.
Shared Database vs Database-per-Service.

---

### Q226.
API Gateway vs Backend for Frontend.

---

### Q227.
Synchronous vs Asynchronous Communication.

---

### Q228.
Event Sourcing vs Traditional CRUD.

---

### Q229.
Service Discovery vs Static Configuration.

---

### Q230.
Canary vs Blue-Green Deployment.

---

# 21. Common Interview Follow-up Questions

## If you mention Microservices
- Bounded Context?
- DDD?
- Database-per-service?
- Deployment?
- Scaling?

---

## If you mention Communication
- REST?
- Kafka?
- gRPC?
- Retries?
- Idempotency?

---

## If you mention Distributed Transactions
- Saga?
- Outbox?
- Inbox?
- Compensating Transactions?
- XA?

---

## If you mention Resilience
- Circuit Breaker?
- Retry?
- Timeout?
- Bulkhead?
- Backpressure?

---

## If you mention Deployment
- Docker?
- Kubernetes?
- Canary?
- Blue-Green?
- Auto Scaling?

---

## If you mention Observability
- Tracing?
- Correlation IDs?
- Metrics?
- Logging?
- Health Checks?

---

# Staff Engineer Discussion Questions

### Q231.
How would you define service boundaries for a new enterprise platform?

---

### Q232.
How would you prevent a distributed monolith from emerging?

---

### Q233.
How would you standardize communication patterns across hundreds of services?

---

### Q234.
How would you design a resilient payment platform handling millions of requests per day?

---

### Q235.
How would you migrate a legacy monolith with minimal business disruption?

---

### Q236.
How would you establish organization-wide API governance?

---

### Q237.
How would you implement organization-wide observability?

---

### Q238.
How would you review a microservice architecture for scalability bottlenecks?

---

### Q239.
What metrics indicate an unhealthy microservice ecosystem?

---

### Q240.
If you were designing a new cloud-native platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Microservices Architecture
- [ ] DDD
- [ ] Bounded Context
- [ ] Service Decomposition
- [ ] Database-per-Service

## Communication
- [ ] REST
- [ ] gRPC
- [ ] Kafka
- [ ] Event-driven Architecture
- [ ] API Gateway

## Reliability
- [ ] Saga Pattern
- [ ] Outbox Pattern
- [ ] Inbox Pattern
- [ ] Eventual Consistency
- [ ] Idempotency

## Resilience
- [ ] Circuit Breaker
- [ ] Retry
- [ ] Timeout
- [ ] Bulkhead
- [ ] Backpressure

## Observability
- [ ] Logging
- [ ] Tracing
- [ ] Metrics
- [ ] Health Checks
- [ ] Correlation IDs

## Deployment
- [ ] Docker
- [ ] Kubernetes
- [ ] Rolling Updates
- [ ] Canary
- [ ] Blue-Green

## Security
- [ ] OAuth2
- [ ] JWT
- [ ] mTLS
- [ ] Service-to-Service Authentication
- [ ] Secret Management

## Interview Readiness
- [ ] Can explain when to use (and avoid) microservices.
- [ ] Can design service boundaries using DDD principles.
- [ ] Can compare synchronous and asynchronous communication.
- [ ] Can design resilient distributed systems using Saga and Outbox patterns.
- [ ] Can discuss production deployment, observability, and scaling strategies.

---

**Total Questions:** 240
**Recommended Time:** 7–8 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
**Most Frequently Asked Topics:** Monolith vs Microservices, DDD, Service Decomposition, API Gateway, Service Discovery, Saga Pattern, Outbox Pattern, Event-Driven Architecture, Circuit Breaker, Resilience4j, Kubernetes, Observability, Distributed Transactions, Deployment Strategies