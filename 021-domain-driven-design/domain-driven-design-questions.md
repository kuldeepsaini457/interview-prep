# Domain-Driven Design (DDD) Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Uber, Google, LinkedIn, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** Java, Spring Boot, Microservices, Event-Driven Architecture, Distributed Systems
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Domain-Driven Design (DDD) is one of the most important architectural concepts for designing scalable microservices. Interviewers expect candidates to understand strategic design, tactical design, bounded contexts, aggregates, entities, value objects, repositories, domain events, and how DDD influences real-world distributed systems.

---

# Table of Contents

1. DDD Fundamentals
2. Strategic Design
3. Bounded Context
4. Ubiquitous Language
5. Context Mapping
6. Tactical Design
7. Entities
8. Value Objects
9. Aggregates
10. Repositories
11. Domain Services
12. Factories
13. Domain Events
14. DDD with Microservices
15. CQRS & Event Sourcing
16. Advanced DDD Concepts
17. Scenario-Based Questions
18. Production Experience
19. Why Questions
20. Trade-offs
21. Common Follow-up Questions

---

# 1. DDD Fundamentals

## Basic

### Q1.
What is Domain-Driven Design (DDD)?

**Follow-ups**
- Why was DDD introduced?
- Who introduced DDD?

---

### Q2.
What problems does DDD solve?

---

### Q3.
What is a Domain?

---

### Q4.
What is the Domain Model?

---

### Q5.
Core Domain vs Supporting Domain vs Generic Domain.

---

### Q6.
What is Domain Knowledge?

---

### Q7.
Characteristics of a good domain model.

---

### Q8.
DDD vs Traditional Layered Architecture.

---

### Q9.
When should DDD be used?

---

### Q10.
When should DDD NOT be used?

---

# 2. Strategic Design

## Intermediate

### Q11.
What is Strategic Design?

---

### Q12.
Business Capability.

---

### Q13.
Subdomains.

---

### Q14.
Core Domain.

---

### Q15.
Supporting Subdomain.

---

### Q16.
Generic Subdomain.

---

### Q17.
How do you identify business capabilities?

---

### Q18.
How do you identify subdomains?

---

### Q19.
Strategic Design vs Tactical Design.

---

### Q20.
Business-driven architecture.

---

# 3. Bounded Context

### Q21.
What is a Bounded Context?

---

### Q22.
Why are Bounded Contexts important?

---

### Q23.
Bounded Context vs Microservice.

---

### Q24.
How do you identify Bounded Contexts?

---

### Q25.
How big should a Bounded Context be?

---

### Q26.
Shared Kernel.

---

### Q27.
Separate Ways.

---

### Q28.
Customer-Supplier relationship.

---

### Q29.
Open Host Service.

---

### Q30.
Published Language.

---

# 4. Ubiquitous Language

### Q31.
What is Ubiquitous Language?

---

### Q32.
Why is it important?

---

### Q33.
Developers and domain experts collaboration.

---

### Q34.
How do you establish a ubiquitous language?

---

### Q35.
Terminology consistency.

---

### Q36.
Code reflecting business language.

---

### Q37.
Documentation using ubiquitous language.

---

### Q38.
Common mistakes.

---

### Q39.
Production examples.

---

### Q40.
Maintaining language consistency.

---

# 5. Context Mapping

### Q41.
What is Context Mapping?

---

### Q42.
Shared Kernel.

---

### Q43.
Partnership.

---

### Q44.
Customer-Supplier.

---

### Q45.
Conformist.

---

### Q46.
Anti-Corruption Layer (ACL).

---

### Q47.
Open Host Service.

---

### Q48.
Published Language.

---

### Q49.
Separate Ways.

---

### Q50.
Choosing the right relationship.

---

# 6. Tactical Design

## Advanced

### Q51.
What is Tactical Design?

---

### Q52.
Building Blocks of Tactical Design.

---

### Q53.
Entities.

---

### Q54.
Value Objects.

---

### Q55.
Aggregates.

---

### Q56.
Repositories.

---

### Q57.
Factories.

---

### Q58.
Domain Services.

---

### Q59.
Domain Events.

---

### Q60.
Application Services.

---

# 7. Entities

### Q61.
What is an Entity?

---

### Q62.
Identity.

---

### Q63.
Entity lifecycle.

---

### Q64.
Mutable entities.

---

### Q65.
Entity equality.

---

### Q66.
Persistence concerns.

---

### Q67.
Entity behavior.

---

### Q68.
Rich Domain Model.

---

### Q69.
Anemic Domain Model.

---

### Q70.
Best practices.

---

# 8. Value Objects

### Q71.
What is a Value Object?

---

### Q72.
Characteristics.

---

### Q73.
Immutability.

---

### Q74.
Equality.

---

### Q75.
Value Object examples.

---

### Q76.
Value Objects vs Entities.

---

### Q77.
Embedding Value Objects.

---

### Q78.
Validation.

