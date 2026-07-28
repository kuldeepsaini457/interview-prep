# Distributed Systems Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Google, Uber, LinkedIn, Meta, Apple, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** Java, Spring Boot, Kafka, Redis, Kubernetes, Cloud, Distributed Databases
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Distributed Systems is one of the most important backend interview topics because almost every large-scale backend application today is distributed. Interviewers expect candidates to understand consistency, replication, partitioning, consensus, distributed transactions, messaging, fault tolerance, scalability, and real-world production trade-offs.

---

# Table of Contents

1. Distributed Systems Fundamentals
2. CAP Theorem
3. Consistency Models
4. Distributed Communication
5. Time & Ordering
6. Distributed Transactions
7. Consensus Algorithms
8. Replication
9. Partitioning (Sharding)
10. Leader Election
11. Distributed Locking
12. Fault Tolerance & Reliability
13. Scalability
14. Distributed Caching
15. Messaging Systems
16. Service Coordination
17. Advanced Distributed Patterns
18. Scenario-Based Questions
19. Production Experience
20. Why Questions
21. Trade-offs
22. Common Follow-up Questions

---

# 1. Distributed Systems Fundamentals

## Basic

### Q1.
What is a Distributed System?

**Follow-ups**
- Why were distributed systems introduced?
- What problems do they solve?

---

### Q2.
Characteristics of a distributed system.

---

### Q3.
Distributed system vs centralized system.

---

### Q4.
Advantages of distributed systems.

---

### Q5.
Disadvantages of distributed systems.

---

### Q6.
Challenges in distributed systems.

---

### Q7.
Why are distributed systems inherently complex?

---

### Q8.
What is transparency in distributed systems?

---

### Q9.
Types of transparency in distributed systems.

---

### Q10.
Real-world examples of distributed systems.

---

# 2. CAP Theorem

## Fundamental

### Q11.
What is the CAP Theorem?

---

### Q12.
Consistency in CAP.

---

### Q13.
Availability in CAP.

---

### Q14.
Partition Tolerance.

---

### Q15.
Why can't all three be guaranteed simultaneously?

---

### Q16.
CP systems.

---

### Q17.
AP systems.

---

### Q18.
CA systems.

---

### Q19.
CAP vs PACELC.

---

### Q20.
Real-world database examples.

---

# 3. Consistency Models

## Advanced

### Q21.
Strong Consistency.

---

### Q22.
Eventual Consistency.

---

### Q23.
Weak Consistency.

---

### Q24.
Causal Consistency.

---

### Q25.
Read-Your-Writes Consistency.

---

### Q26.
Monotonic Reads.

---

### Q27.
Monotonic Writes.

---

### Q28.
Session Consistency.

---

### Q29.
Linearizability.

---

### Q30.
Sequential Consistency.

---

### Q31.
When is eventual consistency acceptable?

---

### Q32.
Consistency in distributed databases.

---

### Q33.
Consistency in distributed caches.

---

### Q34.
Consistency in messaging systems.

---

### Q35.
Production trade-offs.

---

# 4. Distributed Communication

### Q36.
Synchronous communication.

---

### Q37.
Asynchronous communication.

---

### Q38.
RPC.

---

### Q39.
REST.

---

### Q40.
gRPC.

---

### Q41.
Message Queues.

---

### Q42.
Publish-Subscribe.

---

### Q43.
Request-Reply.

---

### Q44.
Event-driven communication.

---

### Q45.
Backpressure.

---

### Q46.
Retries.

---

### Q47.
Timeouts.

---

### Q48.
Idempotency.

---

### Q49.
Duplicate messages.

---

### Q50.
Reliable communication.

---

# 5. Time & Ordering

### Q51.
Why is time difficult in distributed systems?

---

### Q52.
Clock synchronization.

---

### Q53.
NTP.

---

### Q54.
Logical Clocks.

---

### Q55.
Lamport Clocks.

---

### Q56.
Vector Clocks.

---

### Q57.
Causality.

---

### Q58.
Happens-before relationship.

---

### Q59.
Global ordering.

---

### Q60.
Event ordering in Kafka.

---

# 6. Distributed Transactions

