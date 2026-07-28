# Saga Pattern Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Uber, Netflix, LinkedIn, Google, Adobe, Atlassian, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** Microservices, Kafka, RabbitMQ, Spring Boot, Event-Driven Architecture, Distributed Systems
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> The Saga Pattern is one of the most frequently asked distributed systems topics because it is the de facto approach for maintaining consistency across microservices without using distributed transactions (2PC/XA). Interviewers expect candidates to understand orchestration, choreography, compensating transactions, failure handling, idempotency, retries, observability, and production trade-offs.

---

# Table of Contents

1. Saga Fundamentals
2. Distributed Transactions
3. Compensating Transactions
4. Choreography Saga
5. Orchestration Saga
6. Saga State Management
7. Failure Handling
8. Idempotency & Reliability
9. Messaging Integration
10. Saga with Kafka
11. Saga with Workflow Engines
12. Outbox Integration
13. Observability
14. Performance & Scaling
15. Advanced Saga Concepts
16. Scenario-Based Questions
17. Production Experience
18. Why Questions
19. Trade-offs
20. Common Follow-up Questions

---

# 1. Saga Fundamentals

## Basic

### Q1.
What is the Saga Pattern?

**Follow-ups**
- Why was Saga introduced?
- What problems does it solve?

---

### Q2.
What is a distributed transaction?

---

### Q3.
Why can't ACID transactions span multiple microservices?

---

### Q4.
How does Saga maintain data consistency?

---

### Q5.
When should Saga be used?

---

### Q6.
When should Saga NOT be used?

---

### Q7.
Characteristics of a Saga.

---

### Q8.
Real-world examples of Saga.

---

### Q9.
Long-running transactions.

---

### Q10.
Business transactions vs Database transactions.

---

# 2. Distributed Transactions

### Q11.
Distributed transaction challenges.

---

### Q12.
XA Transactions.

---

### Q13.
Two-Phase Commit (2PC).

---

### Q14.
Three-Phase Commit (3PC).

---

### Q15.
Why is 2PC rarely used in microservices?

---

### Q16.
Blocking behavior in 2PC.

---

### Q17.
Coordinator failures.

---

### Q18.
Network partitions.

---

### Q19.
Distributed consistency.

---

### Q20.
Saga vs Distributed Transactions.

---

# 3. Compensating Transactions

## Intermediate

### Q21.
What is a compensating transaction?

---

### Q22.
Why are compensating transactions necessary?

---

### Q23.
Forward recovery vs Compensation.

---

### Q24.
Compensation ordering.

---

### Q25.
Compensation failures.

---

### Q26.
Idempotent compensation.

---

### Q27.
Compensation retries.

---

### Q28.
Compensation timeout.

---

### Q29.
Designing compensation logic.

---

### Q30.
Compensation best practices.

---

# 4. Choreography Saga

### Q31.
What is Choreography Saga?

---

### Q32.
Event-driven choreography.

---

### Q33.
How do services communicate?

---

### Q34.
Advantages.

---

### Q35.
Disadvantages.

---

### Q36.
Service coupling.

---

### Q37.
Event storms.

---

### Q38.
Debugging choreography.

---

### Q39.
Scaling choreography.

---

### Q40.
Production recommendations.

---

# 5. Orchestration Saga

### Q41.
What is Orchestration Saga?

---

### Q42.
Saga Orchestrator.

---

### Q43.
Workflow coordination.

---

### Q44.
Command-based communication.

---

### Q45.
Advantages.

---

### Q46.
Disadvantages.

---

### Q47.
Orchestrator failures.

---

### Q48.
Orchestrator scalability.

---

### Q49.
Workflow persistence.

---

### Q50.
Production recommendations.

---

# 6. Saga State Management

### Q51.
Saga state.

---

### Q52.
State persistence.

---

### Q53.
State transitions.

---

### Q54.
Workflow history.

---

### Q55.
Checkpointing.

---

### Q56.
Saga recovery.

---

### Q57.
Resuming failed workflows.

---

### Q58.
Timeout handling.

---

### Q59.
State storage.

---

### Q60.
Saga lifecycle.

---

# 7. Failure Handling

## Advanced

### Q61.
Service failure.

---

### Q62.
Network failure.

---

### Q63.
Broker failure.

---

### Q64.
Duplicate messages.

---

### Q65.
Partial completion.

---

### Q66.
Retry strategies.

---

### Q67.
Exponential backoff.

---

### Q68.
Poison messages.

---

### Q69.
Dead Letter Queue.

---

### Q70.
Failure recovery strategies.

---

# 8. Idempotency & Reliability

### Q71.
Why is idempotency critical?

---

### Q72.
Idempotent commands.

---

### Q73.
Idempotent events.

---

### Q74.
Duplicate detection.

---

### Q75.
Business keys.

---

### Q76.
Deduplication tables.

---

### Q77.
Retry-safe operations.

---

### Q78.
Reliable message processing.

---

### Q79.
Exactly-once business processing.

---

