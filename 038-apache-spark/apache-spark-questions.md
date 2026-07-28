# Apache Spark Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with 2–5 Years of Experience
>
> **Focus:** Amazon, Google, Microsoft, Uber, Netflix, LinkedIn, Adobe, Walmart Global Tech, Databricks, Apple, Airbnb, PhonePe, Razorpay, Flipkart, Swiggy, Meesho, etc.
>
> **Technology Focus:** Apache Spark, Spark SQL, DataFrames, Datasets, RDDs, Structured Streaming, Performance Optimization, Distributed Computing
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority for Data-Intensive Backend Roles)
>
> Apache Spark is the industry standard for large-scale distributed data processing. SDE-2 engineers working on analytics, recommendation systems, reporting, fraud detection, or ETL pipelines are expected to understand Spark internals, distributed execution, optimization, partitioning, joins, memory management, and production troubleshooting.

---

# Table of Contents

## Part I — Spark Fundamentals
1. Big Data Fundamentals
2. Spark Architecture
3. Driver & Executors
4. Cluster Managers
5. Spark Applications

---

## Part II — Core Spark APIs
6. RDD
7. DataFrame
8. Dataset
9. Spark SQL
10. Encoders

---

## Part III — Spark Execution
11. DAG
12. Jobs
13. Stages
14. Tasks
15. Lazy Evaluation

---

## Part IV — Data Processing
16. Transformations
17. Actions
18. Aggregations
19. Joins
20. Window Functions

---

## Part V — Performance Optimization
21. Partitioning
22. Shuffle
23. Broadcast
24. Caching
25. AQE

---

## Part VI — Spark SQL Optimization
26. Catalyst Optimizer
27. Tungsten Engine
28. Query Planning
29. Cost-Based Optimization
30. Predicate Pushdown

---

## Part VII — Structured Streaming
31. Streaming Fundamentals
32. Watermarks
33. Checkpointing
34. Stateful Processing
35. Output Modes

---

## Part VIII — Resource Management
36. Memory Management
37. Executor Tuning
38. Dynamic Allocation
39. Serialization
40. Garbage Collection

---

## Part IX — Production Troubleshooting
41. Performance Tuning
42. Failure Recovery
43. Monitoring
44. Debugging
45. Production Best Practices

---

## Part X — Staff Engineer Discussion
46. Spark Platform
47. Cluster Optimization
48. Multi-Tenant Clusters
49. Cost Optimization
50. Data Platform Architecture

---

# 1. Spark Fundamentals

## Basic

### Q1.
What is Apache Spark?

---

### Q2.
Why was Spark created?

---

### Q3.
Spark vs Hadoop MapReduce.

---

### Q4.
Spark architecture.

---

### Q5.
Driver vs Executor.

---

### Q6.
What is a Spark Application?

---

### Q7.
What are Cluster Managers?

---

### Q8.
Standalone vs YARN vs Kubernetes.

---

### Q9.
What happens when a Spark job starts?

---

### Q10.
What is SparkContext?

---

### Q11.
What is SparkSession?

---

### Q12.
SparkSession vs SQLContext.

---

### Q13.
Spark components.

---

### Q14.
Spark execution flow.

---

### Q15.
Spark best practices.

---

# 2. RDD, DataFrame & Dataset

## Highest Priority

### Q16.
What is an RDD?

---

### Q17.
RDD characteristics.

---

### Q18.
RDD vs DataFrame.

---

### Q19.
DataFrame vs Dataset.

---

### Q20.
Dataset vs RDD.

---

### Q21.
When should RDDs be preferred?

---

### Q22.
Schema inference.

---

### Q23.
Catalyst support.

---

### Q24.
Encoders.

---

### Q25.
Serialization.

---

### Q26.
Creating DataFrames.

---

### Q27.
Creating Datasets.

---

### Q28.
Converting between RDD, Dataset, and DataFrame.

---

### Q29.
Typed vs Untyped APIs.

---

### Q30.
API selection best practices.

---

# 3. Spark Execution Model

## Highest Priority

### Q31.
What is Lazy Evaluation?

---

### Q32.
Transformations vs Actions.

---

### Q33.
Narrow Transformations.

---

### Q34.
Wide Transformations.

---

### Q35.
What is a DAG?

---

### Q36.
Logical Plan.

---

### Q37.
Physical Plan.

---

### Q38.
Jobs.

---

### Q39.
Stages.

---

### Q40.
Tasks.

---

### Q41.
Shuffle boundaries.

---

### Q42.
Stage generation.

---

### Q43.
Task scheduling.

---

### Q44.
Speculative execution.

---

### Q45.
Execution model best practices.

---

# 4. Data Processing

### Q46.
map()

---

### Q47.
flatMap()

---

### Q48.
filter()

---

