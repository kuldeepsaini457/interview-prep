# SQL Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Google, Uber, LinkedIn, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** SQL, PostgreSQL, MySQL, Oracle, SQL Server, Distributed Databases, Spring Boot
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> SQL is one of the most frequently tested topics in backend interviews. Beyond writing queries, interviewers expect candidates to understand joins, indexing, execution plans, transactions, normalization, query optimization, locking, concurrency, window functions, CTEs, and production database troubleshooting.

---

# Table of Contents

1. SQL Fundamentals
2. Data Definition Language (DDL)
3. Data Manipulation Language (DML)
4. Joins
5. Aggregate Functions
6. Group By & Having
7. Subqueries
8. Common Table Expressions (CTEs)
9. Window Functions
10. Constraints & Keys
11. Indexes
12. Transactions & Concurrency
13. Query Optimization
14. Database Design
15. Advanced SQL
16. Scenario-Based Questions
17. Production Experience
18. Why Questions
19. Trade-offs
20. Common Follow-up Questions

---

# 1. SQL Fundamentals

## Basic

### Q1.
What is SQL?

**Follow-ups**
- Why was SQL introduced?
- What problems does SQL solve?

---

### Q2.
Structured vs Semi-Structured vs Unstructured data.

---

### Q3.
Database vs Schema.

---

### Q4.
Table, Row, and Column.

---

### Q5.
Primary Key.

---

### Q6.
Foreign Key.

---

### Q7.
Candidate Key.

---

### Q8.
Alternate Key.

---

### Q9.
Composite Key.

---

### Q10.
Surrogate Key vs Natural Key.

---

### Q11.
NULL values.

---

### Q12.
Data types.

---

### Q13.
SQL command categories.

---

### Q14.
SQL execution order.

---

### Q15.
ANSI SQL vs Vendor-specific SQL.

---

# 2. Data Definition Language (DDL)

### Q16.
CREATE.

---

### Q17.
ALTER.

---

### Q18.
DROP.

---

### Q19.
TRUNCATE.

---

### Q20.
RENAME.

---

### Q21.
Temporary tables.

---

### Q22.
Views.

---

### Q23.
Materialized Views.

---

### Q24.
Sequences.

---

### Q25.
Identity columns.

---

# 3. Data Manipulation Language (DML)

### Q26.
INSERT.

---

### Q27.
UPDATE.

---

### Q28.
DELETE.

---

### Q29.
MERGE (UPSERT).

---

### Q30.
Bulk inserts.

---

### Q31.
Batch updates.

---

### Q32.
RETURNING clause.

---

### Q33.
INSERT INTO SELECT.

---

### Q34.
Soft delete.

---

### Q35.
Best practices.

---

# 4. Joins

## Highest Priority

### Q36.
INNER JOIN.

---

### Q37.
LEFT JOIN.

---

### Q38.
RIGHT JOIN.

---

### Q39.
FULL OUTER JOIN.

---

### Q40.
CROSS JOIN.

---

### Q41.
SELF JOIN.

---

### Q42.
NATURAL JOIN.

---

### Q43.
Equi Join vs Non-Equi Join.

---

### Q44.
Joining multiple tables.

---

### Q45.
Join execution order.

---

### Q46.
Join algorithms.

---

### Q47.
Nested Loop Join.

---

### Q48.
Hash Join.

---

### Q49.
Merge Join.

---

### Q50.
Optimizing joins.

---

# 5. Aggregate Functions

### Q51.
COUNT.

---

### Q52.
SUM.

---

### Q53.
AVG.

---

### Q54.
MIN.

---

### Q55.
MAX.

---

### Q56.
COUNT(*) vs COUNT(column).

---

### Q57.
DISTINCT.

---

### Q58.
Aggregate on NULL values.

---

### Q59.
Multiple aggregates.

---

### Q60.
Aggregate optimization.

---

# 6. GROUP BY & HAVING

### Q61.
GROUP BY.

---

### Q62.
HAVING.

---

### Q63.
WHERE vs HAVING.

---

### Q64.
GROUPING SETS.

---

### Q65.
ROLLUP.

---

### Q66.
CUBE.

---

### Q67.
GROUP BY multiple columns.

---

### Q68.
Grouping performance.

---

### Q69.
Aggregation strategies.

---

### Q70.
Best practices.

---

# 7. Subqueries

### Q71.
Subquery.

---

### Q72.
Correlated Subquery.

---

### Q73.
Scalar Subquery.

---

### Q74.
EXISTS.

---

### Q75.
NOT EXISTS.

---

### Q76.
IN.

---

### Q77.
NOT IN.

---

### Q78.
ANY.

---

### Q79.
ALL.

---

### Q80.
Subquery optimization.

---

# 8. Common Table Expressions (CTEs)

### Q81.
What is a CTE?

---

### Q82.
Recursive CTE.

---

### Q83.
Multiple CTEs.

---

### Q84.
CTE vs Subquery.

---

### Q85.
CTE performance.

---