### Q80.
Reliability best practices.

---

# 9. Messaging Integration

### Q81.
Kafka with Saga.

---

### Q82.
RabbitMQ with Saga.

---

### Q83.
Command messages.

---

### Q84.
Domain events.

---

### Q85.
Integration events.

---

### Q86.
Event ordering.

---

### Q87.
Correlation IDs.

---

### Q88.
Causation IDs.

---

### Q89.
Message versioning.

---

### Q90.
Broker considerations.

---

# 10. Saga with Kafka

### Q91.
Kafka choreography.

---

### Q92.
Kafka orchestration.

---

### Q93.
Kafka transactions.

---

### Q94.
Outbox Pattern.

---

### Q95.
Inbox Pattern.

---

### Q96.
Consumer groups.

---

### Q97.
Retry topics.

---

### Q98.
Dead Letter Topics.

---

### Q99.
Event replay.

---

### Q100.
Kafka best practices.

---

# 11. Saga with Workflow Engines

### Q101.
Workflow engine.

---

### Q102.
Temporal.

---

### Q103.
Camunda.

---

### Q104.
Netflix Conductor.

---

### Q105.
AWS Step Functions.

---

### Q106.
Workflow persistence.

---

### Q107.
Retries in workflow engines.

---

### Q108.
Timeout management.

---

### Q109.
Human approval workflows.

---

### Q110.
Workflow versioning.

---

# 12. Outbox Integration

### Q111.
Transactional Outbox.

---

### Q112.
Polling Publisher.

---

### Q113.
CDC (Change Data Capture).

---

### Q114.
Debezium.

---

### Q115.
Reliable publishing.

---

### Q116.
Inbox Pattern.

---

### Q117.
Duplicate prevention.

---

### Q118.
Event consistency.

---

### Q119.
Failure recovery.

---

### Q120.
Production best practices.

---

# 13. Observability

### Q121.
Distributed tracing.

---

### Q122.
Correlation IDs.

---

### Q123.
Saga IDs.

---

### Q124.
Workflow monitoring.

---

### Q125.
Metrics.

---

### Q126.
Logging.

---

### Q127.
Tracing across services.

---

### Q128.
Alerting.

---

### Q129.
Stuck Saga detection.

---

### Q130.
Production dashboards.

---

# 14. Performance & Scaling

### Q131.
Scaling Saga workflows.

---

### Q132.
Workflow partitioning.

---

### Q133.
Parallel Saga execution.

---

### Q134.
Compensation performance.

---

### Q135.
Broker throughput.

---

### Q136.
Consumer scaling.

---

### Q137.
Workflow bottlenecks.

---

### Q138.
Timeout tuning.

---

### Q139.
Capacity planning.

---

### Q140.
Performance optimization.

---

# 15. Advanced Saga Concepts

### Q141.
Nested Sagas.

---

### Q142.
Hierarchical Sagas.

---

### Q143.
Parallel compensation.

---

### Q144.
Conditional compensation.

---

### Q145.
Multi-region Sagas.

---

### Q146.
Cross-domain workflows.

---

### Q147.
Saga versioning.

---

### Q148.
Workflow migration.

---

### Q149.
Saga anti-patterns.

---

### Q150.
Enterprise Saga governance.

---

# 16. Scenario-Based Questions

### Q151.
How would you design an order placement Saga involving Inventory, Payment, and Shipping services?

---

### Q152.
A payment succeeds but inventory reservation fails. How would your Saga recover?

---

### Q153.
A compensation transaction itself fails. What should happen next?

---

### Q154.
A network failure occurs after a service completes its work but before the response reaches the orchestrator. How would you prevent inconsistent state?

---

### Q155.
An event is processed twice by a downstream service. How would you ensure business correctness?

---

### Q156.
How would you design a travel booking Saga involving flight, hotel, and car reservations?

---

### Q157.
A choreography-based Saga becomes difficult to debug as more services are added. How would you improve the architecture?

---

### Q158.
A workflow spans dozens of services and includes manual approval steps. Would you build your own orchestrator or use a workflow engine?

---

### Q159.
Your Outbox table grows to billions of records. How would you manage retention and cleanup?

---

### Q160.
A Saga remains stuck in an intermediate state for several hours. How would you investigate and recover it?

---

### Q161.
How would you migrate from synchronous REST-based workflows to Saga-based orchestration?

---

### Q162.
How would you support replaying failed Saga executions safely?

---

### Q163.
How would you prevent duplicate compensations?

---

### Q164.
How would you coordinate inventory reservation across multiple warehouses?

---

### Q165.
How would you design a payment refund workflow using Saga?

---

# 17. Production Experience Questions

### Q166.
Have you implemented the Saga Pattern in production?

---

### Q167.
How did you choose between choreography and orchestration?

---

### Q168.
How do you implement compensating transactions?

---

### Q169.
How do you monitor Saga execution?

---

### Q170.
How do you recover failed workflows?

---

### Q171.
How do you ensure reliable event publishing?

