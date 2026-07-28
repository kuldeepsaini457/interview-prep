# Spring Data JPA Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Spring Version:** Spring Boot 3.x + Spring Data JPA 3.x
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Spring Data JPA is one of the most frequently asked topics in backend interviews. Interviewers expect candidates to understand not only repositories and annotations but also persistence context, dirty checking, entity lifecycle, transactions, fetching strategies, locking, pagination, specifications, projections, performance tuning, and Spring Data internals.

---

# Table of Contents

1. Spring Data JPA Fundamentals
2. Repository Interfaces
3. CRUD Operations
4. Query Methods
5. JPQL
6. Native Queries
7. Entity Lifecycle
8. Persistence Context
9. Dirty Checking
10. Fetching Strategies
11. Relationships
12. Cascading
13. Locking
14. Transactions
15. Pagination & Sorting
16. Specifications
17. Projections
18. Auditing
19. Performance Optimization
20. Spring Data Internals
21. Advanced Questions
22. Scenario-Based Questions
23. Production Experience
24. Why Questions
25. Trade-offs
26. Common Follow-up Questions

---

# 1. Spring Data JPA Fundamentals

## Basic

### Q1.
What is Spring Data JPA?

**Follow-ups**
- Why was Spring Data JPA introduced?
- What problems does it solve?

---

### Q2.
Difference between JPA, Hibernate, and Spring Data JPA.

---

### Q3.
What is a Repository?

---

### Q4.
What are the advantages of Spring Data JPA?

---

### Q5.
How does Spring Data JPA reduce boilerplate code?

---

### Q6.
How does Spring Data JPA create repository implementations?

---

### Q7.
Can Spring Data JPA work without Hibernate?

---

### Q8.
Can Hibernate work without Spring Data JPA?

---

### Q9.
What dependencies are required for Spring Data JPA?

---

### Q10.
How does Spring Boot auto-configure Spring Data JPA?

---

# 2. Repository Interfaces

## Basic

### Q11.
What is CrudRepository?

---

### Q12.
What is PagingAndSortingRepository?

---

### Q13.
What is JpaRepository?

---

### Q14.
Difference between CrudRepository and JpaRepository.

---

### Q15.
Difference between PagingAndSortingRepository and JpaRepository.

---

### Q16.
How are repository interfaces implemented?

---

### Q17.
Can custom repository methods be added?

---

### Q18.
Repository naming conventions.

---

### Q19.
@Repository annotation.

---

### Q20.
Exception translation in repositories.

---

# 3. CRUD Operations

### Q21.
save().

---

### Q22.
saveAll().

---

### Q23.
findById().

---

### Q24.
getReferenceById().

---

### Q25.
findAll().

---

### Q26.
delete().

---

### Q27.
deleteById().

---

### Q28.
deleteAll().

---

### Q29.
existsById().

---

### Q30.
count().

---

### Q31.
Difference between persist() and save().

---

### Q32.
Difference between save() and saveAndFlush().

---

### Q33.
Difference between delete() and remove().

---

### Q34.
Batch insert operations.

---

### Q35.
Batch delete operations.

---

# 4. Query Methods

## Intermediate

### Q36.
How do derived query methods work?

---

### Q37.
Query creation by method name.

---

### Q38.
findBy vs getBy vs readBy.

---

### Q39.
Common query keywords.

---

### Q40.
findByNameAndAge().

---

### Q41.
findByAgeGreaterThan().

---

### Q42.
findByNameContaining().

---

### Q43.
findByCreatedDateBetween().

---

### Q44.
OrderBy keyword.

---

### Q45.
Distinct keyword.

---

### Q46.
IgnoreCase keyword.

---

### Q47.
Top/First keyword.

---

### Q48.
Exists query methods.

---

### Q49.
Delete query methods.

---

### Q50.
Limitations of derived queries.

---

# 5. JPQL

## Intermediate

### Q51.
What is JPQL?

---

### Q52.
JPQL vs SQL.

---

### Q53.
Entity names vs table names.

---

### Q54.
Selecting entities.

---

### Q55.
Selecting DTOs.

---

### Q56.
Constructor expressions.

---

### Q57.
Named parameters.

---

### Q58.
Positional parameters.

---

### Q59.
JOIN in JPQL.

---

### Q60.
FETCH JOIN.

---

### Q61.
Aggregation functions.

---

### Q62.
GROUP BY.

---

### Q63.
HAVING.

---

### Q64.
Subqueries.

---

### Q65.
Bulk update queries.

---

# 6. Native Queries

### Q66.
When should Native Queries be used?

---

### Q67.
Advantages of Native Queries.

---

