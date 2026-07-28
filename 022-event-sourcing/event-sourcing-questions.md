# Event Sourcing Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Google, Uber, LinkedIn, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** Java, Spring Boot, Kafka, Event-Driven Architecture, CQRS, Distributed Systems, DDD
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Event Sourcing is one of the most advanced architectural patterns used in distributed systems. Interviewers expect candidates to understand event stores, immutable events, aggregate reconstruction, snapshots, event replay, CQRS integration, schema evolution, scalability, and production trade-offs.

---

# Table of Contents

1. Event Sourcing Fundamentals
2. Events & Event Store
3. Aggregate Reconstruction
4. Snapshots
5. Event Replay
6. Event Versioning & Schema Evolution
7. CQRS Integration
8. Event Sourcing with DDD
9. Event Sourcing with Kafka
10. Consistency & Reliability
11. Performance & Scalability
12. Observability
13. Advanced Event Sourcing Concepts
14. Scenario-Based Questions
15. Production Experience
16. Why Questions
17. Trade-offs
18. Common Follow-up Questions

---

# 1. Event Sourcing Fundamentals

## Basic

### Q1.
What is Event Sourcing?

**Follow-ups**
- Why was Event Sourcing introduced?
- What problems does it solve?

---

### Q2.
How is Event Sourcing different from CRUD?

---

### Q3.
How does Event Sourcing work?

---

### Q4.
What is an Event Store?

---

### Q5.
Current State vs Event History.

---

### Q6.
Characteristics of Event Sourcing.

---

### Q7.
Benefits of Event Sourcing.

---

### Q8.
Disadvantages of Event Sourcing.

---

### Q9.
When should Event Sourcing be used?

---

### Q10.
When should Event Sourcing NOT be used?

---

# 2. Events & Event Store

## Intermediate

### Q11.
What is an Event?

---

### Q12.
Immutable Events.

---

### Q13.
Business Events vs Technical Events.

---

### Q14.
Event metadata.

---

### Q15.
Event identifiers.

---

### Q16.
Event ordering.

---

### Q17.
Event timestamps.

---

### Q18.
Append-only log.

---

### Q19.
Event Store responsibilities.

---

### Q20.
Choosing an Event Store.

---

### Q21.
Database as Event Store.

---

### Q22.
Kafka as Event Store.

---

### Q23.
EventStoreDB.

---

### Q24.
Event persistence.

---

### Q25.
Event retention strategies.

---

# 3. Aggregate Reconstruction

## Advanced

### Q26.
How is an Aggregate reconstructed?

---

### Q27.
Aggregate Root.

---

### Q28.
Applying events.

---

### Q29.
Loading aggregate history.

---

### Q30.
Rebuilding current state.

---

### Q31.
Optimistic concurrency.

---

### Q32.
Aggregate versioning.

---

### Q33.
Concurrency conflicts.

---

### Q34.
Aggregate lifecycle.

---

### Q35.
Production considerations.

---

# 4. Snapshots

### Q36.
What are snapshots?

---

### Q37.
Why are snapshots needed?

---

### Q38.
Snapshot frequency.

---

### Q39.
Snapshot storage.

---

### Q40.
Snapshot consistency.

---

### Q41.
Snapshot recovery.

---

### Q42.
Snapshot invalidation.

---

### Q43.
Incremental snapshots.

---

### Q44.
Snapshot optimization.

---

### Q45.
Snapshot best practices.

---

# 5. Event Replay

### Q46.
What is event replay?

---

### Q47.
Why replay events?

---

### Q48.
Rebuilding projections.

---

### Q49.
Reprocessing business logic.

---

### Q50.
Replay performance.

---

### Q51.
Replay safety.

---

### Q52.
Replay ordering.

---

### Q53.
Replay failures.

---

### Q54.
Replay tooling.

---

### Q55.
Production replay strategies.

---

# 6. Event Versioning & Schema Evolution

### Q56.
Why is event versioning required?

---

### Q57.
Backward compatibility.

---

### Q58.
Forward compatibility.

---

### Q59.
Event schema evolution.

---

### Q60.
Version migration.

---

### Q61.
Event upcasting.

---

### Q62.
Schema Registry.

---

### Q63.
Avro.

---

### Q64.
Protobuf.

---

### Q65.
Production recommendations.

---

# 7. CQRS Integration

### Q66.
How does Event Sourcing work with CQRS?

---

### Q67.
Write Model.

---

### Q68.
Read Model.

---

### Q69.
Projection.

---

### Q70.
Materialized Views.

---

### Q71.
Projection rebuilding.

---

### Q72.
Eventually consistent reads.

---

### Q73.
Projection failures.

---