---

### Q172.
Have you integrated the Outbox Pattern?

---

### Q173.
How do you prevent duplicate processing?

---

### Q174.
How do you review Saga implementations during code reviews?

---

### Q175.
What Saga-related production incident taught you the most?

---

# 18. "Why" Questions

### Q176.
Why is Saga preferred over XA transactions in microservices?

---

### Q177.
Why are compensating transactions usually business-specific?

---

### Q178.
Why should Saga steps be idempotent?

---

### Q179.
Why is eventual consistency acceptable?

---

### Q180.
Why should workflows be persisted?

---

### Q181.
Why are retries dangerous without idempotency?

---

### Q182.
Why can choreography become difficult at scale?

---

### Q183.
Why are workflow engines becoming popular?

---

### Q184.
Why should compensation logic avoid side effects?

---

### Q185.
Why should every Saga have observability built in?

---

# 19. Trade-off Questions

### Q186.
Saga vs Two-Phase Commit (2PC).

---

### Q187.
Choreography vs Orchestration.

---

### Q188.
Custom Orchestrator vs Temporal.

---

### Q189.
Outbox Pattern vs Direct Event Publishing.

---

### Q190.
Polling Publisher vs Debezium CDC.

---

### Q191.
Kafka vs RabbitMQ for Saga workflows.

---

### Q192.
REST Coordination vs Event-Driven Coordination.

---

### Q193.
Business Compensation vs Database Rollback.

---

### Q194.
Eventually Consistent vs Strongly Consistent Systems.

---

### Q195.
Workflow Engine vs Plain Microservice Coordination.

---

# 20. Common Interview Follow-up Questions

## If you mention Saga
- Why Saga?
- ACID?
- Eventual consistency?
- Compensation?
- Workflow?

---

## If you mention Choreography
- Event storm?
- Coupling?
- Debugging?
- Scaling?
- Observability?

---

## If you mention Orchestration
- Orchestrator?
- Single point of failure?
- State persistence?
- Workflow engine?
- Recovery?

---

## If you mention Outbox
- CDC?
- Debezium?
- Inbox?
- Duplicate handling?
- Reliable publishing?

---

## If you mention Reliability
- Idempotency?
- Retries?
- DLQ?
- Compensation failures?
- Timeout handling?

---

## If you mention Workflow Engines
- Temporal?
- Camunda?
- Step Functions?
- Netflix Conductor?
- Human tasks?

---

# Staff Engineer Discussion Questions

### Q196.
How would you standardize Saga implementations across hundreds of microservices?

---

### Q197.
How would you design a globally distributed payment platform using Saga?

---

### Q198.
How would you establish governance for business workflows across engineering teams?

---

### Q199.
How would you review Saga implementations for reliability and scalability?

---

### Q200.
How would you migrate a monolith using database transactions to Saga-based workflows?

---

### Q201.
How would you ensure organization-wide observability for long-running business processes?

---

### Q202.
How would you prevent workflow coupling as the number of services grows?

---

### Q203.
How would you decide when to introduce a workflow engine instead of custom orchestration?

---

### Q204.
Which metrics would you continuously monitor for Saga health?

---

### Q205.
If you were designing a workflow orchestration platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Saga Pattern
- [ ] Distributed Transactions
- [ ] Eventual Consistency
- [ ] Business Transactions
- [ ] Compensation

## Saga Styles
- [ ] Choreography
- [ ] Orchestration
- [ ] Workflow Coordination
- [ ] State Management
- [ ] Recovery

## Reliability
- [ ] Idempotency
- [ ] Retries
- [ ] Duplicate Handling
- [ ] DLQ
- [ ] Timeout Management

## Messaging
- [ ] Kafka
- [ ] RabbitMQ
- [ ] Correlation IDs
- [ ] Event Ordering
- [ ] Integration Events

## Patterns
- [ ] Outbox Pattern
- [ ] Inbox Pattern
- [ ] CDC
- [ ] Debezium
- [ ] Reliable Publishing

## Workflow Engines
- [ ] Temporal
- [ ] Camunda
- [ ] Conductor
- [ ] AWS Step Functions
- [ ] Workflow Versioning

## Observability
- [ ] Saga IDs
- [ ] Distributed Tracing
- [ ] Metrics
- [ ] Logging
- [ ] Stuck Workflow Detection

## Interview Readiness
- [ ] Can explain Saga from first principles.
- [ ] Can compare Saga with XA/2PC confidently.
- [ ] Can design choreography and orchestration workflows.
- [ ] Can implement reliable workflows using Outbox and idempotency.
- [ ] Can discuss production-scale Saga architecture, monitoring, and recovery.

---

**Total Questions:** 205
**Recommended Time:** 5–6 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
**Most Frequently Asked Topics:** Saga Fundamentals, Choreography vs Orchestration, Compensating Transactions, Outbox Pattern, Idempotency, Workflow Engines (Temporal/Camunda), Failure Recovery, Eventual Consistency, Distributed Transactions, Observability