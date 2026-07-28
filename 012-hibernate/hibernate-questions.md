# Hibernate Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Hibernate Version:** Hibernate ORM 6.x (Spring Boot 3.x)
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Hibernate is one of the highest-priority topics in Java backend interviews. While Spring Data JPA abstracts many operations, interviewers often dive into Hibernate internals to evaluate a candidate's understanding of ORM, caching, persistence, SQL generation, performance tuning, and transaction management.

---

# Table of Contents

1. Hibernate Fundamentals
2. Hibernate Architecture
3. Session & SessionFactory
4. Entity Lifecycle
5. Persistence Context
6. Dirty Checking
7. Fetching Strategies
8. Relationships & Mapping
9. Cascading & Orphan Removal
10. Caching
11. HQL & Criteria API
12. Native SQL
13. Locking
14. Batch Processing
15. Performance Optimization
16. Hibernate Internals
17. Advanced Questions
18. Scenario-Based Questions
19. Production Experience
20. Why Questions
21. Trade-offs
22. Common Follow-up Questions

---

# 1. Hibernate Fundamentals

## Basic

### Q1.
What is Hibernate?

**Follow-ups**
- Why was Hibernate created?
- What problems does it solve?

---

### Q2.
Difference between JDBC and Hibernate.

---

### Q3.
Difference between Hibernate and JPA.

---

### Q4.
Can Hibernate work without JPA?

---

### Q5.
Can JPA work without Hibernate?

---

### Q6.
What is ORM?

---

### Q7.
Advantages of Hibernate.

---

### Q8.
Disadvantages of Hibernate.

---

### Q9.
What are Hibernate modules?

---

### Q10.
How does Hibernate fit into Spring Boot?

---

# 2. Hibernate Architecture

## Basic

### Q11.
Draw Hibernate architecture.

---

### Q12.
Explain SessionFactory.

---

### Q13.
Explain Session.

---

### Q14.
Explain Transaction.

---

### Q15.
Explain Query.

---

### Q16.
Explain Configuration.

---

### Q17.
How does Hibernate communicate with JDBC?

---

### Q18.
What is Dialect?

---

### Q19.
How does Hibernate generate SQL?

---

### Q20.
How does Hibernate map Java objects to database tables?

---

# 3. Session & SessionFactory

## Intermediate

### Q21.
What is SessionFactory?

---

### Q22.
Why is SessionFactory thread-safe?

---

### Q23.
How many SessionFactory instances should an application have?

---

### Q24.
What is Session?

---

### Q25.
Is Session thread-safe?

---

### Q26.
Difference between Session and EntityManager.

---

### Q27.
openSession() vs getCurrentSession().

---

### Q28.
Session lifecycle.

---

### Q29.
When is a Session closed?

---

### Q30.
Common Session-related issues.

---

# 4. Entity Lifecycle

## Intermediate

### Q31.
Explain Hibernate entity lifecycle.

---

### Q32.
Transient state.

---

### Q33.
Persistent state.

---

### Q34.
Detached state.

---

### Q35.
Removed state.

---

### Q36.
State transitions.

---

### Q37.
persist().

---

### Q38.
save().

---

### Q39.
merge().

---

### Q40.
update().

---

### Q41.
saveOrUpdate().

---

### Q42.
delete().

---

### Q43.
evict().

---

### Q44.
refresh().

---

### Q45.
replicate().

---

# 5. Persistence Context

## Advanced

### Q46.
What is Persistence Context?

---

### Q47.
How does Hibernate implement Persistence Context?

---

### Q48.
First-Level Cache.

---

### Q49.
Identity Map.

---

### Q50.
Entity uniqueness guarantee.

---

### Q51.
flush().

---

### Q52.
clear().

---

### Q53.
detach().

---

### Q54.
Persistence Context synchronization.

---

### Q55.
Persistence Context lifecycle.

---

# 6. Dirty Checking

### Q56.
What is Dirty Checking?

---

### Q57.
How does Dirty Checking work internally?

---

### Q58.
Snapshot mechanism.

---

### Q59.
When does Dirty Checking occur?

---

### Q60.
How does Hibernate know an entity changed?

---

### Q61.
Bytecode enhancement.

---

### Q62.
Dynamic Update.

---

### Q63.
Dynamic Insert.

---

### Q64.
Read-only entities.

---

### Q65.
Performance implications.

---

# 7. Fetching Strategies