## Advanced

### Q61.
Distributed Transactions.

---

### Q62.
Why are distributed transactions difficult?

---

### Q63.
Two-Phase Commit (2PC).

---

### Q64.
Three-Phase Commit (3PC).

---

### Q65.
XA Transactions.

---

### Q66.
Saga Pattern.

---

### Q67.
Compensating Transactions.

---

### Q68.
Transactional Outbox.

---

### Q69.
Inbox Pattern.

---

### Q70.
Eventual Consistency.

---

### Q71.
Idempotency.

---

### Q72.
Exactly-once semantics.

---

### Q73.
At-least-once delivery.

---

### Q74.
Failure recovery.

---

### Q75.
Production strategies.

---

# 7. Consensus Algorithms

## Advanced

### Q76.
What is Consensus?

---

### Q77.
Why is consensus needed?

---

### Q78.
Paxos.

---

### Q79.
Raft.

---

### Q80.
Leader election in Raft.

---

### Q81.
Log replication.

---

### Q82.
Quorum.

---

### Q83.
Split brain.

---

### Q84.
Majority voting.

---

### Q85.
Consensus failures.

---

### Q86.
ZooKeeper consensus.

---

### Q87.
etcd.

---

### Q88.
Kubernetes control plane.

---

### Q89.
When should consensus be avoided?

---

### Q90.
Performance implications.

---

# 8. Replication

### Q91.
Replication.

---

### Q92.
Leader-Follower replication.

---

### Q93.
Multi-Leader replication.

---

### Q94.
Leaderless replication.

---

### Q95.
Synchronous replication.

---

### Q96.
Asynchronous replication.

---

### Q97.
Read replicas.

---

### Q98.
Write replication.

---

### Q99.
Replication lag.

---

### Q100.
Conflict resolution.

---

### Q101.
Quorum Reads/Writes.

---

### Q102.
Read Repair.

---

### Q103.
Hinted Handoff.

---

### Q104.
Anti-Entropy.

---

### Q105.
Production best practices.

---

# 9. Partitioning (Sharding)

### Q106.
What is sharding?

---

### Q107.
Horizontal partitioning.

---

### Q108.
Vertical partitioning.

---

### Q109.
Hash-based sharding.

---

### Q110.
Range-based sharding.

---

### Q111.
Directory-based sharding.

---

### Q112.
Shard rebalancing.

---

### Q113.
Hot partitions.

---

### Q114.
Consistent Hashing.

---

### Q115.
Cross-shard joins.

---

### Q116.
Cross-shard transactions.

---

### Q117.
Shard keys.

---

### Q118.
Auto-sharding.

---

### Q119.
Resharding.

---

### Q120.
Production considerations.

---

# 10. Leader Election

### Q121.
Leader Election.

---

### Q122.
Election algorithms.

---

### Q123.
ZooKeeper leader election.

---

### Q124.
Raft leader election.

---

### Q125.
Leader failure.

---

### Q126.
Leader heartbeat.

---

### Q127.
Follower synchronization.

---

### Q128.
Leader failover.

---

### Q129.
Split brain prevention.

---

### Q130.
Production scenarios.

---

# 11. Distributed Locking

### Q131.
Why are distributed locks needed?

---

### Q132.
Redis distributed locking.

---

### Q133.
RedLock algorithm.

---

### Q134.
ZooKeeper locking.

---

### Q135.
Database locking vs Distributed locking.

---

### Q136.
Lease-based locking.

---

### Q137.
Lock expiration.

---

### Q138.
Deadlocks.

---

### Q139.
Lock contention.

---

### Q140.
Best practices.

---

# 12. Fault Tolerance & Reliability

### Q141.
Fault tolerance.

---

### Q142.
Failure detection.

---

### Q143.
Heartbeat.

---

### Q144.
Retry Pattern.

---

### Q145.
Circuit Breaker.

---

### Q146.
Bulkhead.

---

### Q147.
Timeouts.

---

### Q148.
Graceful degradation.

---

### Q149.
Chaos Engineering.

---

### Q150.
Disaster Recovery.

---

# 13. Scalability

### Q151.
Horizontal Scaling.

---