### Q49.
groupBy()

---

### Q50.
groupByKey() vs reduceByKey().

---

### Q51.
reduce()

---

### Q52.
aggregate()

---

### Q53.
fold()

---

### Q54.
Joins in Spark.

---

### Q55.
Inner Join.

---

### Q56.
Outer Join.

---

### Q57.
Broadcast Join.

---

### Q58.
Sort Merge Join.

---

### Q59.
Shuffle Hash Join.

---

### Q60.
Window Functions.

---

### Q61.
collect_list()

---

### Q62.
collect_set()

---

### Q63.
explode()

---

### Q64.
pivot()

---

### Q65.
Spark SQL best practices.

---

# 5. Performance Optimization

## Highest Priority

### Q66.
Why is shuffle expensive?

---

### Q67.
What causes shuffle?

---

### Q68.
How do you reduce shuffle?

---

### Q69.
repartition() vs coalesce().

---

### Q70.
Partition pruning.

---

### Q71.
Predicate pushdown.

---

### Q72.
Broadcast variables.

---

### Q73.
Broadcast joins.

---

### Q74.
Caching vs Persisting.

---

### Q75.
Storage levels.

---

### Q76.
Adaptive Query Execution (AQE).

---

### Q77.
Skewed joins.

---

### Q78.
Salting technique.

---

### Q79.
Small files problem.

---

### Q80.
How do you optimize Spark jobs?

---

### Q81.
How do you tune partition count?

---

### Q82.
How do you avoid collect()?

---

### Q83.
Serialization optimization.

---

### Q84.
Kryo Serialization.

---

### Q85.
Spark optimization best practices.

---

# 6. Spark SQL Internals

### Q86.
Catalyst Optimizer.

---

### Q87.
Rule-based optimization.

---

### Q88.
Cost-Based Optimizer.

---

### Q89.
Whole-stage code generation.

---

### Q90.
Tungsten Engine.

---

### Q91.
Vectorized execution.

---

### Q92.
EXPLAIN command.

---

### Q93.
Logical Plan vs Physical Plan.

---

### Q94.
Adaptive Query Execution.

---

### Q95.
Spark SQL optimization.

---

# 7. Structured Streaming

### Q96.
What is Structured Streaming?

---

### Q97.
Micro-batch processing.

---

### Q98.
Continuous processing.

---

### Q99.
Output Modes.

---

### Q100.
Append Mode.

---

### Q101.
Complete Mode.

---

### Q102.
Update Mode.

---

### Q103.
Watermarking.

---

### Q104.
Late-arriving data.

---

### Q105.
Checkpointing.

---

### Q106.
State Store.

---

### Q107.
Exactly-once processing.

---

### Q108.
Kafka integration.

---

### Q109.
Streaming joins.

---

### Q110.
Streaming best practices.

---

# 8. Resource Management

### Q111.
Executor memory.

---

### Q112.
Driver memory.

---

### Q113.
Executor cores.

---

### Q114.
Dynamic allocation.

---

### Q115.
Executor sizing.

---

### Q116.
Garbage Collection tuning.

---

### Q117.
Memory fractions.

---

### Q118.
Off-heap memory.

---

### Q119.
Spill to disk.

---

### Q120.
Resource tuning best practices.

---

# 9. Production Experience Questions

### Q121.
Describe your Spark architecture.

---

### Q122.
Have you optimized Spark jobs?

---

### Q123.
Describe the largest dataset you've processed.

---

### Q124.
How do you debug slow Spark jobs?

---

### Q125.
Have you worked with partitioned datasets?

---

### Q126.
How do you optimize joins?

---

### Q127.
How do you monitor Spark applications?

---

### Q128.
How do you deploy Spark on Kubernetes?

---

### Q129.
Describe a production Spark issue you solved.

---

### Q130.
What Spark metrics do you monitor?

---

# 10. Scenario-Based Questions

### Q131.
A Spark job that normally finishes in 10 minutes suddenly takes 45 minutes. How would you investigate?

---

### Q132.
One executor consistently runs much longer than the others. What could be the reason?

---

### Q133.
A join causes an OutOfMemoryError. How would you optimize it?

---

### Q134.
Your Spark job performs excessive shuffling. How would you reduce it?

---

### Q135.
Millions of tiny Parquet files slow down your job. How would you solve this?

---

### Q136.
A Kafka Structured Streaming application falls behind. How would you investigate?

---

### Q137.
A Spark executor repeatedly crashes due to memory pressure. What would you check?

---

### Q138.
How would you optimize a Spark job with severe data skew?

---

### Q139.
A Spark job passes locally but fails in production. How would you debug it?

---

### Q140.
Describe a real production Spark optimization that improved performance.

---

# 11. "Why" Questions

### Q141.
Why is Spark faster than Hadoop MapReduce?