### Q66.
LAZY fetching.

---

### Q67.
EAGER fetching.

---

### Q68.
Default fetch types.

---

### Q69.
Proxy objects.

---

### Q70.
LazyInitializationException.

---

### Q71.
N+1 Query Problem.

---

### Q72.
How to identify N+1 queries.

---

### Q73.
JOIN FETCH.

---

### Q74.
Batch Fetching.

---

### Q75.
Subselect Fetching.

---

### Q76.
Fetch Profiles.

---

### Q77.
Entity Graphs.

---

### Q78.
Open Session In View.

---

### Q79.
MultipleBagFetchException.

---

### Q80.
Fetching best practices.

---

# 8. Relationships & Mapping

### Q81.
One-to-One.

---

### Q82.
One-to-Many.

---

### Q83.
Many-to-One.

---

### Q84.
Many-to-Many.

---

### Q85.
mappedBy.

---

### Q86.
@JoinColumn.

---

### Q87.
@JoinTable.

---

### Q88.
Embedded Objects.

---

### Q89.
Composite Keys.

---

### Q90.
@Embeddable vs @EmbeddedId.

---

### Q91.
@IdClass.

---

### Q92.
Inheritance Mapping.

---

### Q93.
Single Table Strategy.

---

### Q94.
Joined Strategy.

---

### Q95.
Table Per Class Strategy.

---

# 9. Cascading & Orphan Removal

### Q96.
Cascade types.

---

### Q97.
Cascade ALL.

---

### Q98.
Cascade REMOVE.

---

### Q99.
Cascade MERGE.

---

### Q100.
Cascade PERSIST.

---

### Q101.
Cascade DETACH.

---

### Q102.
Cascade REFRESH.

---

### Q103.
Orphan Removal.

---

### Q104.
Cascade pitfalls.

---

### Q105.
Best practices.

---

# 10. Caching

## Advanced

### Q106.
Why does Hibernate use caching?

---

### Q107.
First-Level Cache.

---

### Q108.
Second-Level Cache.

---

### Q109.
Query Cache.

---

### Q110.
Difference between First-Level and Second-Level Cache.

---

### Q111.
How does Second-Level Cache work?

---

### Q112.
Cache providers.

---

### Q113.
Ehcache.

---

### Q114.
Redis as Hibernate cache.

---

### Q115.
Cache concurrency strategies.

---

### Q116.
READ_ONLY.

---

### Q117.
NONSTRICT_READ_WRITE.

---

### Q118.
READ_WRITE.

---

### Q119.
TRANSACTIONAL.

---

### Q120.
When should caching be avoided?

---

# 11. HQL & Criteria API

### Q121.
What is HQL?

---

### Q122.
HQL vs SQL.

---

### Q123.
HQL vs JPQL.

---

### Q124.
Named Queries.

---

### Q125.
Criteria API.

---

### Q126.
CriteriaBuilder.

---

### Q127.
CriteriaQuery.

---

### Q128.
Dynamic Queries.

---

### Q129.
Pagination.

---

### Q130.
Aggregations.

---

### Q131.
Subqueries.

---

### Q132.
Bulk updates.

---

### Q133.
Bulk deletes.

---

### Q134.
DTO projection.

---

### Q135.
Performance considerations.

---

# 12. Native SQL

### Q136.
When should Native SQL be used?

---

### Q137.
Advantages.

---

### Q138.
Disadvantages.

---

### Q139.
Vendor-specific SQL.

---

### Q140.
Stored Procedures.

---

### Q141.
Mapping results.

---

### Q142.
Named Native Queries.

---

### Q143.
Pagination.

---

### Q144.
Performance tuning.

---

### Q145.
Database portability.

---

# 13. Locking

### Q146.
Optimistic Locking.

---

### Q147.
Pessimistic Locking.

---

### Q148.
@Version.

---

### Q149.
LockMode.

---

### Q150.
LockModeType.

---

### Q151.
OptimisticLockException.

---

### Q152.
Lost Update Problem.

---

### Q153.
Deadlocks.

---

### Q154.
Retry mechanisms.

---

### Q155.
Choosing locking strategies.

---

# 14. Batch Processing

### Q156.
Batch Inserts.

---

### Q157.
Batch Updates.

---

### Q158.
Batch Deletes.

---

### Q159.
hibernate.jdbc.batch_size.

---

