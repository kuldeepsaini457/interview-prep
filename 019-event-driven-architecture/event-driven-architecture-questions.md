# Event-Driven Architecture Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Uber, LinkedIn, Google, Netflix, Adobe, Atlassian, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** Kafka, RabbitMQ, Pulsar, Spring Boot, Spring Kafka, Microservices, Distributed Systems
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Event-Driven Architecture (EDA) is a core architectural style for modern distributed systems. Interviewers expect candidates to understand events, event modeling, asynchronous communication, messaging patterns, reliability, consistency, event versioning, observability, and production-scale event-driven systems.

---

# Table of Contents

1. Event-Driven Architecture Fundamentals
2. Events & Event Modeling
3. Event Producers & Consumers
4. Messaging Patterns
5. Event Brokers
6. Event Ordering & Delivery
7. Event Reliability
8. Event Versioning & Schema Evolution
9. Event Processing
10. Event Sourcing
11. CQRS
12. Saga & Distributed Workflows
13. Outbox & Inbox Patterns
14. Observability
15. Performance & Scaling
16. Advanced Event-Driven Patterns
17. Scenario-Based Questions
18. Production Experience
19. Why Questions
20. Trade-offs
21. Common Follow-up Questions

---

# 1. Event-Driven Architecture Fundamentals

## Basic

### Q1.
What is Event-Driven Architecture (EDA)?

**Follow-ups**
- Why was EDA introduced?
- What problems does it solve?

---

### Q2.
What is an event?

---

### Q3.
Characteristics of Event-Driven Architecture.

---

### Q4.
Synchronous vs Event-Driven Architecture.

---

### Q5.
Advantages of Event-Driven Architecture.

---

### Q6.
Disadvantages of Event-Driven Architecture.

---

### Q7.
When should Event-Driven Architecture be avoided?

---

### Q8.
Real-world examples of Event-Driven systems.

---

### Q9.
Event-driven systems vs request-response systems.

---

### Q10.
Core building blocks of EDA.

---

# 2. Events & Event Modeling

## Intermediate

### Q11.
What makes a good event?

---

### Q12.
Domain Event vs Integration Event.

---

### Q13.
Business Event vs Technical Event.

---

### Q14.
Event payload design.

---

### Q15.
Immutable events.

---

### Q16.
Event naming conventions.

---

### Q17.
Event metadata.

---

### Q18.
Event timestamps.

---

### Q19.
Correlation IDs.

---

### Q20.
Causation IDs.

---

### Q21.
Event granularity.

---

### Q22.
Event ownership.

---

### Q23.
Fat events vs Thin events.

---

### Q24.
Event lifecycle.

---

### Q25.
Event modeling best practices.

---

# 3. Event Producers & Consumers

### Q26.
Producer responsibilities.

---

### Q27.
Consumer responsibilities.

---

### Q28.
Producer acknowledgments.

---

### Q29.
Producer retries.

---

### Q30.
Consumer retries.

---

### Q31.
Idempotent consumers.

---

### Q32.
Consumer scaling.

---

### Q33.
Consumer failures.

---

### Q34.
Poison messages.

---

### Q35.
Dead Letter Queues (DLQ).

---

# 4. Messaging Patterns

### Q36.
Publish-Subscribe.

---

### Q37.
Point-to-Point messaging.

---

### Q38.
Competing Consumers.

---

### Q39.
Request-Reply over messaging.

---

### Q40.
Event Notification pattern.

---

### Q41.
Event-Carried State Transfer.

---

### Q42.
Command Message pattern.

---

### Q43.
Event Collaboration.

---

### Q44.
Claim Check pattern.

---

### Q45.
Aggregator pattern.

---

### Q46.
Scatter-Gather pattern.

---

### Q47.
Routing Slip.

---

### Q48.
Message Filter.

---

### Q49.
Content-Based Routing.

---

### Q50.
Messaging best practices.

---

# 5. Event Brokers

### Q51.
What is an Event Broker?

---

### Q52.
Kafka.

---

### Q53.
RabbitMQ.

---

### Q54.
Apache Pulsar.

