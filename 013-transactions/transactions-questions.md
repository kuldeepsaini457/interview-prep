# Transactions Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Technology Focus:** Spring Framework 6.x, Spring Boot 3.x, Spring Data JPA, Hibernate, JDBC
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Transactions are one of the most frequently asked backend interview topics because they sit at the intersection of databases, Spring, Hibernate, concurrency, distributed systems, and microservices. Interviewers expect engineers to understand ACID properties, transaction propagation, isolation levels, rollback behavior, Spring transaction internals, distributed transactions, and production debugging.

---

# Table of Contents

1. Transaction Fundamentals
2. ACID Properties
3. Spring Transaction Management
4. @Transactional
5. Transaction Propagation
6. Transaction Isolation Levels
7. Rollback Management
8. Transaction Lifecycle
9. Read-Only Transactions
10. Nested Transactions
11. Savepoints
12. Transaction Synchronization
13. Programmatic Transactions
14. JPA & Hibernate Transactions
15. Distributed Transactions
16. Performance & Optimization
17. Spring Transaction Internals
18. Advanced Questions
19. Scenario-Based Questions
20. Production Experience
21. Why Questions
22. Trade-offs
23. Common Follow-up Questions

---

# 1. Transaction Fundamentals

## Basic

### Q1.
What is a database transaction?

**Follow-ups**
- Why are transactions needed?
- What problems do they solve?

---

### Q2.
What are the properties of a transaction?

---

### Q3.
What happens if a transaction is interrupted?

---

### Q4.
Difference between a transaction and a database query.

---

### Q5.
What operations are typically performed inside a transaction?

---

### Q6.
What is transaction consistency?

---

### Q7.
What is transaction durability?

---

### Q8.
Can transactions span multiple SQL statements?

---

### Q9.
What is auto-commit mode?

---

### Q10.
When should auto-commit be disabled?

---

# 2. ACID Properties

## Basic

### Q11.
Explain ACID properties.

---

### Q12.
Atomicity.

---

### Q13.
Consistency.

---

### Q14.
Isolation.

---

### Q15.
Durability.

---

### Q16.
Can a database satisfy ACID without transactions?

---

### Q17.
Which ACID property is hardest to implement?

---

### Q18.
How do relational databases implement Atomicity?

---

### Q19.
How is Durability guaranteed?

---

### Q20.
Production examples of ACID.

---

# 3. Spring Transaction Management

## Intermediate

### Q21.
How does Spring manage transactions?

---

### Q22.
Declarative vs Programmatic Transactions.

---

### Q23.
PlatformTransactionManager.

---

### Q24.
JpaTransactionManager.

---

### Q25.
DataSourceTransactionManager.

---

### Q26.
JtaTransactionManager.

---

### Q27.
How does Spring choose the TransactionManager?

---

### Q28.
TransactionInterceptor.

---

### Q29.
TransactionAttributeSource.

---

### Q30.
How does Spring create transactional proxies?

---

# 4. @Transactional

## Intermediate

### Q31.
What is `@Transactional`?

---

### Q32.
Where can `@Transactional` be applied?

---

### Q33.
Class-level vs Method-level `@Transactional`.

---

### Q34.
Default behavior of `@Transactional`.

---

### Q35.
How does Spring detect transactional methods?

---

### Q36.
How does proxy-based transaction management work?

---

### Q37.
Can private methods be transactional?

---

### Q38.
Can final methods be transactional?

---

### Q39.
Can static methods be transactional?

---

### Q40.
Self Invocation problem.

---

### Q41.
How do you solve Self Invocation?

---

### Q42.
Transaction boundaries.

---

### Q43.
Transaction timeout.

---

### Q44.
Transaction naming.

---

### Q45.
Best practices for using `@Transactional`.

---

# 5. Transaction Propagation

## Advanced

### Q46.
What is transaction propagation?

---

### Q47.
Propagation.REQUIRED.

---

### Q48.
Propagation.REQUIRES_NEW.

---

### Q49.
Propagation.MANDATORY.

---

### Q50.
Propagation.NEVER.

---

### Q51.
Propagation.NOT_SUPPORTED.

---

### Q52.
Propagation.SUPPORTS.

---

### Q53.
Propagation.NESTED.

---

### Q54.
Difference between REQUIRED and REQUIRES_NEW.

---

### Q55.
Difference between REQUIRES_NEW and NESTED.

---

### Q56.
How does Spring suspend transactions?

---

### Q57.
When should REQUIRES_NEW be used?

---

### Q58.
When should NESTED be used?

---