---

### Q79.
Performance implications.

---

### Q80.
Best practices.

---

# 9. Aggregates

## Highest Priority

### Q81.
What is an Aggregate?

---

### Q82.
Aggregate Root.

---

### Q83.
Aggregate boundaries.

---

### Q84.
Aggregate invariants.

---

### Q85.
Transaction boundaries.

---

### Q86.
Aggregate consistency.

---

### Q87.
Aggregate references.

---

### Q88.
Small vs Large aggregates.

---

### Q89.
Cross-aggregate communication.

---

### Q90.
Aggregate design best practices.

---

# 10. Repositories

### Q91.
What is a Repository?

---

### Q92.
Repository vs DAO.

---

### Q93.
Repository responsibilities.

---

### Q94.
Repository implementation.

---

### Q95.
Aggregate persistence.

---

### Q96.
Custom repositories.

---

### Q97.
Repository interfaces.

---

### Q98.
Spring Data repositories.

---

### Q99.
Repository anti-patterns.

---

### Q100.
Best practices.

---

# 11. Domain Services

### Q101.
What is a Domain Service?

---

### Q102.
When should Domain Services be used?

---

### Q103.
Domain Service vs Application Service.

---

### Q104.
Business logic placement.

---

### Q105.
Stateless Domain Services.

---

### Q106.
Cross-aggregate operations.

---

### Q107.
Dependency management.

---

### Q108.
Examples.

---

### Q109.
Testing Domain Services.

---

### Q110.
Best practices.

---

# 12. Factories

### Q111.
Factory Pattern in DDD.

---

### Q112.
Factory responsibilities.

---

### Q113.
Complex object creation.

---

### Q114.
Aggregate creation.

---

### Q115.
Validation during creation.

---

### Q116.
Factory vs Builder.

---

### Q117.
Factory placement.

---

### Q118.
Examples.

---

### Q119.
Testing factories.

---

### Q120.
Best practices.

---

# 13. Domain Events

### Q121.
What is a Domain Event?

---

### Q122.
Domain Event vs Integration Event.

---

### Q123.
Event publication.

---

### Q124.
Event handlers.

---

### Q125.
Event consistency.

---

### Q126.
Event ordering.

---

### Q127.
Outbox Pattern.

---

### Q128.
Reliable publishing.

---

### Q129.
Event versioning.

---

### Q130.
Best practices.

---

# 14. DDD with Microservices

### Q131.
DDD and Microservices.

---

### Q132.
Bounded Context vs Service.

---

### Q133.
Database per Bounded Context.

---

### Q134.
Domain Events between services.

---

### Q135.
API design using DDD.

---

### Q136.
Saga with DDD.

---

### Q137.
Event-driven architecture with DDD.

---

### Q138.
CQRS integration.

---

### Q139.
Service decomposition.

---

### Q140.
Production recommendations.

---

# 15. CQRS & Event Sourcing

### Q141.
CQRS with DDD.

---

### Q142.
Event Sourcing with DDD.

---

### Q143.
Aggregate reconstruction.

---

### Q144.
Snapshots.

---

### Q145.
Read models.

---

### Q146.
Event replay.

---

### Q147.
Version migration.

---

### Q148.
Consistency.

---

### Q149.
Trade-offs.

---

### Q150.
Production examples.

---

# 16. Advanced DDD Concepts

### Q151.
Anemic Domain Model.

---

### Q152.
Rich Domain Model.

---

### Q153.
Domain Model evolution.

---

### Q154.
Legacy system migration.

---

### Q155.
Anti-Corruption Layer.

---

### Q156.
Hexagonal Architecture.

---

### Q157.
Clean Architecture.

---

### Q158.
Ports & Adapters.

---

### Q159.
Strategic refactoring.

---

### Q160.
DDD anti-patterns.

---

# 17. Scenario-Based Questions

### Q161.
How would you identify Bounded Contexts for an e-commerce platform?

---

### Q162.
How would you model an Order Aggregate?

---

### Q163.
How would you model Inventory and Order as separate aggregates?

---

### Q164.
A business invariant spans multiple aggregates. How would you maintain consistency?

---

### Q165.
How would you migrate an anemic domain model to a rich domain model?

---

### Q166.
How would you design a payment domain using DDD?

---

### Q167.
A legacy monolith has shared entities across modules. How would you introduce Bounded Contexts?

---

### Q168.
How would you prevent aggregate boundaries from becoming too large?

---

### Q169.
How would you integrate DDD with Kafka-based event-driven architecture?

---

### Q170.
How would you design a booking system using DDD?

---

### Q171.
How would you model a bank account aggregate?

---

### Q172.
How would you review a domain model during an architecture review?

---

### Q173.
How would you split a User module into multiple Bounded Contexts?

---

### Q174.
How would you model discounts and promotions without violating aggregate boundaries?

---

### Q175.
How would you evolve a domain model as business rules change?

---