### Q86.
Hierarchical queries.

---

### Q87.
Recursive traversal.

---

### Q88.
Tree structures.

---

### Q89.
Graph queries.

---

### Q90.
Best practices.

---

# 9. Window Functions

## Advanced

### Q91.
What are Window Functions?

---

### Q92.
OVER clause.

---

### Q93.
PARTITION BY.

---

### Q94.
ORDER BY in window functions.

---

### Q95.
ROW_NUMBER.

---

### Q96.
RANK.

---

### Q97.
DENSE_RANK.

---

### Q98.
NTILE.

---

### Q99.
LAG.

---

### Q100.
LEAD.

---

### Q101.
FIRST_VALUE.

---

### Q102.
LAST_VALUE.

---

### Q103.
Running totals.

---

### Q104.
Moving averages.

---

### Q105.
Window frame clauses.

---

# 10. Constraints & Keys

### Q106.
PRIMARY KEY.

---

### Q107.
FOREIGN KEY.

---

### Q108.
UNIQUE.

---

### Q109.
CHECK.

---

### Q110.
NOT NULL.

---

### Q111.
DEFAULT.

---

### Q112.
ON DELETE CASCADE.

---

### Q113.
ON UPDATE CASCADE.

---

### Q114.
Referential integrity.

---

### Q115.
Constraint best practices.

---

# 11. Indexes

## Highest Priority

### Q116.
What is an Index?

---

### Q117.
Clustered Index.

---

### Q118.
Non-Clustered Index.

---

### Q119.
Composite Index.

---

### Q120.
Covering Index.

---

### Q121.
Unique Index.

---

### Q122.
Partial Index.

---

### Q123.
Bitmap Index.

---

### Q124.
B-Tree Index.

---

### Q125.
Hash Index.

---

### Q126.
Index Selectivity.

---

### Q127.
Index Cardinality.

---

### Q128.
Index Scan vs Table Scan.

---

### Q129.
Index maintenance.

---

### Q130.
Index design best practices.

---

# 12. Transactions & Concurrency

### Q131.
ACID properties.

---

### Q132.
Transaction lifecycle.

---

### Q133.
COMMIT.

---

### Q134.
ROLLBACK.

---

### Q135.
SAVEPOINT.

---

### Q136.
Isolation Levels.

---

### Q137.
Dirty Reads.

---

### Q138.
Non-repeatable Reads.

---

### Q139.
Phantom Reads.

---

### Q140.
Serializable isolation.

---

### Q141.
Locks.

---

### Q142.
Shared Lock.

---

### Q143.
Exclusive Lock.

---

### Q144.
Deadlocks.

---

### Q145.
Optimistic vs Pessimistic locking.

---

# 13. Query Optimization

### Q146.
Execution Plan.

---

### Q147.
EXPLAIN.

---

### Q148.
Cost-based optimizer.

---

### Q149.
Predicate Pushdown.

---

### Q150.
Index usage.

---

### Q151.
Join optimization.

---

### Q152.
Query rewriting.

---

### Q153.
Pagination optimization.

---

### Q154.
Statistics.

---

### Q155.
Slow query troubleshooting.

---

# 14. Database Design

### Q156.
Normalization.

---

### Q157.
First Normal Form (1NF).

---

### Q158.
Second Normal Form (2NF).

---

### Q159.
Third Normal Form (3NF).

---

### Q160.
BCNF.

---

### Q161.
Denormalization.

---

### Q162.
Star Schema.

---

### Q163.
Snowflake Schema.

---

### Q164.
ER Diagrams.

---

### Q165.
Database design best practices.

---

# 15. Advanced SQL

### Q166.
Pivot.

---

### Q167.
Unpivot.

---

### Q168.
Recursive queries.

---

### Q169.
MERGE.

---

### Q170.
JSON support in SQL.

---

### Q171.
Stored Procedures.

---

### Q172.
Functions.

---

### Q173.
Triggers.

---

### Q174.
Views vs Materialized Views.

---

### Q175.
Temporal tables.

---

# 16. Scenario-Based Questions

### Q176.
A query that used to run in milliseconds now takes several minutes. How would you investigate?

---

### Q177.
How would you find duplicate records without using DISTINCT?

---

### Q178.
How would you retrieve the second highest salary?

---

### Q179.
How would you find employees earning more than their managers?

---

### Q180.
How would you identify missing sequence numbers in a table?

---

### Q181.
A table contains hundreds of millions of rows. How would you optimize queries against it?

---

### Q182.
How would you paginate results efficiently?

---

### Q183.
How would you delete duplicate rows while keeping one copy?

---

### Q184.
A transaction frequently deadlocks. How would you investigate?

---

### Q185.
How would you optimize a report containing multiple joins and aggregations?

---

### Q186.
How would you design indexes for an e-commerce Orders table?

---

### Q187.
A batch update locks the entire table. How would you reduce its impact?

---

### Q188.
How would you migrate a normalized schema to improve reporting performance?

---

### Q189.
How would you troubleshoot a slow production database?