### Q59.
Common propagation mistakes.

---

### Q60.
Production examples.

---

# 6. Transaction Isolation Levels

## Advanced

### Q61.
What is transaction isolation?

---

### Q62.
READ_UNCOMMITTED.

---

### Q63.
READ_COMMITTED.

---

### Q64.
REPEATABLE_READ.

---

### Q65.
SERIALIZABLE.

---

### Q66.
DEFAULT isolation.

---

### Q67.
Dirty Read.

---

### Q68.
Non-repeatable Read.

---

### Q69.
Phantom Read.

---

### Q70.
Lost Update.

---

### Q71.
Which isolation level prevents Dirty Reads?

---

### Q72.
Which isolation level prevents Phantom Reads?

---

### Q73.
Isolation level support across databases.

---

### Q74.
Isolation level performance trade-offs.

---

### Q75.
Production recommendations.

---

# 7. Rollback Management

### Q76.
When does Spring roll back a transaction?

---

### Q77.
Checked Exception rollback.

---

### Q78.
Runtime Exception rollback.

---

### Q79.
rollbackFor.

---

### Q80.
noRollbackFor.

---

### Q81.
UnexpectedRollbackException.

---

### Q82.
Marking transactions rollback-only.

---

### Q83.
Programmatic rollback.

---

### Q84.
Partial rollback.

---

### Q85.
Rollback best practices.

---

# 8. Transaction Lifecycle

### Q86.
Transaction begin.

---

### Q87.
Transaction commit.

---

### Q88.
Transaction rollback.

---

### Q89.
Flush before commit.

---

### Q90.
Synchronization callbacks.

---

### Q91.
Transaction completion.

---

### Q92.
Resource cleanup.

---

### Q93.
Connection release.

---

### Q94.
What happens during commit?

---

### Q95.
What happens during rollback?

---

# 9. Read-Only Transactions

### Q96.
What is a read-only transaction?

---

### Q97.
How does Spring implement read-only transactions?

---

### Q98.
Hibernate optimization for read-only transactions.

---

### Q99.
Can entities still be modified?

---

### Q100.
Performance benefits.

---

### Q101.
Limitations.

---

### Q102.
Read-only in MySQL.

---

### Q103.
Read-only in PostgreSQL.

---

### Q104.
Production recommendations.

---

### Q105.
Common misconceptions.

---

# 10. Nested Transactions

### Q106.
What are nested transactions?

---

### Q107.
How are Savepoints used?

---

### Q108.
Database support.

---

### Q109.
Nested rollback.

---

### Q110.
Nested commit.

---

### Q111.
REQUIRES_NEW vs Nested.

---

### Q112.
Nested transactions in JPA.

---

### Q113.
Limitations.

---

### Q114.
Production examples.

---

### Q115.
Best practices.

---

# 11. Savepoints

### Q116.
What is a Savepoint?

---

### Q117.
Creating Savepoints.

---

### Q118.
Rollback to Savepoint.

---

### Q119.
Savepoints vs Nested Transactions.

---

### Q120.
Database support.

---

# 12. Transaction Synchronization

### Q121.
TransactionSynchronizationManager.

---

### Q122.
TransactionSynchronization.

---

### Q123.
beforeCommit().

---

### Q124.
afterCommit().

---

### Q125.
afterCompletion().

---

### Q126.
Transaction-bound resources.

---

### Q127.
Connection binding.

---

### Q128.
ThreadLocal usage.

---

### Q129.
Transaction synchronization callbacks.

---

### Q130.
Production use cases.

---

# 13. Programmatic Transactions

### Q131.
TransactionTemplate.

---

### Q132.
PlatformTransactionManager API.

---

### Q133.
Programmatic commit.

---

### Q134.
Programmatic rollback.

---

### Q135.
When should programmatic transactions be used?

---

### Q136.
Declarative vs Programmatic.

---

### Q137.
Custom transaction handling.

---

### Q138.
Error handling.

---

### Q139.
Testing programmatic transactions.

---

### Q140.
Best practices.

---

# 14. JPA & Hibernate Transactions

### Q141.
How does Hibernate integrate with Spring Transactions?

---

### Q142.
Persistence Context and transactions.

---

### Q143.
Dirty Checking.

---

### Q144.
Flush timing.

---

### Q145.
FlushMode.

---

### Q146.
EntityManager synchronization.

---

### Q147.
Lazy Loading inside transactions.

---

### Q148.
Open Session In View.

---

### Q149.
Transaction boundaries and EntityManager.

---

### Q150.
Common Hibernate transaction issues.