# 18. Production Experience Questions

### Q176.
Have you used DDD in production?

---

### Q177.
How did you identify service boundaries?

---

### Q178.
How did you collaborate with domain experts?

---

### Q179.
How do you review aggregate designs?

---

### Q180.
Have you implemented Domain Events?

---

### Q181.
How do you prevent anemic domain models?

---

### Q182.
How do you model complex business rules?

---

### Q183.
How do you integrate DDD with Spring Boot?

---

### Q184.
How do you evolve domain models safely?

---

### Q185.
What DDD-related production incident taught you the most?

---

# 19. "Why" Questions

### Q186.
Why should aggregates enforce invariants?

---

### Q187.
Why should aggregate boundaries remain small?

---

### Q188.
Why are Value Objects immutable?

---

### Q189.
Why should entities contain behavior instead of only data?

---

### Q190.
Why are repositories designed around aggregates?

---

### Q191.
Why is Ubiquitous Language important?

---

### Q192.
Why should every Bounded Context own its data?

---

### Q193.
Why are Domain Events useful?

---

### Q194.
Why should external systems communicate through ACLs?

---

### Q195.
Why is DDD not suitable for every application?

---

# 20. Trade-off Questions

### Q196.
Rich Domain Model vs Anemic Domain Model.

---

### Q197.
Entity vs Value Object.

---

### Q198.
Repository vs DAO.

---

### Q199.
Aggregate vs Entity.

---

### Q200.
DDD vs CRUD Architecture.

---

### Q201.
Bounded Context vs Microservice.

---

### Q202.
Domain Events vs Integration Events.

---

### Q203.
Factory vs Builder.

---

### Q204.
ACL vs Direct Integration.

---

### Q205.
DDD vs Traditional Layered Architecture.

---

# 21. Common Interview Follow-up Questions

## If you mention DDD
- Strategic Design?
- Tactical Design?
- Eric Evans?
- Domain Model?
- Business capability?

---

## If you mention Aggregates
- Aggregate Root?
- Invariants?
- Transactions?
- References?
- Consistency?

---

## If you mention Bounded Context
- Context Mapping?
- Shared Kernel?
- ACL?
- Published Language?
- Open Host Service?

---

## If you mention Entities
- Identity?
- Equality?
- Lifecycle?
- Behavior?
- Persistence?

---

## If you mention Domain Events
- Integration Events?
- Outbox?
- Kafka?
- Eventual consistency?
- Versioning?

---

## If you mention Repositories
- Spring Data?
- DAO?
- Aggregate persistence?
- Repository interfaces?
- Testing?

---

# Staff Engineer Discussion Questions

### Q206.
How would you introduce DDD into an organization with dozens of legacy services?

---

### Q207.
How would you identify Bounded Contexts for a new enterprise platform?

---

### Q208.
How would you review aggregate boundaries across hundreds of microservices?

---

### Q209.
How would you establish organization-wide Ubiquitous Language?

---

### Q210.
How would you prevent domain model degradation over multiple years?

---

### Q211.
How would you integrate DDD with event-driven architecture at enterprise scale?

---

### Q212.
How would you balance business-driven design with engineering simplicity?

---

### Q213.
How would you migrate a CRUD application toward DDD incrementally?

---

### Q214.
Which metrics would indicate unhealthy domain boundaries?

---

### Q215.
If you were designing an enterprise platform from scratch today, what DDD principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Domain-Driven Design
- [ ] Strategic Design
- [ ] Tactical Design
- [ ] Domain Model
- [ ] Business Capabilities

## Strategic Design
- [ ] Bounded Context
- [ ] Context Mapping
- [ ] Ubiquitous Language
- [ ] ACL
- [ ] Shared Kernel

## Tactical Design
- [ ] Entities
- [ ] Value Objects
- [ ] Aggregates
- [ ] Repositories
- [ ] Domain Services

## Integration
- [ ] Domain Events
- [ ] Integration Events
- [ ] Outbox Pattern
- [ ] CQRS
- [ ] Event Sourcing

## Architecture
- [ ] Microservices
- [ ] Hexagonal Architecture
- [ ] Clean Architecture
- [ ] Ports & Adapters
- [ ] Aggregate Boundaries

## Interview Readiness
- [ ] Can identify Bounded Contexts from business requirements.
- [ ] Can design Aggregates with correct transaction boundaries.
- [ ] Can distinguish Entities, Value Objects, Domain Services, and Repositories.
- [ ] Can integrate DDD with Microservices, Kafka, Saga, and CQRS.
- [ ] Can discuss strategic and tactical DDD decisions using real-world examples.

---

**Total Questions:** 215

**Recommended Time:** 6–7 Days

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** Bounded Context, Aggregates, Aggregate Root, Value Objects, Entities, Ubiquitous Language, Context Mapping, Anti-Corruption Layer, Domain Events, Repository Pattern, Rich Domain Model, DDD with Microservices