### Q152.
Vertical Scaling.

---

### Q153.
Elasticity.

---

### Q154.
Auto Scaling.

---

### Q155.
Load Balancing.

---

### Q156.
Sticky Sessions.

---

### Q157.
Stateless services.

---

### Q158.
Geo-distribution.

---

### Q159.
Edge Computing.

---

### Q160.
Scalability bottlenecks.

---

# 14. Distributed Caching

### Q161.
Distributed Cache.

---

### Q162.
Cache Aside.

---

### Q163.
Read Through.

---

### Q164.
Write Through.

---

### Q165.
Write Behind.

---

### Q166.
Cache Invalidation.

---

### Q167.
Cache Stampede.

---

### Q168.
Cache Penetration.

---

### Q169.
Cache Avalanche.

---

### Q170.
Cache consistency.

---

# 15. Messaging Systems

### Q171.
Kafka.

---

### Q172.
RabbitMQ.

---

### Q173.
Amazon SQS.

---

### Q174.
Apache Pulsar.

---

### Q175.
Consumer Groups.

---

### Q176.
Message ordering.

---

### Q177.
Dead Letter Queues.

---

### Q178.
Retry Topics.

---

### Q179.
Poison Messages.

---

### Q180.
Event Streaming.

---

# 16. Service Coordination

### Q181.
ZooKeeper.

---

### Q182.
etcd.

---

### Q183.
Consul.

---

### Q184.
Service Registry.

---

### Q185.
Distributed Configuration.

---

### Q186.
Leader Election.

---

### Q187.
Distributed Coordination.

---

### Q188.
Health Checking.

---

### Q189.
Membership management.

---

### Q190.
Failure detection.

---

# 17. Advanced Distributed Patterns

### Q191.
CQRS.

---

### Q192.
Event Sourcing.

---

### Q193.
Outbox Pattern.

---

### Q194.
Inbox Pattern.

---

### Q195.
Saga Pattern.

---

### Q196.
Event-Carried State Transfer.

---

### Q197.
Claim Check Pattern.

---

### Q198.
Scatter-Gather.

---

### Q199.
Competing Consumers.

---

### Q200.
Bulkhead Pattern.

---

# 18. Scenario-Based Questions

### Q201.
How would you design a globally distributed payment system?

---

### Q202.
Your distributed cache returns stale data. How would you investigate?

---

### Q203.
How would you design an order processing system with eventual consistency?

---

### Q204.
A Kafka consumer receives duplicate events. How would you ensure correctness?

---

### Q205.
How would you design a distributed lock for inventory reservation?

---

### Q206.
A leader node crashes unexpectedly. What happens next?

---

### Q207.
Your database shard becomes a hotspot. How would you solve it?

---

### Q208.
A network partition occurs between two data centers. How should your system behave?

---

### Q209.
How would you implement distributed tracing across 50+ microservices?

---

### Q210.
A downstream dependency becomes slow and starts causing cascading failures. How would you protect the system?

---

# 19. Production Experience Questions

### Q211.
Have you worked on distributed systems in production?

---

### Q212.
How have you handled eventual consistency?

---

### Q213.
Have you implemented Saga or Outbox patterns?

---

### Q214.
How do you monitor distributed applications?

---

### Q215.
How do you troubleshoot distributed failures?

---

### Q216.
Have you dealt with partition tolerance issues?

---

### Q217.
How do you ensure idempotency?

---

### Q218.
How do you debug distributed transactions?

---

### Q219.
What distributed systems production incident taught you the most?

---

### Q220.
How do you perform root-cause analysis across multiple services?

---

# 20. "Why" Questions

### Q221.
Why are distributed systems difficult to build?

---

### Q222.
Why is eventual consistency acceptable in many applications?

---

### Q223.
Why can't distributed systems guarantee perfect consistency and availability simultaneously?

---

### Q224.
Why should distributed services be stateless?

---

### Q225.
Why is idempotency critical?

---

### Q226.
Why are retries dangerous without safeguards?

---

### Q227.
Why is clock synchronization unreliable?

---

### Q228.
Why is consensus expensive?

---

### Q229.
Why should synchronous service chains be minimized?