### Q74.
Read model synchronization.

---

### Q75.
CQRS trade-offs.

---

# 8. Event Sourcing with DDD

### Q76.
Aggregates in Event Sourcing.

---

### Q77.
Aggregate invariants.

---

### Q78.
Domain Events.

---

### Q79.
Value Objects.

---

### Q80.
Repositories.

---

### Q81.
Domain Services.

---

### Q82.
Event publication.

---

### Q83.
Business workflows.

---

### Q84.
Bounded Contexts.

---

### Q85.
DDD best practices.

---

# 9. Event Sourcing with Kafka

### Q86.
Kafka as an Event Store.

---

### Q87.
Kafka log compaction.

---

### Q88.
Partition ordering.

---

### Q89.
Replay using Kafka.

---

### Q90.
Consumer groups.

---

### Q91.
Offsets.

---

### Q92.
Retention.

---

### Q93.
Event streaming.

---

### Q94.
Outbox integration.

---

### Q95.
Kafka limitations.

---

# 10. Consistency & Reliability

### Q96.
Eventual consistency.

---

### Q97.
Optimistic locking.

---

### Q98.
Duplicate events.

---

### Q99.
Idempotency.

---

### Q100.
Reliable publishing.

---

### Q101.
Outbox Pattern.

---

### Q102.
Inbox Pattern.

---

### Q103.
Exactly-once business processing.

---

### Q104.
Failure recovery.

---

### Q105.
Consistency trade-offs.

---

# 11. Performance & Scalability

### Q106.
Scaling Event Stores.

---

### Q107.
Aggregate hotspots.

---

### Q108.
Partitioning.

---

### Q109.
Snapshots.

---

### Q110.
Projection scaling.

---

### Q111.
Parallel replay.

---

### Q112.
Storage optimization.

---

### Q113.
Compression.

---

### Q114.
Archiving old events.

---

### Q115.
Capacity planning.

---

# 12. Observability

### Q116.
Correlation IDs.

---

### Q117.
Causation IDs.

---

### Q118.
Distributed tracing.

---

### Q119.
Projection monitoring.

---

### Q120.
Replay monitoring.

---

### Q121.
Metrics.

---

### Q122.
Logging.

---

### Q123.
Dead Letter Queue monitoring.

---

### Q124.
Audit trails.

---

### Q125.
Production dashboards.

---

# 13. Advanced Event Sourcing Concepts

### Q126.
Temporal queries.

---

### Q127.
Time travel.

---

### Q128.
Audit history.

---

### Q129.
Multi-stream events.

---

### Q130.
Cross-aggregate workflows.

---

### Q131.
Long-running business processes.

---

### Q132.
Multi-region event stores.

---

### Q133.
Cross-region replication.

---

### Q134.
Event Store migration.

---

### Q135.
Event Sourcing anti-patterns.

---

# 14. Scenario-Based Questions

### Q136.
How would you design an Event Sourcing-based order management system?

---

### Q137.
An aggregate contains millions of events. How would you optimize reconstruction?

---

### Q138.
A bug in projection logic requires rebuilding every read model. How would you perform the replay?

---

### Q139.
How would you migrate a CRUD application to Event Sourcing?

---

### Q140.
A new event schema breaks replay of historical events. How would you solve it?

---

### Q141.
How would you implement audit history for a banking application?

---

### Q142.
A replay takes several days due to billions of events. How would you optimize it?

---

### Q143.
How would you design snapshots for a high-volume payment service?

---

### Q144.
An event is published twice. How would you ensure correctness?

---

### Q145.
How would you rebuild projections after a production outage?

---

### Q146.
How would you support rollback without deleting events?

---

### Q147.
How would you model inventory adjustments using Event Sourcing?

---

### Q148.
How would you integrate Event Sourcing with Saga workflows?

---

### Q149.
How would you migrate event schemas consumed by hundreds of services?

---

### Q150.
How would you review an Event Sourcing architecture for scalability?

---

# 15. Production Experience Questions

### Q151.
Have you used Event Sourcing in production?

---

### Q152.
How do you manage event versioning?

---

### Q153.
How do you rebuild projections safely?

---

### Q154.
How do you optimize aggregate loading?

---

### Q155.
Have you implemented snapshots?

---

### Q156.
How do you monitor replay performance?

---

### Q157.
How do you debug projection inconsistencies?

---

### Q158.
How do you integrate Event Sourcing with Kafka?

---

### Q159.
How do you evolve Event Sourcing architectures over time?

---

### Q160.
What Event Sourcing production incident taught you the most?

---

# 16. "Why" Questions

### Q161.
Why are events immutable?

---

### Q162.
Why is the Event Store append-only?

---

