# PostgreSQL Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Google, Uber, LinkedIn, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** PostgreSQL, Java, Spring Boot, JPA, Hibernate, SQL, Distributed Systems
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> PostgreSQL is one of the most popular relational databases used in production systems. Interviewers expect candidates to understand PostgreSQL architecture, MVCC, indexing, query optimization, transactions, locking, partitioning, replication, JSONB, extensions, and production troubleshooting.

---

# Table of Contents

1. PostgreSQL Fundamentals
2. PostgreSQL Architecture
3. Data Types
4. Indexes
5. MVCC & Concurrency
6. Transactions & Locking
7. Query Optimization
8. Partitioning
9. Replication & High Availability
10. JSON & JSONB
11. Extensions
12. Backup & Recovery
13. Monitoring & Performance
14. PostgreSQL with Spring Boot
15. Advanced PostgreSQL Concepts
16. Scenario-Based Questions
17. Production Experience
18. Why Questions
19. Trade-offs
20. Common Follow-up Questions

---

# 1. PostgreSQL Fundamentals

## Basic

### Q1.
What is PostgreSQL?

**Follow-ups**
- Why is PostgreSQL popular?
- What problems does it solve?

---

### Q2.
Features of PostgreSQL.

---

### Q3.
PostgreSQL vs MySQL.

---

### Q4.
PostgreSQL vs Oracle.

---

### Q5.
PostgreSQL vs SQL Server.

---

### Q6.
ACID compliance in PostgreSQL.

---

### Q7.
PostgreSQL architecture overview.

---

### Q8.
When should PostgreSQL be used?

---

### Q9.
When should PostgreSQL NOT be used?

---

### Q10.
Common production use cases.

---

# 2. PostgreSQL Architecture

## Intermediate

### Q11.
PostgreSQL process architecture.

---

### Q12.
Postmaster process.

---

### Q13.
Backend processes.

---

### Q14.
Shared memory.

---

### Q15.
Shared Buffers.

---

### Q16.
WAL (Write Ahead Log).

---

### Q17.
Checkpointer.

---

### Q18.
Background Writer.

---

### Q19.
Autovacuum process.

---

### Q20.
Statistics Collector.

---

### Q21.
Connection lifecycle.

---

### Q22.
Buffer Manager.

---

### Q23.
Storage Manager.

---

### Q24.
Physical file structure.

---

### Q25.
Architecture best practices.

---

# 3. Data Types

### Q26.
Numeric data types.

---

### Q27.
Character data types.

---

### Q28.
Boolean type.

---

### Q29.
Date & Time types.

---

### Q30.
UUID.

---

### Q31.
ENUM.

---

### Q32.
ARRAY.

---

### Q33.
JSON.

---

### Q34.
JSONB.

---

### Q35.
Custom data types.

---

# 4. Indexes

## Highest Priority

### Q36.
How does indexing work in PostgreSQL?

---

### Q37.
B-Tree Index.

---

### Q38.
Hash Index.

---

### Q39.
GIN Index.

---

### Q40.
GiST Index.

---

### Q41.
BRIN Index.

---

### Q42.
SP-GiST Index.

---

### Q43.
Bloom Index.

---

### Q44.
Expression Index.

---

### Q45.
Partial Index.

---

### Q46.
Composite Index.

---

### Q47.
Unique Index.

---

### Q48.
Covering Index (INCLUDE).

---

### Q49.
Index-only Scan.

---

### Q50.
Index maintenance.

---

# 5. MVCC & Concurrency

## Highest Priority

### Q51.
What is MVCC?

---

### Q52.
Why does PostgreSQL use MVCC?

---

### Q53.
Tuple versioning.

---

### Q54.
Transaction IDs (XID).

---

### Q55.
xmin and xmax.

---

### Q56.
Visibility rules.

---

### Q57.
Snapshot isolation.

---

### Q58.
VACUUM.

---

### Q59.
Autovacuum.

