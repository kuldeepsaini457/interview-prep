# MongoDB Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Google, Uber, LinkedIn, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** MongoDB, Java, Spring Boot, Spring Data MongoDB, Distributed Systems, Microservices
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> MongoDB is one of the most widely used NoSQL databases in backend systems. Interviewers expect candidates to understand document modeling, indexing, replication, sharding, aggregation pipeline, transactions, consistency, performance tuning, and production troubleshooting.

---

# Table of Contents

1. MongoDB Fundamentals
2. MongoDB Architecture
3. Documents & Collections
4. CRUD Operations
5. Indexing
6. Aggregation Pipeline
7. Data Modeling
8. Replication
9. Sharding
10. Transactions & Consistency
11. Performance & Optimization
12. Monitoring & Troubleshooting
13. MongoDB with Spring Boot
14. Advanced MongoDB Concepts
15. Scenario-Based Questions
16. Production Experience
17. Why Questions
18. Trade-offs
19. Common Follow-up Questions

---

# 1. MongoDB Fundamentals

## Basic

### Q1.
What is MongoDB?

**Follow-ups**
- Why was MongoDB introduced?
- What problems does MongoDB solve?

---

### Q2.
MongoDB vs Relational Database.

---

### Q3.
Document-oriented database.

---

### Q4.
Collection vs Table.

---

### Q5.
Document vs Row.

---

### Q6.
BSON.

---

### Q7.
Schema-less database.

---

### Q8.
Advantages of MongoDB.

---

### Q9.
Disadvantages of MongoDB.

---

### Q10.
When should MongoDB be used?

---

### Q11.
When should MongoDB NOT be used?

---

### Q12.
MongoDB architecture overview.

---

### Q13.
Primary use cases.

---

### Q14.
CAP theorem and MongoDB.

---

### Q15.
MongoDB editions.

---

# 2. MongoDB Architecture

## Intermediate

### Q16.
MongoDB architecture.

---

### Q17.
mongod.

---

### Q18.
mongos.

---

### Q19.
Config Servers.

---

### Q20.
Replica Sets.

---

### Q21.
Sharded Clusters.

---

### Q22.
Storage Engine.

---

### Q23.
WiredTiger.

---

### Q24.
Memory management.

---

### Q25.
Journal.

---

### Q26.
Write path.

---

### Q27.
Read path.

---

### Q28.
Storage layout.

---

### Q29.
Database lifecycle.

---

### Q30.
Production architecture.

---

# 3. Documents & Collections

### Q31.
Document structure.

---

### Q32.
Embedded documents.

---

### Q33.
Arrays.

---

### Q34.
ObjectId.

---

### Q35.
Collections.

---

### Q36.
Capped Collections.

---

### Q37.
Time Series Collections.

---

### Q38.
Document size limit.

---

### Q39.
Dynamic schema.

---

### Q40.
Collection best practices.

---

# 4. CRUD Operations

### Q41.
Insert operations.

---

### Q42.
Update operations.

---

### Q43.
Replace operations.

---

### Q44.
Delete operations.

---

### Q45.
find().

---

### Q46.
Projection.

---

### Q47.
Sorting.

---

### Q48.
Pagination.

---

### Q49.
Bulk operations.

---

### Q50.
CRUD best practices.

---

# 5. Indexing

## Highest Priority

### Q51.
What is an Index?

---

### Q52.
Single Field Index.

---

### Q53.
Compound Index.

---

### Q54.
Multikey Index.

---

### Q55.
Text Index.

---

### Q56.
Hashed Index.

---

### Q57.
Geospatial Index.

---

### Q58.
TTL Index.

---

### Q59.
Wildcard Index.

---

### Q60.
Unique Index.

---

### Q61.
Sparse Index.

---

### Q62.
Partial Index.

---

### Q63.
Covered Queries.

---

### Q64.
Explain Plans.

---

### Q65.
Index best practices.

---

# 6. Aggregation Pipeline

## Highest Priority

### Q66.
What is the Aggregation Pipeline?

---

### Q67.
$match.

---

### Q68.
$project.

---

### Q69.
$group.

---

### Q70.
$sort.

---

### Q71.
$limit.

---

### Q72.
$skip.

---

### Q73.
$lookup.

---

### Q74.
$unwind.

---

### Q75.
$facet.

---

### Q76.
$bucket.

---

### Q77.
$set.

---

### Q78.
$merge.

---

### Q79.
Pipeline optimization.

---

### Q80.
Aggregation best practices.

---

# 7. Data Modeling

### Q81.
Embedding vs Referencing.

---

### Q82.
One-to-One relationships.

---

### Q83.
One-to-Many relationships.

---

### Q84.
Many-to-Many relationships.

---

### Q85.
Document design.

---

### Q86.
Denormalization.

---

### Q87.
Schema validation.

---

### Q88.
Bucket Pattern.