---

# 15. Distributed Transactions

### Q151.
What are distributed transactions?

---

### Q152.
Two-Phase Commit (2PC).

---

### Q153.
Three-Phase Commit (3PC).

---

### Q154.
XA Transactions.

---

### Q155.
Why are distributed transactions expensive?

---

### Q156.
Saga Pattern.

---

### Q157.
Compensating Transactions.

---

### Q158.
Outbox Pattern.

---

### Q159.
Transactional Messaging.

---

### Q160.
Eventual Consistency.

---

# 16. Performance & Optimization

### Q161.
Keep transactions short.

---

### Q162.
Avoid long-running transactions.

---

### Q163.
Database locking impact.

---

### Q164.
Deadlock prevention.

---

### Q165.
Batch processing.

---

### Q166.
Transaction timeout tuning.

---

### Q167.
Connection pool utilization.

---

### Q168.
Read-only optimization.

---

### Q169.
Transaction monitoring.

---

### Q170.
Performance tuning checklist.

---

# 17. Spring Transaction Internals

### Q171.
TransactionAspectSupport.

---

### Q172.
TransactionInterceptor internals.

---

### Q173.
Transaction proxy creation.

---

### Q174.
AOP integration.

---

### Q175.
ThreadLocal transaction storage.

---

### Q176.
Connection acquisition.

---

### Q177.
Commit sequence.

---

### Q178.
Rollback sequence.

---

### Q179.
Synchronization callbacks.

---

### Q180.
PlatformTransactionManager workflow.

---

# 18. Advanced Questions

### Q181.
How does Spring suspend a transaction during REQUIRES_NEW?

---

### Q182.
How does rollback-only propagation work?

---

### Q183.
Why does UnexpectedRollbackException occur?

---

### Q184.
How does transaction synchronization work internally?

---

### Q185.
How does Spring bind EntityManager to the current thread?

---

### Q186.
How does Hibernate synchronize with transaction commits?

---

### Q187.
What happens when multiple TransactionManagers exist?

---

### Q188.
How are nested transactions implemented internally?

---

### Q189.
How do transaction proxies interact with AOP?

---

### Q190.
How do transactions behave in asynchronous methods?

---

# 19. Scenario-Based Questions

### Q191.
A transaction silently doesn't start. What would you investigate?

---

### Q192.
Your `@Transactional` method calls another transactional method in the same class, but the second transaction never starts. Why?

---

### Q193.
A transaction rolls back unexpectedly after catching an exception. Why?

---

### Q194.
A long-running transaction blocks other users. How would you redesign it?

---

### Q195.
Your service updates the database and publishes a Kafka event. How do you guarantee consistency?

---

### Q196.
A payment succeeds but notification fails. Which transaction strategy would you recommend?

---

### Q197.
A deadlock occurs under heavy load. How would you investigate and resolve it?

---

### Q198.
A REQUIRES_NEW transaction commits even though the outer transaction rolls back. Why?

---

### Q199.
You need to update multiple microservices in one business workflow. Would you use XA transactions or Saga? Why?

---

### Q200.
An application experiences connection pool exhaustion because of long-running transactions. How would you diagnose the issue?

---

# 20. Production Experience Questions

### Q201.
Have you debugged transaction rollback issues in production?

---

### Q202.
How do you choose transaction boundaries in service methods?

---

### Q203.
Have you used REQUIRES_NEW in production? Why?

---

### Q204.
How do you prevent deadlocks?

---

### Q205.
How do you monitor long-running transactions?

---

### Q206.
Have you implemented Saga or Outbox patterns?

---

### Q207.
How do you debug transaction propagation issues?

---

### Q208.
Have you optimized read-only transactions?

---

### Q209.
How do you review transactional code during code reviews?

---

### Q210.
What transaction-related production issue taught you the most?

---

# 21. "Why" Questions

### Q211.
Why does Spring use proxies for transaction management?

---

### Q212.
Why don't private methods participate in transactions?

---

### Q213.
Why are RuntimeExceptions rolled back by default?

---

### Q214.
Why are checked exceptions not rolled back by default?

---

### Q215.
Why should transactions remain short-lived?

---

### Q216.
Why should external API calls usually not be inside database transactions?

---

### Q217.
Why is REQUIRES_NEW potentially dangerous?

---

### Q218.
Why is SERIALIZABLE rarely used in high-throughput systems?

---

### Q219.
Why is Saga preferred over XA in microservices?

---

### Q220.
Why is Eventual Consistency acceptable in distributed systems?

---