---

### Q60.
VACUUM FULL.

---

### Q61.
Dead tuples.

---

### Q62.
Table bloat.

---

### Q63.
HOT updates.

---

### Q64.
Freeze operation.

---

### Q65.
MVCC best practices.

---

# 6. Transactions & Locking

### Q66.
Transaction lifecycle.

---

### Q67.
Isolation Levels.

---

### Q68.
Serializable Snapshot Isolation.

---

### Q69.
Row-level locking.

---

### Q70.
Table-level locking.

---

### Q71.
SELECT FOR UPDATE.

---

### Q72.
SELECT FOR SHARE.

---

### Q73.
NOWAIT.

---

### Q74.
SKIP LOCKED.

---

### Q75.
Deadlocks.

---

### Q76.
Lock monitoring.

---

### Q77.
Optimistic locking.

---

### Q78.
Pessimistic locking.

---

### Q79.
Long-running transactions.

---

### Q80.
Transaction best practices.

---

# 7. Query Optimization

### Q81.
EXPLAIN.

---

### Q82.
EXPLAIN ANALYZE.

---

### Q83.
Sequential Scan.

---

### Q84.
Index Scan.

---

### Q85.
Bitmap Index Scan.

---

### Q86.
Parallel Query.

---

### Q87.
Query Planner.

---

### Q88.
Statistics.

---

### Q89.
ANALYZE command.

---

### Q90.
Cost estimation.

---

### Q91.
Join strategies.

---

### Q92.
Predicate pushdown.

---

### Q93.
CTE optimization.

---

### Q94.
Slow query analysis.

---

### Q95.
Optimization best practices.

---

# 8. Partitioning

### Q96.
Table partitioning.

---

### Q97.
Range partitioning.

---

### Q98.
List partitioning.

---

### Q99.
Hash partitioning.

---

### Q100.
Partition pruning.

---

### Q101.
Local indexes.

---

### Q102.
Global indexes.

---

### Q103.
Partition maintenance.

---

### Q104.
Large table strategies.

---

### Q105.
Partitioning trade-offs.

---

# 9. Replication & High Availability

### Q106.
Streaming Replication.

---

### Q107.
Physical Replication.

---

### Q108.
Logical Replication.

---

### Q109.
Replication Slots.

---

### Q110.
Hot Standby.

---

### Q111.
Synchronous Replication.

---

### Q112.
Asynchronous Replication.

---

### Q113.
Failover.

---

### Q114.
Read Replicas.

---

### Q115.
Replication monitoring.

---

# 10. JSON & JSONB

### Q116.
JSON vs JSONB.

---

### Q117.
JSON operators.

---

### Q118.
JSONB indexing.

---

### Q119.
GIN indexes for JSONB.

---

### Q120.
Nested JSON queries.

---

### Q121.
Updating JSON documents.

---

### Q122.
JSON aggregation.

---

### Q123.
Performance considerations.

---

### Q124.
Production use cases.

---

### Q125.
Best practices.

---

# 11. Extensions

### Q126.
What are PostgreSQL extensions?

---

### Q127.
pg_stat_statements.

---

### Q128.
PostGIS.

---

### Q129.
pgcrypto.

---

### Q130.
UUID extensions.

---

### Q131.
TimescaleDB.

---

### Q132.
Citus.

---

### Q133.
FDW (Foreign Data Wrapper).

---

### Q134.
Extension management.

---

### Q135.
Production recommendations.

---

# 12. Backup & Recovery

### Q136.
pg_dump.

---

### Q137.
pg_restore.

---

### Q138.
Base backup.

---

### Q139.
Point-in-Time Recovery (PITR).

---

### Q140.
WAL archiving.

---

### Q141.
Recovery process.

---

### Q142.
Disaster recovery.

---

### Q143.
Backup strategies.

---

### Q144.
Backup verification.

---

### Q145.
Production recovery planning.

---

# 13. Monitoring & Performance