### Q68.
Disadvantages of Native Queries.

---

### Q69.
NativeQuery annotation.

---

### Q70.
Mapping native query results.

---

### Q71.
Pagination with Native Queries.

---

### Q72.
Database portability.

---

### Q73.
Stored Procedures.

---

### Q74.
Vendor-specific SQL.

---

### Q75.
Performance considerations.

---

# 7. Entity Lifecycle

## Intermediate

### Q76.
Entity lifecycle states.

---

### Q77.
Transient state.

---

### Q78.
Persistent state.

---

### Q79.
Detached state.

---

### Q80.
Removed state.

---

### Q81.
State transitions.

---

### Q82.
merge().

---

### Q83.
detach().

---

### Q84.
refresh().

---

### Q85.
clear().

---

# 8. Persistence Context

## Advanced

### Q86.
What is Persistence Context?

---

### Q87.
EntityManager.

---

### Q88.
First-Level Cache.

---

### Q89.
Persistence Context vs First-Level Cache.

---

### Q90.
Identity guarantee.

---

### Q91.
flush().

---

### Q92.
Flush modes.

---

### Q93.
clear().

---

### Q94.
detach().

---

### Q95.
Persistence Context lifecycle.

---

# 9. Dirty Checking

### Q96.
What is Dirty Checking?

---

### Q97.
How does Dirty Checking work?

---

### Q98.
When does Dirty Checking occur?

---

### Q99.
Does Dirty Checking require save()?

---

### Q100.
Performance implications.

---

### Q101.
Disabling Dirty Checking.

---

### Q102.
Dirty Checking vs explicit update.

---

### Q103.
Read-only transactions.

---

### Q104.
Entity snapshots.

---

### Q105.
Production considerations.

---

# 10. Fetching Strategies

### Q106.
EAGER fetching.

---

### Q107.
LAZY fetching.

---

### Q108.
Default fetch types.

---

### Q109.
N+1 Query Problem.

---

### Q110.
How to identify N+1 queries.

---

### Q111.
How to solve N+1 queries.

---

### Q112.
JOIN FETCH.

---

### Q113.
Entity Graph.

---

### Q114.
Batch fetching.

---

### Q115.
Open Session in View.

---

# 11. Relationships

### Q116.
One-to-One.

---

### Q117.
One-to-Many.

---

### Q118.
Many-to-One.

---

### Q119.
Many-to-Many.

---

### Q120.
Owning side.

---

### Q121.
mappedBy.

---

### Q122.
JoinColumn.

---

### Q123.
JoinTable.

---

### Q124.
Bidirectional vs Unidirectional.

---

### Q125.
Relationship best practices.

---

# 12. Cascading

### Q126.
Cascade types.

---

### Q127.
CascadeType.ALL.

---

### Q128.
CascadeType.PERSIST.

---

### Q129.
CascadeType.MERGE.

---

### Q130.
CascadeType.REMOVE.

---

### Q131.
CascadeType.REFRESH.

---

### Q132.
CascadeType.DETACH.

---

### Q133.
Orphan Removal.

---

### Q134.
Cascade pitfalls.

---

### Q135.
Production recommendations.

---

# 13. Locking

### Q136.
Optimistic Locking.

---

### Q137.
Pessimistic Locking.

---

### Q138.
@Version.

---

### Q139.
OptimisticLockException.

---

### Q140.
LockModeType.

---

### Q141.
When should Optimistic Locking be used?

---

### Q142.
When should Pessimistic Locking be used?

---

### Q143.
Deadlocks.

---

### Q144.
Retry strategies.

---

### Q145.
Concurrency best practices.

---

# 14. Transactions

### Q146.
How does Spring Data JPA integrate with @Transactional?

---

### Q147.
Repository transaction defaults.

---

### Q148.
Read-only transactions.

---

### Q149.
Transaction propagation.

---

### Q150.
Transaction isolation.

---

### Q151.
Flush before commit.

---

### Q152.
Rollback behavior.

---

### Q153.
Transaction boundaries.

---

### Q154.
Long-running transactions.

---

### Q155.
Transaction best practices.

---

# 15. Pagination & Sorting

### Q156.
Pageable.

---

### Q157.
Page.

---

### Q158.
Slice.

---

### Q159.
Sort.

---

### Q160.
Difference between Page and Slice.

---

### Q161.
Offset pagination.

---

### Q162.
Keyset pagination.

---

### Q163.
Sorting multiple columns.

---

### Q164.
Pagination performance.

---

### Q165.
Production recommendations.

---

# 16. Specifications

### Q166.
What are Specifications?

---

### Q167.
Criteria API.

---