# 22. Trade-off Questions

### Q221.
Declarative vs Programmatic Transactions.

---

### Q222.
REQUIRED vs REQUIRES_NEW.

---

### Q223.
REQUIRES_NEW vs NESTED.

---

### Q224.
READ_COMMITTED vs REPEATABLE_READ.

---

### Q225.
REPEATABLE_READ vs SERIALIZABLE.

---

### Q226.
Optimistic Locking vs Transactions.

---

### Q227.
Database Transaction vs Distributed Transaction.

---

### Q228.
XA Transactions vs Saga Pattern.

---

### Q229.
Outbox Pattern vs Two-Phase Commit.

---

### Q230.
Read-only Transaction vs Normal Transaction.

---

# 23. Common Interview Follow-up Questions

## If you mention `@Transactional`
- Proxy?
- Self Invocation?
- Private methods?
- Rollback?
- Timeout?

---

## If you mention Propagation
- REQUIRED?
- REQUIRES_NEW?
- NESTED?
- MANDATORY?
- SUPPORTS?

---

## If you mention Isolation
- Dirty Reads?
- Phantom Reads?
- Lost Updates?
- Performance?
- Database defaults?

---

## If you mention Rollback
- RuntimeException?
- Checked Exception?
- rollbackFor?
- rollback-only?
- UnexpectedRollbackException?

---

## If you mention Distributed Transactions
- Saga?
- Outbox?
- XA?
- Eventual Consistency?
- Kafka?

---

## If you mention Performance
- Long-running transactions?
- Deadlocks?
- Lock contention?
- Connection pool?
- Read-only optimization?

---

# Staff Engineer Discussion Questions

### Q231.
How would you define transaction boundaries across hundreds of microservices?

---

### Q232.
How would you balance consistency and availability in distributed systems?

---

### Q233.
How do you review code for transaction anti-patterns?

---

### Q234.
When would you avoid using `@Transactional`?

---

### Q235.
How would you standardize transaction management across teams?

---

### Q236.
How do you design resilient payment workflows without distributed transactions?

---

### Q237.
How do you monitor transaction health in production?

---

### Q238.
What metrics indicate transaction bottlenecks?

---

### Q239.
How would you migrate a monolith using XA transactions to microservices?

---

### Q240.
If you were redesigning Spring's transaction framework today, what would you improve?

---

# Completion Checklist

## Fundamentals
- [ ] ACID Properties
- [ ] Transaction Lifecycle
- [ ] Auto Commit
- [ ] Commit & Rollback
- [ ] Transaction Boundaries

## Spring Transactions
- [ ] PlatformTransactionManager
- [ ] `@Transactional`
- [ ] Transaction Proxy
- [ ] Transaction Interceptor
- [ ] Transaction Synchronization

## Propagation
- [ ] REQUIRED
- [ ] REQUIRES_NEW
- [ ] NESTED
- [ ] SUPPORTS
- [ ] MANDATORY

## Isolation
- [ ] Dirty Read
- [ ] Non-repeatable Read
- [ ] Phantom Read
- [ ] Lost Update
- [ ] Isolation Levels

## Rollback
- [ ] Runtime Exceptions
- [ ] Checked Exceptions
- [ ] rollbackFor
- [ ] noRollbackFor
- [ ] UnexpectedRollbackException

## JPA & Hibernate
- [ ] Persistence Context
- [ ] Dirty Checking
- [ ] Flush
- [ ] EntityManager
- [ ] Open Session in View

## Distributed Systems
- [ ] XA Transactions
- [ ] Saga Pattern
- [ ] Outbox Pattern
- [ ] Eventual Consistency
- [ ] Compensating Transactions

## Production
- [ ] Deadlock Prevention
- [ ] Connection Pool Management
- [ ] Long-running Transactions
- [ ] Monitoring
- [ ] Performance Tuning

## Interview Readiness
- [ ] Can explain Spring transaction internals from proxy creation to commit.
- [ ] Can compare all propagation behaviors with real production scenarios.
- [ ] Can choose appropriate isolation levels based on business requirements.
- [ ] Can debug rollback, self-invocation, and propagation issues.
- [ ] Can discuss distributed transaction patterns (Saga, Outbox, XA) confidently.

---

**Total Questions:** 240
**Recommended Time:** 5–6 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** ACID Properties, `@Transactional`, Transaction Propagation, Isolation Levels, Rollback Rules, Self Invocation, Transaction Proxies, PlatformTransactionManager, Dirty Checking, Saga Pattern, Outbox Pattern, Distributed Transactions