### Q146.
pg_stat_activity.

---

### Q147.
pg_locks.

---

### Q148.
pg_stat_statements.

---

### Q149.
Connection monitoring.

---

### Q150.
Slow query logging.

---

### Q151.
Connection pooling.

---

### Q152.
PgBouncer.

---

### Q153.
Resource tuning.

---

### Q154.
Memory parameters.

---

### Q155.
Performance tuning checklist.

---

# 14. PostgreSQL with Spring Boot

### Q156.
Spring Data PostgreSQL integration.

---

### Q157.
Hibernate dialect.

---

### Q158.
Connection pools (HikariCP).

---

### Q159.
Batch inserts.

---

### Q160.
Transaction management.

---

### Q161.
Optimistic locking.

---

### Q162.
Pessimistic locking.

---

### Q163.
Native SQL queries.

---

### Q164.
JSONB mapping.

---

### Q165.
Production recommendations.

---

# 15. Advanced PostgreSQL Concepts

### Q166.
Declarative partitioning.

---

### Q167.
Materialized Views.

---

### Q168.
Recursive queries.

---

### Q169.
Generated columns.

---

### Q170.
Full-text search.

---

### Q171.
Triggers.

---

### Q172.
Stored Procedures.

---

### Q173.
LISTEN / NOTIFY.

---

### Q174.
Foreign Data Wrappers.

---

### Q175.
Advanced tuning.

---

# 16. Scenario-Based Questions

### Q176.
A PostgreSQL query suddenly becomes slow in production. How would you investigate?

---

### Q177.
Autovacuum is not keeping up with updates. What would you do?

---

### Q178.
A table grows to billions of rows. How would you redesign it?

---

### Q179.
How would you design indexes for an Orders table handling millions of transactions per day?

---

### Q180.
A transaction causes frequent deadlocks. How would you troubleshoot it?

---

### Q181.
Your application requires high read throughput. How would you design replication?

---

### Q182.
How would you migrate a MySQL application to PostgreSQL?

---

### Q183.
JSONB queries become slow over time. How would you optimize them?

---

### Q184.
How would you implement zero-downtime PostgreSQL upgrades?

---

### Q185.
A production database experiences severe table bloat. How would you recover?

---

### Q186.
How would you perform PITR after accidental data deletion?

---

### Q187.
How would you scale PostgreSQL horizontally?

---

### Q188.
How would you troubleshoot connection exhaustion?

---

### Q189.
How would you review PostgreSQL queries during a code review?

---

### Q190.
How would you optimize batch processing using PostgreSQL?

---

# 17. Production Experience Questions

### Q191.
Have you used PostgreSQL in production?

---

### Q192.
How do you optimize PostgreSQL queries?

---

### Q193.
How do you monitor PostgreSQL performance?

---

### Q194.
How do you tune Autovacuum?

---

### Q195.
Have you configured replication?

---

### Q196.
How do you perform backups?

---

### Q197.
How do you troubleshoot deadlocks?

---

### Q198.
How do you optimize JSONB queries?

---

### Q199.
How do you manage PostgreSQL upgrades?

---

### Q200.
What PostgreSQL-related production incident taught you the most?

---

# 18. "Why" Questions

### Q201.
Why does PostgreSQL use MVCC instead of read locks?

---

### Q202.
Why is WAL written before data pages?

---

### Q203.
Why is Autovacuum critical?

---

### Q204.
Why can excessive indexing hurt performance?

---

### Q205.
Why is JSONB usually preferred over JSON?

---

### Q206.
Why are HOT updates beneficial?

---

### Q207.
Why should long-running transactions be avoided?

---

### Q208.
Why does PostgreSQL accumulate dead tuples?

---

### Q209.
Why should connection pooling be used?

---

### Q210.
Why is EXPLAIN ANALYZE preferred over guessing query performance?

---

# 19. Trade-off Questions

### Q211.
PostgreSQL vs MySQL.