---

### Q55.
Amazon EventBridge.

---

### Q56.
Google Pub/Sub.

---

### Q57.
Azure Event Hubs.

---

### Q58.
Broker responsibilities.

---

### Q59.
Broker selection.

---

### Q60.
Broker scaling.

---

# 6. Event Ordering & Delivery

### Q61.
Message ordering.

---

### Q62.
Ordering guarantees.

---

### Q63.
Partition-based ordering.

---

### Q64.
Global ordering.

---

### Q65.
At-most-once delivery.

---

### Q66.
At-least-once delivery.

---

### Q67.
Exactly-once delivery.

---

### Q68.
Duplicate event handling.

---

### Q69.
Idempotency.

---

### Q70.
Delivery guarantees trade-offs.

---

# 7. Event Reliability

### Q71.
Reliable event publishing.

---

### Q72.
Reliable event consumption.

---

### Q73.
Retry strategies.

---

### Q74.
Exponential backoff.

---

### Q75.
Jitter.

---

### Q76.
Dead Letter Queue.

---

### Q77.
Retry topics.

---

### Q78.
Poison message handling.

---

### Q79.
Message expiration.

---

### Q80.
Failure recovery.

---

# 8. Event Versioning & Schema Evolution

### Q81.
Why is event versioning important?

---

### Q82.
Schema Registry.

---

### Q83.
Avro.

---

### Q84.
Protobuf.

---

### Q85.
JSON Schema.

---

### Q86.
Backward compatibility.

---

### Q87.
Forward compatibility.

---

### Q88.
Full compatibility.

---

### Q89.
Versioned event contracts.

---

### Q90.
Migrating event schemas.

---

# 9. Event Processing

### Q91.
Stream processing.

---

### Q92.
Batch processing.

---

### Q93.
Real-time processing.

---

### Q94.
Windowing.

---

### Q95.
Sliding windows.

---

### Q96.
Tumbling windows.

---

### Q97.
Session windows.

---

### Q98.
Event-time vs Processing-time.

---

### Q99.
Late arriving events.

---

### Q100.
Watermarks.

---

# 10. Event Sourcing

## Advanced

### Q101.
What is Event Sourcing?

---

### Q102.
Event Store.

---

### Q103.
Rebuilding state.

---

### Q104.
Snapshots.

---

### Q105.
Advantages of Event Sourcing.

---

### Q106.
Disadvantages.

---

### Q107.
When should Event Sourcing be used?

---

### Q108.
Event replay.

---

### Q109.
Version migration.

---

### Q110.
Production considerations.

---

# 11. CQRS

### Q111.
What is CQRS?

---

### Q112.
Read Model.

---

### Q113.
Write Model.

---

### Q114.
CQRS with Event Sourcing.

---

### Q115.
Read model synchronization.

---

### Q116.
Materialized Views.

---

### Q117.
Projection services.

---

### Q118.
Eventually consistent reads.

---

### Q119.
CQRS pitfalls.

---

### Q120.
Production recommendations.

---

# 12. Saga & Distributed Workflows

### Q121.
Saga Pattern.

---

### Q122.
Orchestration Saga.

---

### Q123.
Choreography Saga.

---

### Q124.
Compensating Transactions.

---

### Q125.
Workflow engines.

---

### Q126.
Temporal.

---

### Q127.
Camunda.

---

### Q128.
Conductor.

---

### Q129.
Long-running transactions.

---

### Q130.
Failure recovery.

---

# 13. Outbox & Inbox Patterns

### Q131.
Transactional Outbox.

---

### Q132.
Inbox Pattern.

---

### Q133.
Reliable event publishing.

---

### Q134.
Reliable event consumption.

---

### Q135.
Duplicate prevention.

---

### Q136.
Event deduplication.

---

### Q137.
Polling publisher.

---

### Q138.
CDC (Change Data Capture).

---

### Q139.
Debezium.

---

### Q140.
Production best practices.

---

# 14. Observability

### Q141.
Distributed tracing.

---

### Q142.
Correlation IDs.

---

### Q143.
Causation IDs.

---