---

### Q89.
Outlier Pattern.

---

### Q90.
Subset Pattern.

---

### Q91.
Computed Pattern.

---

### Q92.
Extended Reference Pattern.

---

### Q93.
Attribute Pattern.

---

### Q94.
Data modeling anti-patterns.

---

### Q95.
Production recommendations.

---

# 8. Replication

### Q96.
Replica Set.

---

### Q97.
Primary.

---

### Q98.
Secondary.

---

### Q99.
Arbiter.

---

### Q100.
Election process.

---

### Q101.
Replication lag.

---

### Q102.
Read Preference.

---

### Q103.
Write Concern.

---

### Q104.
Read Concern.

---

### Q105.
High Availability.

---

# 9. Sharding

## Advanced

### Q106.
What is Sharding?

---

### Q107.
Shard Key.

---

### Q108.
Choosing a Shard Key.

---

### Q109.
Range Sharding.

---

### Q110.
Hashed Sharding.

---

### Q111.
Zone Sharding.

---

### Q112.
Chunk migration.

---

### Q113.
Balancer.

---

### Q114.
Config Servers.

---

### Q115.
Sharding best practices.

---

# 10. Transactions & Consistency

### Q116.
Single-document atomicity.

---

### Q117.
Multi-document transactions.

---

### Q118.
ACID support.

---

### Q119.
Transaction lifecycle.

---

### Q120.
Retryable writes.

---

### Q121.
Consistency model.

---

### Q122.
Read Concern levels.

---

### Q123.
Write Concern levels.

---

### Q124.
Distributed transactions.

---

### Q125.
Transaction best practices.

---

# 11. Performance & Optimization

### Q126.
Explain plans.

---

### Q127.
Query Planner.

---

### Q128.
Working Set.

---

### Q129.
Memory optimization.

---

### Q130.
Projection optimization.

---

### Q131.
Aggregation optimization.

---

### Q132.
Slow queries.

---

### Q133.
Connection pooling.

---

### Q134.
Compression.

---

### Q135.
Performance tuning checklist.

---

# 12. Monitoring & Troubleshooting

### Q136.
mongostat.

---

### Q137.
mongotop.

---

### Q138.
Profiler.

---

### Q139.
Slow query logs.

---

### Q140.
Index statistics.

---

### Q141.
Replication monitoring.

---

### Q142.
Sharding monitoring.

---

### Q143.
Memory monitoring.

---

### Q144.
Lock monitoring.

---

### Q145.
Production debugging workflow.

---

# 13. MongoDB with Spring Boot

### Q146.
Spring Data MongoDB.

---

### Q147.
MongoRepository.

---

### Q148.
ReactiveMongoRepository.

---

### Q149.
MongoTemplate.

---

### Q150.
Aggregation with Spring Data.

---

### Q151.
Custom repositories.

---

### Q152.
Transactions in Spring.

---

### Q153.
Optimistic locking.

---

### Q154.
Reactive MongoDB.

---

### Q155.
Production recommendations.

---

# 14. Advanced MongoDB Concepts

### Q156.
Change Streams.

---

### Q157.
TTL Collections.

---

### Q158.
GridFS.

---

### Q159.
Atlas Search.

---

### Q160.
Time Series Collections.

---

### Q161.
Atlas Triggers.

---

### Q162.
Schema Versioning.

---

### Q163.
Queryable Encryption.

---

### Q164.
Field-Level Encryption.

---

### Q165.
Advanced architecture patterns.

---

# 15. Scenario-Based Questions

### Q166.
How would you design a MongoDB schema for an e-commerce platform?

---

### Q167.
A query that was fast becomes slow after data growth. How would you investigate?

---

### Q168.
How would you choose a shard key for a payment service?

---

### Q169.
How would you model Orders and Order Items?

---

### Q170.
A collection grows to billions of documents. How would you scale it?

---

### Q171.
How would you migrate from SQL to MongoDB?

---

### Q172.
How would you optimize a large aggregation pipeline?

---

### Q173.
A replica set continuously re-elects the primary. How would you debug it?

---

### Q174.
How would you store user profiles with dynamic attributes?

---

### Q175.
How would you implement soft delete in MongoDB?

---

### Q176.
How would you optimize pagination for millions of documents?

---

### Q177.
A shard becomes a hotspot. What would you do?

---

### Q178.
How would you troubleshoot replication lag?

---

### Q179.
How would you review MongoDB queries during a code review?

---

### Q180.
How would you optimize Spring Boot applications using MongoDB?

---

# 16. Production Experience Questions

### Q181.
Have you used MongoDB in production?

---

### Q182.
How do you design MongoDB schemas?

---

### Q183.
How do you optimize MongoDB queries?

---

### Q184.
How do you monitor MongoDB performance?

---

### Q185.
Have you implemented sharding?

---