---

### Q212.
JSON vs JSONB.

---

### Q213.
GIN vs GiST.

---

### Q214.
B-Tree vs BRIN.

---

### Q215.
Streaming Replication vs Logical Replication.

---

### Q216.
Synchronous vs Asynchronous Replication.

---

### Q217.
VACUUM vs VACUUM FULL.

---

### Q218.
Partitioning vs Sharding.

---

### Q219.
MVCC vs Lock-based concurrency.

---

### Q220.
Connection Pooling vs Direct Connections.

---

# 20. Common Interview Follow-up Questions

## If you mention MVCC
- xmin?
- xmax?
- Visibility?
- Snapshot?
- Dead tuples?

---

## If you mention WAL
- Crash recovery?
- Replication?
- PITR?
- WAL archiving?
- Checkpoint?

---

## If you mention Indexes
- B-Tree?
- GIN?
- BRIN?
- Partial Index?
- Covering Index?

---

## If you mention Replication
- Physical?
- Logical?
- Failover?
- Replication slots?
- Hot standby?

---

## If you mention JSONB
- Operators?
- Indexes?
- Performance?
- Aggregation?
- Nested queries?

---

## If you mention Performance
- EXPLAIN ANALYZE?
- Autovacuum?
- PgBouncer?
- Statistics?
- Slow queries?

---

# Staff Engineer Discussion Questions

### Q221.
How would you design a PostgreSQL architecture supporting billions of records?

---

### Q222.
How would you establish PostgreSQL tuning standards across engineering teams?

---

### Q223.
How would you design a high-availability PostgreSQL platform?

---

### Q224.
How would you reduce database costs while maintaining performance?

---

### Q225.
How would you review indexing strategies across hundreds of services?

---

### Q226.
How would you prepare PostgreSQL for disaster recovery?

---

### Q227.
How would you scale PostgreSQL for global applications?

---

### Q228.
How would you standardize database migrations organization-wide?

---

### Q229.
Which PostgreSQL metrics would you continuously monitor?

---

### Q230.
If you were designing a PostgreSQL platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] PostgreSQL Basics
- [ ] Architecture
- [ ] Data Types
- [ ] WAL
- [ ] MVCC

## Performance
- [ ] Indexes
- [ ] EXPLAIN ANALYZE
- [ ] Query Planner
- [ ] Statistics
- [ ] Optimization

## Concurrency
- [ ] Transactions
- [ ] Isolation Levels
- [ ] Locks
- [ ] MVCC
- [ ] Deadlocks

## Storage
- [ ] VACUUM
- [ ] Autovacuum
- [ ] Table Bloat
- [ ] HOT Updates
- [ ] Partitioning

## High Availability
- [ ] Streaming Replication
- [ ] Logical Replication
- [ ] Read Replicas
- [ ] Failover
- [ ] PITR

## Advanced Features
- [ ] JSONB
- [ ] Extensions
- [ ] Materialized Views
- [ ] Full-text Search
- [ ] LISTEN / NOTIFY

## Production
- [ ] Monitoring
- [ ] PgBouncer
- [ ] Backup & Recovery
- [ ] Performance Tuning
- [ ] Troubleshooting

## Interview Readiness
- [ ] Can explain PostgreSQL architecture and MVCC from first principles.
- [ ] Can optimize queries using execution plans and advanced indexes.
- [ ] Can troubleshoot production issues involving locks, deadlocks, and table bloat.
- [ ] Can design highly available PostgreSQL deployments with replication and PITR.
- [ ] Can confidently discuss PostgreSQL performance tuning and operational best practices.

---

**Total Questions:** 230

**Recommended Time:** 7–8 Days

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** MVCC, WAL, Autovacuum, Index Types (B-Tree, GIN, BRIN), Query Optimization, EXPLAIN ANALYZE, Replication, Partitioning, JSONB, Connection Pooling, PITR, PostgreSQL Performance Tuning