### Q144.
Message tracing.

---

### Q145.
Centralized logging.

---

### Q146.
Metrics.

---

### Q147.
Event latency monitoring.

---

### Q148.
Consumer lag.

---

### Q149.
Dead Letter Queue monitoring.

---

### Q150.
Production dashboards.

---

# 15. Performance & Scaling

### Q151.
Horizontal scaling.

---

### Q152.
Consumer groups.

---

### Q153.
Partitioning.

---

### Q154.
Batch consumption.

---

### Q155.
Parallel consumers.

---

### Q156.
Throughput optimization.

---

### Q157.
Latency optimization.

---

### Q158.
Backpressure.

---

### Q159.
Load balancing.

---

### Q160.
Capacity planning.

---

# 16. Advanced Event-Driven Patterns

### Q161.
Event Collaboration.

---

### Q162.
Event Mesh.

---

### Q163.
Event Gateway.

---

### Q164.
Event Broker Federation.

---

### Q165.
Fan-out pattern.

---

### Q166.
Fan-in pattern.

---

### Q167.
Competing Consumers.

---

### Q168.
Event Aggregation.

---

### Q169.
Choreography vs Orchestration.

---

### Q170.
Hybrid architectures.

---

### Q171.
Request-Reply fallback.

---

### Q172.
Command Query Responsibility Separation with events.

---

### Q173.
Event-driven cache invalidation.

---

### Q174.
Real-time analytics pipelines.

---

### Q175.
Digital Twin architectures.

---

# 17. Scenario-Based Questions

### Q176.
How would you design an event-driven order processing system?

---

### Q177.
An event is published successfully but the consumer processes it twice. How would you ensure correctness?

---

### Q178.
A consumer crashes after updating the database but before committing the offset. What happens?

---

### Q179.
How would you guarantee reliable event publishing from a Spring Boot application?

---

### Q180.
A producer publishes events faster than consumers can process them. How would you scale the system?

---

### Q181.
A new event schema breaks existing consumers. How would you handle schema evolution?

---

### Q182.
A payment workflow spans five microservices. Would you choose choreography or orchestration? Why?

---

### Q183.
How would you replay historical events to rebuild a read model?

---

### Q184.
Your Dead Letter Queue grows continuously. How would you investigate the root cause?

---

### Q185.
An event-driven architecture becomes difficult to debug due to asynchronous workflows. How would you improve observability?

---

### Q186.
How would you design a notification system using event-driven architecture?

---

### Q187.
How would you implement exactly-once business processing without relying solely on broker guarantees?

---

### Q188.
How would you migrate a synchronous microservice ecosystem to event-driven communication?

---

### Q189.
How would you prevent event storms caused by cascading events?

---

### Q190.
How would you evolve an event contract consumed by dozens of downstream services?

---

# 18. Production Experience Questions

### Q191.
Have you designed event-driven systems in production?

---

### Q192.
How do you choose between REST and events?

---

### Q193.
How have you implemented Saga workflows?

---

### Q194.
How do you ensure idempotent event processing?

---

### Q195.
How do you monitor consumer lag and event latency?

---

### Q196.
Have you implemented the Outbox Pattern?

---

### Q197.
How do you handle schema evolution?

---

### Q198.
How do you debug distributed event flows?

---

### Q199.
How do you review event contracts during code reviews?

---

### Q200.
What event-driven production incident taught you the most?

---

# 19. "Why" Questions

### Q201.
Why are events immutable?

---

### Q202.
Why should business events be named in the past tense?

---

### Q203.
Why is idempotency critical in event-driven systems?

---

### Q204.
Why should producers avoid knowing their consumers?

---

### Q205.
Why is eventual consistency acceptable in event-driven architectures?

---

### Q206.
Why is choreography sometimes harder to maintain than orchestration?

---

### Q207.
Why is schema evolution challenging?

---

### Q208.
Why are correlation IDs essential?

---

### Q209.
Why should event payloads avoid unnecessary data?

---

### Q210.
Why are retries dangerous without proper safeguards?

---

# 20. Trade-off Questions