### Q168.
Dynamic Queries.

---

### Q169.
Combining Specifications.

---

### Q170.
AND vs OR Specifications.

---

### Q171.
Reusable Specifications.

---

### Q172.
Specification performance.

---

### Q173.
When to use Specifications.

---

### Q174.
Alternatives to Specifications.

---

### Q175.
Production use cases.

---

# 17. Projections

### Q176.
Interface-based Projections.

---

### Q177.
DTO Projections.

---

### Q178.
Closed Projections.

---

### Q179.
Open Projections.

---

### Q180.
Nested Projections.

---

### Q181.
Constructor Projections.

---

### Q182.
Projection performance.

---

### Q183.
Projection limitations.

---

### Q184.
When to use Projections.

---

### Q185.
Entity vs DTO retrieval.

---

# 18. Auditing

### Q186.
Spring Data Auditing.

---

### Q187.
@EnableJpaAuditing.

---

### Q188.
@CreatedDate.

---

### Q189.
@LastModifiedDate.

---

### Q190.
@CreatedBy.

---

### Q191.
@LastModifiedBy.

---

### Q192.
AuditorAware.

---

### Q193.
Soft Delete.

---

### Q194.
Auditing best practices.

---

### Q195.
Production auditing.

---

# 19. Performance Optimization

### Q196.
Batch inserts.

---

### Q197.
Batch updates.

---

### Q198.
Batch fetching.

---

### Q199.
JDBC batching.

---

### Q200.
Entity Graph.

---

### Q201.
Fetch Join.

---

### Q202.
Second-Level Cache overview.

---

### Q203.
Query Cache.

---

### Q204.
Read-only entities.

---

### Q205.
Performance tuning checklist.

---

# 20. Spring Data Internals

### Q206.
Repository proxy generation.

---

### Q207.
RepositoryFactoryBean.

---

### Q208.
SimpleJpaRepository.

---

### Q209.
QueryLookupStrategy.

---

### Q210.
Derived query parser.

---

### Q211.
Repository fragments.

---

### Q212.
Custom repository implementation.

---

### Q213.
JpaRepositoryFactory.

---

### Q214.
EntityInformation.

---

### Q215.
How Spring Data creates repository beans.

---

# 21. Advanced Questions

### Q216.
How does save() decide between persist() and merge()?

---

### Q217.
How does EntityManager manage entity identity?

---

### Q218.
How does Dirty Checking avoid unnecessary updates?

---

### Q219.
What happens during flush()?

---

### Q220.
How does Spring Data JPA interact with Hibernate Session?

---

### Q221.
How does JPQL translate into SQL?

---

### Q222.
How does query derivation work internally?

---

### Q223.
How are transactions synchronized with Persistence Context?

---

### Q224.
How does Spring Data JPA optimize repeated entity lookups?

---

### Q225.
Performance implications of large Persistence Contexts.

---

# 22. Scenario-Based Questions

### Q226.
Your application suffers from the N+1 query problem. How would you identify and fix it?

---

### Q227.
A transaction updates an entity without calling save(), yet the database is updated. Why?

---

### Q228.
Your application experiences slow pagination on large tables. How would you optimize it?

---

### Q229.
Two users update the same record simultaneously. How would you prevent lost updates?

---

### Q230.
A detached entity causes unexpected behavior. How would you debug it?

---

### Q231.
A repository method derived from its name becomes unreadable. What alternatives would you consider?

---

### Q232.
Your application loads thousands of entities into memory and becomes slow. How would you optimize it?

---

### Q233.
A LazyInitializationException occurs in production. What are the possible causes and solutions?

---

### Q234.
Your REST endpoint returns an entity graph with circular references. How would you redesign it?

---

### Q235.
A batch insert job performs poorly. Which JPA and Hibernate settings would you investigate?

---

# 23. Production Experience Questions

### Q236.
Have you optimized JPA queries in production?

---

### Q237.
How have you solved the N+1 query problem?

---

### Q238.
Have you used Specifications for dynamic searching?

---

### Q239.
How do you decide between JPQL and Native SQL?

---

### Q240.
Have you implemented optimistic locking?

---

### Q241.
How do you monitor SQL generated by Hibernate?

---

### Q242.
Have you configured JDBC batching?

---

### Q243.
How do you manage transactions in service layers?

---

### Q244.
Have you customized repository implementations?

---

### Q245.
What Spring Data JPA issue taught you the most?

---

# 24. "Why" Questions

### Q246.
Why does Spring Data JPA use interfaces instead of concrete repository classes?

---

### Q247.
Why is LAZY loading recommended by default?

---