### Q160.
flush() and clear() in batch processing.

---

### Q161.
Scrollable Results.

---

### Q162.
StatelessSession.

---

### Q163.
Memory optimization.

---

### Q164.
Large dataset processing.

---

### Q165.
Production recommendations.

---

# 15. Performance Optimization

### Q166.
SQL logging.

---

### Q167.
Hibernate Statistics.

---

### Q168.
show_sql vs logging framework.

---

### Q169.
SQL formatting.

---

### Q170.
Statement batching.

---

### Q171.
Fetch size.

---

### Q172.
DTO projections.

---

### Q173.
Read-only transactions.

---

### Q174.
Avoiding unnecessary updates.

---

### Q175.
Performance tuning checklist.

---

# 16. Hibernate Internals

## Advanced

### Q176.
How does Hibernate generate proxy objects?

---

### Q177.
How does bytecode enhancement work?

---

### Q178.
Action Queue.

---

### Q179.
Entity Persister.

---

### Q180.
Collection Persister.

---

### Q181.
Event Listeners.

---

### Q182.
Interceptor.

---

### Q183.
Hibernate SPI.

---

### Q184.
Dirty Checking internals.

---

### Q185.
SQL generation pipeline.

---

### Q186.
Flush process.

---

### Q187.
Transaction synchronization.

---

### Q188.
JDBC batching internals.

---

### Q189.
PersistenceContext implementation.

---

### Q190.
How Hibernate integrates with Spring Transactions.

---

# 17. Advanced Questions

### Q191.
How does Hibernate decide between INSERT and UPDATE?

---

### Q192.
How does merge() differ internally from update()?

---

### Q193.
How does Hibernate avoid duplicate entity instances?

---

### Q194.
How does Hibernate optimize SQL generation?

---

### Q195.
How does Hibernate minimize database round trips?

---

### Q196.
How does bytecode enhancement improve performance?

---

### Q197.
Why does LazyInitializationException occur?

---

### Q198.
How does Hibernate synchronize with the database during commit?

---

### Q199.
How do caches affect transaction consistency?

---

### Q200.
Performance implications of a large Persistence Context.

---

# 18. Scenario-Based Questions

### Q201.
Your application suffers from N+1 queries. How would you diagnose and fix them?

---

### Q202.
A transaction updates thousands of rows and eventually runs out of memory. How would you optimize it?

---

### Q203.
A LazyInitializationException appears in production. How would you investigate it?

---

### Q204.
A service becomes slow after enabling the Second-Level Cache. Why might this happen?

---

### Q205.
Two users update the same record simultaneously. Which locking strategy would you choose?

---

### Q206.
A repository executes hundreds of UPDATE statements although only a few entities changed. What Hibernate mechanisms would you investigate?

---

### Q207.
An API returns entities with circular references causing serialization issues. How would you redesign the persistence layer?

---

### Q208.
A bulk update query leaves cached entities stale. What should you consider?

---

### Q209.
Batch inserts are slower than expected. Which Hibernate settings would you tune?

---

### Q210.
A Hibernate Session grows continuously during a long-running job. How would you prevent memory issues?

---

# 19. Production Experience Questions

### Q211.
Have you optimized Hibernate-generated SQL in production?

---

### Q212.
How have you solved the N+1 query problem?

---

### Q213.
Have you configured Second-Level Cache?

---

### Q214.
How do you monitor Hibernate performance?

---

### Q215.
Have you used Hibernate Statistics?

---

### Q216.
How do you optimize large batch jobs?

---

### Q217.
How do you debug LazyInitializationException?

---

### Q218.
Have you customized Hibernate Interceptors or Event Listeners?

---

### Q219.
How do you profile Hibernate-generated SQL?

---

### Q220.
What Hibernate production issue taught you the most?

---

# 20. "Why" Questions

### Q221.
Why does Hibernate use proxies?

---

### Q222.
Why is LAZY loading preferred?

---

### Q223.
Why is EAGER fetching discouraged?

---

### Q224.
Why is Dirty Checking considered a major Hibernate feature?

---

### Q225.
Why is Session not thread-safe?

---

### Q226.
Why is SessionFactory thread-safe?

---

### Q227.
Why is the First-Level Cache mandatory?

---

### Q228.
Why are DTO projections often better than entities for read APIs?

---

### Q229.
Why is Optimistic Locking preferred for most applications?

---