### Q186.
How do you choose shard keys?

---

### Q187.
How do you troubleshoot replication issues?

---

### Q188.
How do you optimize aggregation pipelines?

---

### Q189.
How do you use MongoTemplate in production?

---

### Q190.
What MongoDB-related production incident taught you the most?

---

# 17. "Why" Questions

### Q191.
Why is MongoDB document-oriented instead of relational?

---

### Q192.
Why is embedding often preferred over referencing?

---

### Q193.
Why should shard keys have high cardinality?

---

### Q194.
Why are aggregation pipelines preferred over multiple queries?

---

### Q195.
Why are transactions generally less common in MongoDB?

---

### Q196.
Why is ObjectId a good default identifier?

---

### Q197.
Why is WiredTiger the default storage engine?

---

### Q198.
Why should indexes be carefully designed?

---

### Q199.
Why can excessive denormalization become problematic?

---

### Q200.
Why should large arrays be avoided?

---

# 18. Trade-off Questions

### Q201.
MongoDB vs PostgreSQL.

---

### Q202.
Embedding vs Referencing.

---

### Q203.
Replica Set vs Sharding.

---

### Q204.
Range Sharding vs Hashed Sharding.

---

### Q205.
JSON vs BSON.

---

### Q206.
find() vs Aggregation Pipeline.

---

### Q207.
MongoTemplate vs MongoRepository.

---

### Q208.
Single-document vs Multi-document Transactions.

---

### Q209.
Text Index vs Atlas Search.

---

### Q210.
Dynamic Schema vs Fixed Schema.

---

# 19. Common Interview Follow-up Questions

## If you mention Documents
- BSON?
- ObjectId?
- Embedded documents?
- Arrays?
- Size limit?

---

## If you mention Indexes
- Compound Index?
- Multikey?
- TTL?
- Covered Query?
- Explain Plan?

---

## If you mention Aggregation
- $lookup?
- $group?
- $match?
- $facet?
- Optimization?

---

## If you mention Replication
- Primary?
- Secondary?
- Election?
- Write Concern?
- Read Preference?

---

## If you mention Sharding
- Shard Key?
- Chunk?
- Balancer?
- Config Servers?
- Hotspot?

---

## If you mention Spring Data
- MongoRepository?
- MongoTemplate?
- ReactiveMongoRepository?
- Transactions?
- Aggregation?

---

# Staff Engineer Discussion Questions

### Q211.
How would you design a MongoDB cluster handling billions of documents?

---

### Q212.
How would you establish schema design standards across engineering teams?

---

### Q213.
How would you design an optimal sharding strategy for a global application?

---

### Q214.
How would you migrate hundreds of relational services to MongoDB?

---

### Q215.
How would you review MongoDB data models organization-wide?

---

### Q216.
How would you reduce infrastructure cost while maintaining MongoDB performance?

---

### Q217.
How would you prepare MongoDB for disaster recovery?

---

### Q218.
How would you monitor a large MongoDB deployment?

---

### Q219.
Which MongoDB metrics would you continuously monitor?

---

### Q220.
If you were designing a MongoDB platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] MongoDB Basics
- [ ] BSON
- [ ] Documents
- [ ] Collections
- [ ] CRUD

## Data Modeling
- [ ] Embedding
- [ ] Referencing
- [ ] Schema Design
- [ ] Design Patterns
- [ ] Validation

## Querying
- [ ] Indexes
- [ ] Aggregation Pipeline
- [ ] Explain Plans
- [ ] Projection
- [ ] Pagination

## Scalability
- [ ] Replica Sets
- [ ] Sharding
- [ ] Shard Keys
- [ ] Chunk Migration
- [ ] Balancer

## Transactions
- [ ] ACID
- [ ] Write Concern
- [ ] Read Concern
- [ ] Retryable Writes
- [ ] Consistency

## Performance
- [ ] Working Set
- [ ] Connection Pooling
- [ ] Query Optimization
- [ ] Monitoring
- [ ] Troubleshooting

## Spring Boot
- [ ] MongoRepository
- [ ] MongoTemplate
- [ ] ReactiveMongoRepository
- [ ] Aggregation
- [ ] Transactions

## Interview Readiness
- [ ] Can explain MongoDB architecture and document model.
- [ ] Can design efficient document schemas using embedding and referencing.
- [ ] Can optimize queries with proper indexes and aggregation pipelines.
- [ ] Can design highly available and scalable MongoDB deployments using replica sets and sharding.
- [ ] Can confidently troubleshoot production MongoDB performance and replication issues.

---

**Total Questions:** 220

**Recommended Time:** 6–7 Days

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** Data Modeling, Embedding vs Referencing, Aggregation Pipeline, Indexes, Replica Sets, Sharding, Shard Keys, Write Concern, Read Concern, Transactions, Explain Plans, MongoDB with Spring Boot, Performance Tuning