---

### Q190.
How would you review SQL queries during a code review?

---

# 17. Production Experience Questions

### Q191.
Have you optimized SQL queries in production?

---

### Q192.
How do you analyze execution plans?

---

### Q193.
How do you identify missing indexes?

---

### Q194.
How do you troubleshoot deadlocks?

---

### Q195.
How do you tune large joins?

---

### Q196.
How do you manage schema migrations?

---

### Q197.
Have you worked with partitioned tables?

---

### Q198.
How do you monitor slow queries?

---

### Q199.
How do you review SQL written by teammates?

---

### Q200.
What SQL-related production incident taught you the most?

---

# 18. "Why" Questions

### Q201.
Why are indexes not created on every column?

---

### Q202.
Why are clustered indexes usually limited?

---

### Q203.
Why can NULL values behave unexpectedly?

---

### Q204.
Why is EXISTS often faster than IN?

---

### Q205.
Why can SELECT * be problematic?

---

### Q206.
Why should transactions remain short?

---

### Q207.
Why is normalization important?

---

### Q208.
Why do window functions outperform some subqueries?

---

### Q209.
Why should execution plans be analyzed before adding indexes?

---

### Q210.
Why are materialized views faster than regular views?

---

# 19. Trade-off Questions

### Q211.
INNER JOIN vs LEFT JOIN.

---

### Q212.
EXISTS vs IN.

---

### Q213.
DELETE vs TRUNCATE vs DROP.

---

### Q214.
Clustered vs Non-Clustered Index.

---

### Q215.
B-Tree vs Hash Index.

---

### Q216.
CTE vs Subquery.

---

### Q217.
Normalization vs Denormalization.

---

### Q218.
View vs Materialized View.

---

### Q219.
Optimistic vs Pessimistic Locking.

---

### Q220.
OFFSET Pagination vs Keyset Pagination.

---

# 20. Common Interview Follow-up Questions

## If you mention Joins
- Hash Join?
- Merge Join?
- Nested Loop Join?
- Join order?
- Index usage?

---

## If you mention Indexes
- B-Tree?
- Cardinality?
- Selectivity?
- Covering index?
- Composite index?

---

## If you mention Transactions
- ACID?
- Isolation?
- Deadlock?
- Locks?
- Rollback?

---

## If you mention Window Functions
- ROW_NUMBER?
- RANK?
- DENSE_RANK?
- LAG?
- LEAD?

---

## If you mention Query Optimization
- EXPLAIN?
- Execution plan?
- Statistics?
- Predicate pushdown?
- Slow queries?

---

## If you mention Database Design
- Normalization?
- BCNF?
- ER diagram?
- Keys?
- Constraints?

---

# Staff Engineer Discussion Questions

### Q221.
How would you design a database schema for billions of records?

---

### Q222.
How would you establish SQL query review standards across engineering teams?

---

### Q223.
How would you optimize a reporting database serving thousands of concurrent users?

---

### Q224.
How would you identify and eliminate organization-wide SQL performance bottlenecks?

---

### Q225.
How would you decide between normalization and denormalization for a large-scale platform?

---

### Q226.
How would you design an indexing strategy for a rapidly growing enterprise database?

---

### Q227.
How would you migrate a legacy database with minimal downtime?

---

### Q228.
How would you standardize database schema evolution across hundreds of microservices?

---

### Q229.
Which SQL metrics would you continuously monitor in production?

---

### Q230.
If you were designing a relational database platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] SQL Basics
- [ ] Keys
- [ ] Constraints
- [ ] NULL Handling
- [ ] SQL Execution Order

## Querying
- [ ] Joins
- [ ] Aggregations
- [ ] GROUP BY
- [ ] HAVING
- [ ] Subqueries

## Advanced SQL
- [ ] CTEs
- [ ] Window Functions
- [ ] Recursive Queries
- [ ] Views
- [ ] Materialized Views

## Performance
- [ ] Indexes
- [ ] Execution Plans
- [ ] Query Optimization
- [ ] Statistics
- [ ] Slow Query Analysis

## Transactions
- [ ] ACID
- [ ] Isolation Levels
- [ ] Locks
- [ ] Deadlocks
- [ ] Concurrency Control

## Database Design
- [ ] Normalization
- [ ] Denormalization
- [ ] ER Modeling
- [ ] Partitioning
- [ ] Schema Design

## Interview Readiness
- [ ] Can write complex SQL queries involving joins, CTEs, and window functions.
- [ ] Can optimize queries using execution plans and indexing strategies.
- [ ] Can explain transactions, locking, and concurrency issues confidently.
- [ ] Can design scalable relational schemas for production systems.
- [ ] Can troubleshoot real-world SQL performance problems.

---

**Total Questions:** 230

**Recommended Time:** 7–8 Days

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** SQL Joins, Window Functions, Indexes, Query Optimization, Execution Plans, Transactions, Isolation Levels, Deadlocks, CTEs, Normalization, Database Design, Pagination, Slow Query Analysis