### Q230.
Why should Hibernate Sessions remain short-lived?

---

# 21. Trade-off Questions

### Q231.
Hibernate vs JDBC.

---

### Q232.
Hibernate vs Spring Data JPA.

---

### Q233.
Session vs EntityManager.

---

### Q234.
LAZY vs EAGER Fetching.

---

### Q235.
First-Level Cache vs Second-Level Cache.

---

### Q236.
HQL vs Native SQL.

---

### Q237.
Optimistic vs Pessimistic Locking.

---

### Q238.
merge() vs update().

---

### Q239.
Batch Processing vs Single-row Operations.

---

### Q240.
Entity Retrieval vs DTO Projection.

---

# 22. Common Interview Follow-up Questions

## If you mention Session
- SessionFactory?
- Thread safety?
- Persistence Context?
- flush()?
- clear()?

---

## If you mention Dirty Checking
- Snapshot?
- Bytecode enhancement?
- flush()?
- Dynamic Update?
- Read-only transactions?

---

## If you mention Fetching
- N+1?
- JOIN FETCH?
- Entity Graph?
- Proxy?
- LazyInitializationException?

---

## If you mention Caching
- First-Level Cache?
- Second-Level Cache?
- Query Cache?
- Cache providers?
- Concurrency strategies?

---

## If you mention Locking
- @Version?
- Lost updates?
- Deadlocks?
- Retry?
- LockMode?

---

## If you mention Performance
- Batch processing?
- DTO projections?
- Hibernate Statistics?
- SQL logging?
- Fetch size?

---

# Staff Engineer Discussion Questions

### Q241.
How would you standardize Hibernate usage across hundreds of microservices?

---

### Q242.
How do you decide when to bypass Hibernate and use JDBC?

---

### Q243.
How would you review a codebase for Hibernate performance anti-patterns?

---

### Q244.
How would you minimize database round trips while maintaining clean domain models?

---

### Q245.
How do you monitor Hibernate performance in production?

---

### Q246.
How would you design caching strategies for high-read enterprise applications?

---

### Q247.
How would you educate junior engineers about Hibernate pitfalls?

---

### Q248.
How do Hibernate internals influence architectural decisions in large systems?

---

### Q249.
What metrics would you monitor to detect Hibernate bottlenecks?

---

### Q250.
If you were redesigning Hibernate today, what would you improve and why?

---

# Completion Checklist

## Fundamentals
- [ ] ORM
- [ ] Hibernate Architecture
- [ ] SessionFactory
- [ ] Session
- [ ] Transactions

## Persistence
- [ ] Entity Lifecycle
- [ ] Persistence Context
- [ ] Dirty Checking
- [ ] Flush
- [ ] Entity States

## Fetching
- [ ] LAZY Loading
- [ ] EAGER Loading
- [ ] N+1 Problem
- [ ] Fetch Join
- [ ] Entity Graph

## Mapping
- [ ] Relationships
- [ ] Composite Keys
- [ ] Inheritance Mapping
- [ ] Cascading
- [ ] Orphan Removal

## Performance
- [ ] Caching
- [ ] Batch Processing
- [ ] SQL Optimization
- [ ] Hibernate Statistics
- [ ] DTO Projections

## Concurrency
- [ ] Optimistic Locking
- [ ] Pessimistic Locking
- [ ] @Version
- [ ] Deadlocks
- [ ] Retry Strategies

## Advanced
- [ ] Proxy Objects
- [ ] Bytecode Enhancement
- [ ] Action Queue
- [ ] Event Listeners
- [ ] Hibernate SPI

## Production
- [ ] SQL Monitoring
- [ ] Performance Tuning
- [ ] Cache Configuration
- [ ] Batch Jobs
- [ ] Memory Optimization

## Interview Readiness
- [ ] Can explain Hibernate architecture and Session lifecycle.
- [ ] Can diagnose N+1 queries and LazyInitializationException.
- [ ] Can explain Dirty Checking and Persistence Context internals.
- [ ] Can compare Hibernate APIs (persist, merge, update, save).
- [ ] Can discuss Hibernate performance tuning and caching strategies with production examples.

---

**Total Questions:** 250
**Recommended Time:** 5–6 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** Session vs SessionFactory, Persistence Context, Dirty Checking, Fetch Strategies, N+1 Query Problem, LazyInitializationException, Caching, Locking, Batch Processing, Hibernate Internals, Performance Optimization