### Q248.
Why is EAGER fetching dangerous?

---

### Q249.
Why does Dirty Checking improve developer productivity?

---

### Q250.
Why is the Persistence Context important?

---

### Q251.
Why should entities not be returned directly from REST APIs?

---

### Q252.
Why are DTO projections often preferred?

---

### Q253.
Why is optimistic locking preferred over pessimistic locking in most applications?

---

### Q254.
Why are long-running transactions discouraged?

---

### Q255.
Why should business logic avoid EntityManager whenever possible?

---

# 25. Trade-off Questions

### Q256.
JPQL vs Native SQL.

---

### Q257.
CrudRepository vs JpaRepository.

---

### Q258.
Entity vs DTO Projection.

---

### Q259.
LAZY vs EAGER Fetching.

---

### Q260.
Optimistic vs Pessimistic Locking.

---

### Q261.
Page vs Slice.

---

### Q262.
Derived Query vs @Query.

---

### Q263.
Specifications vs QueryDSL.

---

### Q264.
Cascade REMOVE vs Orphan Removal.

---

### Q265.
save() vs saveAndFlush().

---

# 26. Common Interview Follow-up Questions

## If you mention Persistence Context
- First-Level Cache?
- Dirty Checking?
- Flush?
- Detach?
- Clear?

---

## If you mention LAZY Loading
- N+1 problem?
- Fetch Join?
- Entity Graph?
- LazyInitializationException?
- Batch fetching?

---

## If you mention Repositories
- Proxy creation?
- Query derivation?
- Repository fragments?
- Custom repositories?
- Exception translation?

---

## If you mention Transactions
- Dirty Checking?
- Flush?
- Read-only?
- Rollback?
- Isolation?

---

## If you mention Locking
- @Version?
- Retry?
- Deadlocks?
- Lost updates?
- OptimisticLockException?

---

## If you mention Performance
- Batch inserts?
- Entity Graph?
- DTO Projection?
- Query Cache?
- Monitoring SQL?

---

# Staff Engineer Discussion Questions

### Q266.
How would you standardize JPA usage across hundreds of microservices?

---

### Q267.
How do you decide when to bypass Spring Data JPA and write native SQL?

---

### Q268.
How would you review a codebase for JPA performance anti-patterns?

---

### Q269.
How do you minimize database load while maintaining maintainable repository code?

---

### Q270.
How would you design repository abstractions for a large enterprise application?

---

### Q271.
How do you ensure transaction boundaries remain clear across service layers?

---

### Q272.
How do you monitor and optimize JPA performance in production?

---

### Q273.
How would you migrate a legacy JDBC application to Spring Data JPA?

---

### Q274.
How do you educate junior engineers about common JPA pitfalls?

---

### Q275.
If you were redesigning Spring Data JPA today, what improvements would you make?

---

# Completion Checklist

## Fundamentals
- [ ] Spring Data JPA Architecture
- [ ] Repository Interfaces
- [ ] CRUD Operations
- [ ] Query Methods
- [ ] JPQL

## Persistence
- [ ] Entity Lifecycle
- [ ] Persistence Context
- [ ] Dirty Checking
- [ ] EntityManager
- [ ] Flush

## Relationships
- [ ] One-to-One
- [ ] One-to-Many
- [ ] Many-to-One
- [ ] Many-to-Many
- [ ] Cascading

## Performance
- [ ] Fetch Strategies
- [ ] N+1 Problem
- [ ] Batch Processing
- [ ] DTO Projections
- [ ] Entity Graphs

## Transactions
- [ ] Locking
- [ ] Optimistic Locking
- [ ] Pessimistic Locking
- [ ] Transaction Boundaries
- [ ] Rollback

## Advanced
- [ ] Specifications
- [ ] Projections
- [ ] Auditing
- [ ] Repository Internals
- [ ] Query Optimization

## Production
- [ ] SQL Monitoring
- [ ] Performance Tuning
- [ ] Batch Operations
- [ ] Large Dataset Handling
- [ ] Repository Design

## Interview Readiness
- [ ] Can explain the complete entity lifecycle and persistence context.
- [ ] Can diagnose N+1 queries and LazyInitializationException.
- [ ] Can compare JPQL, Native SQL, and derived queries.
- [ ] Can explain Dirty Checking and transaction synchronization.
- [ ] Can discuss Spring Data JPA performance tuning and production best practices.

---

**Total Questions:** 275
**Recommended Time:** 6–7 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** Repository Internals, Entity Lifecycle, Persistence Context, Dirty Checking, Fetch Strategies, N+1 Query Problem, JPQL, Transactions, Locking, Specifications, Projections, Performance Optimization