---

### Q230.
Why are distributed caches challenging to maintain?

---

# 21. Trade-off Questions

### Q231.
Strong Consistency vs Eventual Consistency.

---

### Q232.
REST vs Messaging.

---

### Q233.
Kafka vs RabbitMQ.

---

### Q234.
Leader-Follower vs Leaderless Replication.

---

### Q235.
Synchronous vs Asynchronous Replication.

---

### Q236.
2PC vs Saga.

---

### Q237.
Hash-based vs Range-based Sharding.

---

### Q238.
Redis Lock vs ZooKeeper Lock.

---

### Q239.
CP vs AP Systems.

---

### Q240.
Consistency vs Availability.

---

# 22. Common Interview Follow-up Questions

## If you mention CAP Theorem
- PACELC?
- Consistency?
- Availability?
- Partition Tolerance?
- Database examples?

---

## If you mention Replication
- Replication lag?
- Read replicas?
- Conflict resolution?
- Quorum?
- Leader election?

---

## If you mention Messaging
- Ordering?
- Duplicates?
- DLQ?
- Consumer groups?
- Retry?

---

## If you mention Distributed Transactions
- Saga?
- Outbox?
- Inbox?
- Idempotency?
- Compensation?

---

## If you mention Caching
- Stampede?
- Avalanche?
- Consistency?
- Invalidation?
- Redis?

---

## If you mention Scalability
- Load balancing?
- Auto Scaling?
- Sharding?
- Stateless services?
- Bottlenecks?

---

# Staff Engineer Discussion Questions

### Q241.
How would you design a globally distributed system serving hundreds of millions of users?

---

### Q242.
How would you balance consistency, availability, and latency for a financial platform?

---

### Q243.
How would you review a distributed architecture for scalability and resilience?

---

### Q244.
How would you choose between synchronous APIs and event-driven communication?

---

### Q245.
How would you implement organization-wide observability for distributed systems?

---

### Q246.
How would you minimize cascading failures across hundreds of services?

---

### Q247.
How would you evolve a monolithic system into a resilient distributed platform?

---

### Q248.
What metrics would you monitor to identify distributed bottlenecks?

---

### Q249.
How would you educate junior engineers about distributed systems complexity?

---

### Q250.
If you were designing a distributed platform from scratch today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Distributed Systems Basics
- [ ] CAP Theorem
- [ ] PACELC
- [ ] Consistency Models
- [ ] Transparency

## Communication
- [ ] REST
- [ ] gRPC
- [ ] Messaging
- [ ] Event-driven Architecture
- [ ] Idempotency

## Data
- [ ] Replication
- [ ] Sharding
- [ ] Quorum
- [ ] Leader Election
- [ ] Distributed Transactions

## Reliability
- [ ] Saga
- [ ] Outbox
- [ ] Retry
- [ ] Circuit Breaker
- [ ] Fault Tolerance

## Coordination
- [ ] ZooKeeper
- [ ] etcd
- [ ] Distributed Locks
- [ ] Consensus
- [ ] Service Coordination

## Scalability
- [ ] Horizontal Scaling
- [ ] Load Balancing
- [ ] Distributed Cache
- [ ] Auto Scaling
- [ ] Geo-distribution

## Observability
- [ ] Logging
- [ ] Metrics
- [ ] Tracing
- [ ] Correlation IDs
- [ ] Health Checks

## Interview Readiness
- [ ] Can explain CAP, PACELC, and consistency models confidently.
- [ ] Can design resilient distributed systems using Saga, Outbox, and event-driven patterns.
- [ ] Can compare replication, partitioning, and consensus algorithms.
- [ ] Can discuss distributed failures, observability, and fault tolerance.
- [ ] Can solve large-scale distributed system design problems with clear trade-off analysis.

---

**Total Questions:** 250
**Recommended Time:** 8–10 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
**Most Frequently Asked Topics:** CAP Theorem, PACELC, Consistency Models, Replication, Sharding, Consensus (Raft/Paxos), Distributed Transactions, Saga Pattern, Outbox Pattern, Distributed Locking, Kafka, Fault Tolerance, Distributed Caching, Observability, Leader Election