### Q163.
Why are snapshots optional rather than mandatory?

---

### Q164.
Why is Event Sourcing naturally suited for auditing?

---

### Q165.
Why are projections eventually consistent?

---

### Q166.
Why is replay one of the biggest advantages of Event Sourcing?

---

### Q167.
Why is schema evolution difficult?

---

### Q168.
Why should aggregates remain small?

---

### Q169.
Why should event payloads remain business-focused?

---

### Q170.
Why isn't Event Sourcing suitable for every application?

---

# 17. Trade-off Questions

### Q171.
Event Sourcing vs CRUD.

---

### Q172.
Event Store vs Relational Database.

---

### Q173.
Snapshots vs Full Replay.

---

### Q174.
Kafka vs EventStoreDB.

---

### Q175.
CQRS with Event Sourcing vs Traditional Architecture.

---

### Q176.
Domain Events vs Integration Events.

---

### Q177.
Replay vs Backup Restoration.

---

### Q178.
Append-only Storage vs Mutable Storage.

---

### Q179.
Optimistic Locking vs Pessimistic Locking.

---

### Q180.
Audit Tables vs Event Sourcing.

---

# 18. Common Interview Follow-up Questions

## If you mention Event Sourcing
- CRUD?
- Replay?
- Snapshots?
- Event Store?
- Aggregate reconstruction?

---

## If you mention Events
- Domain Events?
- Versioning?
- Metadata?
- Ordering?
- Upcasting?

---

## If you mention CQRS
- Read models?
- Projection?
- Eventual consistency?
- Materialized views?
- Synchronization?

---

## If you mention Kafka
- Retention?
- Replay?
- Offsets?
- Ordering?
- Log compaction?

---

## If you mention DDD
- Aggregates?
- Repository?
- Domain Events?
- Bounded Context?
- Invariants?

---

## If you mention Reliability
- Outbox?
- Idempotency?
- Duplicate events?
- Optimistic locking?
- Failure recovery?

---

# Staff Engineer Discussion Questions

### Q181.
How would you determine whether Event Sourcing is appropriate for a new enterprise platform?

---

### Q182.
How would you design an Event Store capable of handling billions of events?

---

### Q183.
How would you standardize event schemas across hundreds of engineering teams?

---

### Q184.
How would you migrate a large CRUD-based enterprise system to Event Sourcing incrementally?

---

### Q185.
How would you minimize replay time for petabyte-scale event stores?

---

### Q186.
How would you design organization-wide governance for event versioning?

---

### Q187.
How would you review Event Sourcing implementations for correctness and scalability?

---

### Q188.
How would you integrate Event Sourcing with Saga, CQRS, and Kafka at enterprise scale?

---

### Q189.
Which operational metrics would you continuously monitor in an Event Sourcing platform?

---

### Q190.
If you were designing an enterprise Event Store today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Event Sourcing
- [ ] Event Store
- [ ] Immutable Events
- [ ] Append-only Log
- [ ] Aggregate Reconstruction

## Storage
- [ ] Event Store
- [ ] Snapshots
- [ ] Event Replay
- [ ] Schema Evolution
- [ ] Versioning

## DDD Integration
- [ ] Aggregates
- [ ] Domain Events
- [ ] Repositories
- [ ] Bounded Contexts
- [ ] Aggregate Invariants

## CQRS
- [ ] Read Models
- [ ] Write Models
- [ ] Projections
- [ ] Materialized Views
- [ ] Replay

## Reliability
- [ ] Optimistic Locking
- [ ] Idempotency
- [ ] Outbox Pattern
- [ ] Inbox Pattern
- [ ] Failure Recovery

## Performance
- [ ] Snapshots
- [ ] Replay Optimization
- [ ] Storage Management
- [ ] Projection Scaling
- [ ] Capacity Planning

## Observability
- [ ] Correlation IDs
- [ ] Tracing
- [ ] Metrics
- [ ] Logging
- [ ] Audit Trails

## Interview Readiness
- [ ] Can explain Event Sourcing from first principles.
- [ ] Can compare Event Sourcing with CRUD and traditional persistence.
- [ ] Can design scalable Event Stores with snapshots and replay.
- [ ] Can integrate Event Sourcing with DDD, CQRS, Kafka, and Saga.
- [ ] Can discuss production-scale event replay, schema evolution, and operational trade-offs.

---

**Total Questions:** 190

**Recommended Time:** 5–6 Days

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** Event Store, Aggregate Reconstruction, Snapshots, Event Replay, CQRS Integration, Event Versioning, Schema Evolution, Kafka Integration, Optimistic Locking, Event Sourcing vs CRUD, Audit Trails, Replay Strategies