---

### Q142.
Why are DataFrames preferred over RDDs?

---

### Q143.
Why is lazy evaluation important?

---

### Q144.
Why is shuffle expensive?

---

### Q145.
Why should collect() be avoided on large datasets?

---

### Q146.
Why does broadcasting improve join performance?

---

### Q147.
Why is partitioning important?

---

### Q148.
Why is Adaptive Query Execution beneficial?

---

### Q149.
Why should Kryo serialization be preferred in many cases?

---

### Q150.
Why should Spark jobs avoid creating too many small partitions?

---

# 12. Trade-off Questions

### Q151.
RDD vs DataFrame.

---

### Q152.
DataFrame vs Dataset.

---

### Q153.
cache() vs persist().

---

### Q154.
repartition() vs coalesce().

---

### Q155.
Broadcast Join vs Sort Merge Join.

---

### Q156.
Micro-batch vs Continuous Streaming.

---

### Q157.
Memory vs Disk Persistence.

---

### Q158.
Static Allocation vs Dynamic Allocation.

---

### Q159.
Spark SQL vs RDD APIs.

---

### Q160.
Standalone vs Kubernetes deployment.

---

# 13. Common Interview Follow-up Questions

## If you mention Spark SQL
- Catalyst?
- Tungsten?
- EXPLAIN?
- AQE?
- Predicate Pushdown?

---

## If you mention Performance
- Shuffle?
- Broadcast?
- Partition count?
- Data skew?
- Cache?

---

## If you mention Structured Streaming
- Watermarks?
- Checkpointing?
- Exactly-once?
- Output modes?
- Kafka integration?

---

## If you mention Memory
- Executor memory?
- Spill?
- Kryo?
- GC?
- Off-heap?

---

## If you mention Production
- Spark UI?
- Event logs?
- Monitoring?
- Kubernetes?
- Executor failures?

---

# Staff Engineer Discussion Questions

### Q161.
How would you design a Spark platform capable of processing petabytes of data?

---

### Q162.
How would you optimize Spark infrastructure costs across hundreds of daily jobs?

---

### Q163.
How would you establish Spark coding standards across engineering teams?

---

### Q164.
How would you handle multi-tenant Spark clusters with competing workloads?

---

### Q165.
How would you detect performance regressions automatically in Spark pipelines?

---

### Q166.
How would you design observability for thousands of Spark jobs?

---

### Q167.
How would you migrate legacy MapReduce jobs to Spark?

---

### Q168.
How would you optimize Spark for cloud-native Kubernetes deployments?

---

### Q169.
Which Spark metrics would you monitor continuously?

---

### Q170.
If you were responsible for the organization's data platform, what Spark standards and best practices would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Spark Architecture
- [ ] Driver & Executors
- [ ] SparkSession
- [ ] Cluster Managers
- [ ] Application Lifecycle

## Core APIs
- [ ] RDD
- [ ] DataFrame
- [ ] Dataset
- [ ] Spark SQL
- [ ] Encoders

## Execution Model
- [ ] Lazy Evaluation
- [ ] DAG
- [ ] Jobs
- [ ] Stages
- [ ] Tasks

## Performance
- [ ] Shuffle
- [ ] Partitioning
- [ ] Broadcast Join
- [ ] AQE
- [ ] Caching

## Spark SQL
- [ ] Catalyst Optimizer
- [ ] Tungsten
- [ ] Query Plans
- [ ] Predicate Pushdown
- [ ] Cost-Based Optimization

## Streaming
- [ ] Structured Streaming
- [ ] Watermarking
- [ ] Checkpointing
- [ ] Output Modes
- [ ] Kafka Integration

## Resource Management
- [ ] Executor Sizing
- [ ] Memory Tuning
- [ ] Dynamic Allocation
- [ ] Kryo Serialization
- [ ] Spill Management

## Interview Readiness
- [ ] Can explain Spark architecture and distributed execution from Driver to Executors.
- [ ] Can optimize Spark jobs using partitioning, caching, AQE, and join strategies.
- [ ] Can troubleshoot production issues like shuffle bottlenecks, data skew, and memory pressure.
- [ ] Can design efficient batch and streaming data pipelines.
- [ ] Can confidently discuss real production Spark optimizations and performance tuning.

---

**Total Questions:** **170**

**Recommended Study Time:** **6–7 Days**

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority for Data-Intensive Backend Roles)

**Most Frequently Asked Topics:** Spark Architecture, Driver vs Executor, RDD vs DataFrame vs Dataset, Lazy Evaluation, DAG, Shuffle, Partitioning, `repartition()` vs `coalesce()`, Broadcast Join, AQE, Catalyst Optimizer, Structured Streaming, Watermarking, Executor Memory Tuning, Data Skew