### Q211.
REST vs Event-Driven Architecture.

---

### Q212.
Kafka vs RabbitMQ.

---

### Q213.
Choreography vs Orchestration.

---

### Q214.
Event Notification vs Event-Carried State Transfer.

---

### Q215.
Outbox Pattern vs Direct Publishing.

---

### Q216.
Polling Publisher vs CDC (Debezium).

---

### Q217.
CQRS vs Traditional CRUD.

---

### Q218.
Event Sourcing vs State Storage.

---

### Q219.
At-least-once vs Exactly-once Processing.

---

### Q220.
Real-time Processing vs Batch Processing.

---

# 21. Common Interview Follow-up Questions

## If you mention Events
- Domain Event?
- Integration Event?
- Event schema?
- Metadata?
- Versioning?

---

## If you mention Messaging
- Ordering?
- Retries?
- DLQ?
- Idempotency?
- Delivery guarantees?

---

## If you mention Event Sourcing
- Snapshots?
- Replay?
- CQRS?
- Event Store?
- Schema migration?

---

## If you mention Saga
- Orchestration?
- Choreography?
- Compensation?
- Failure handling?
- Outbox?

---

## If you mention Observability
- Correlation IDs?
- Distributed tracing?
- Metrics?
- Consumer lag?
- Logging?

---

## If you mention Performance
- Scaling?
- Backpressure?
- Partitioning?
- Consumer groups?
- Throughput optimization?

---

# Staff Engineer Discussion Questions

### Q221.
How would you design an event-driven platform processing billions of events per day?

---

### Q222.
How would you establish event governance across hundreds of microservices?

---

### Q223.
How would you standardize event schemas across engineering teams?

---

### Q224.
How would you balance eventual consistency with business requirements?

---

### Q225.
How would you review an event-driven architecture for reliability and scalability?

---

### Q226.
How would you migrate a monolithic system to event-driven architecture incrementally?

---

### Q227.
How would you implement organization-wide observability for asynchronous workflows?

---

### Q228.
How would you prevent event coupling and schema drift over time?

---

### Q229.
What metrics would you continuously monitor in an event-driven platform?

---

### Q230.
If you were designing a new enterprise event platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Event-Driven Architecture
- [ ] Events
- [ ] Producers
- [ ] Consumers
- [ ] Event Brokers

## Messaging
- [ ] Publish-Subscribe
- [ ] Competing Consumers
- [ ] Request-Reply
- [ ] Delivery Guarantees
- [ ] Dead Letter Queues

## Reliability
- [ ] Idempotency
- [ ] Retries
- [ ] Outbox Pattern
- [ ] Inbox Pattern
- [ ] Failure Recovery

## Event Modeling
- [ ] Domain Events
- [ ] Integration Events
- [ ] Event Contracts
- [ ] Schema Evolution
- [ ] Correlation IDs

## Advanced Patterns
- [ ] CQRS
- [ ] Event Sourcing
- [ ] Saga
- [ ] Choreography
- [ ] Orchestration

## Performance
- [ ] Consumer Groups
- [ ] Partitioning
- [ ] Throughput Optimization
- [ ] Backpressure
- [ ] Capacity Planning

## Observability
- [ ] Distributed Tracing
- [ ] Event Latency
- [ ] Metrics
- [ ] Logging
- [ ] Monitoring

## Interview Readiness
- [ ] Can explain the complete lifecycle of an event from producer to consumer.
- [ ] Can compare synchronous and event-driven architectures with real-world trade-offs.
- [ ] Can design reliable event-driven systems using Outbox, Saga, and CQRS.
- [ ] Can discuss schema evolution, idempotency, and event observability.
- [ ] Can design scalable enterprise event-driven platforms with confidence.

---

**Total Questions:** 230
**Recommended Time:** 6–7 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
**Most Frequently Asked Topics:** Event Modeling, Kafka-based Event-Driven Architecture, Domain Events, Integration Events, Saga Pattern, Outbox Pattern, Event Sourcing, CQRS, Schema Evolution, Idempotency, Delivery Guarantees, Event Observability, Choreography vs Orchestration