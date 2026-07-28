# Performance Optimization Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with 2–5 Years of Experience
>
> **Focus:** Amazon, Google, Microsoft, Uber, Netflix, LinkedIn, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Meesho, etc.
>
> **Technology Focus:** Java, Spring Boot, JVM, SQL, Redis, Kafka, MongoDB, PostgreSQL, Kubernetes, Microservices
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Performance optimization is one of the most practical SDE-2 interview topics. Companies expect engineers to identify bottlenecks, optimize applications, reduce latency, increase throughput, improve scalability, and make informed trade-offs between performance, reliability, and cost.

---

# Table of Contents

## Part I — Performance Fundamentals
1. Performance Basics
2. Performance Metrics
3. Bottleneck Analysis
4. Profiling
5. Benchmarking

---

## Part II — Java Performance
6. JVM Optimization
7. Garbage Collection
8. Memory Optimization
9. Object Allocation
10. Concurrency Optimization

---

## Part III — Spring Boot Performance
11. Startup Optimization
12. Request Processing
13. Thread Pools
14. Reactive Programming
15. Connection Pooling

---

## Part IV — Database Performance
16. SQL Optimization
17. PostgreSQL Performance
18. MongoDB Performance
19. Indexing
20. Query Optimization

---

## Part V — Caching
21. Redis Optimization
22. Cache Strategies
23. Cache Invalidation
24. Local Cache
25. Distributed Cache

---

## Part VI — Kafka & Messaging
26. Kafka Performance
27. Producer Optimization
28. Consumer Optimization
29. Batch Processing
30. Event Processing

---

## Part VII — Network Performance
31. HTTP Optimization
32. Serialization
33. Compression
34. gRPC
35. Connection Reuse

---

## Part VIII — Distributed Systems Performance
36. Load Balancing
37. Horizontal Scaling
38. Autoscaling
39. Backpressure
40. Rate Limiting

---

## Part IX — Performance Testing
41. Load Testing
42. Stress Testing
43. Profiling Tools
44. Benchmarking
45. Monitoring

---

## Part X — Production Optimization
46. Production Incidents
47. Capacity Planning
48. Cost Optimization
49. Observability
50. Performance Tuning

---

# 1. Performance Fundamentals

## Basic

### Q1.
What is performance optimization?

---

### Q2.
Latency vs Throughput.

---

### Q3.
Response Time vs Processing Time.

---

### Q4.
CPU-bound vs IO-bound applications.

---

### Q5.
What is a bottleneck?

---

### Q6.
How do you identify bottlenecks?

---

### Q7.
What are the common causes of slow applications?

---

### Q8.
How do you measure application performance?

---

### Q9.
What is benchmarking?

---

### Q10.
Microbenchmark vs Macrobenchmark.

---

### Q11.
Warm-up vs Cold Start.

---

### Q12.
Average latency vs P95 vs P99.

---

### Q13.
Why are P99 metrics more important than averages?

---

### Q14.
How do SLAs, SLOs, and SLIs relate to performance?

---

### Q15.
How would you approach optimizing an application?

---

# 2. Java Performance

## Highest Priority

### Q16.
How does object creation impact performance?

---

### Q17.
Stack memory vs Heap memory performance.

---

### Q18.
Primitive vs Wrapper performance.

---

### Q19.
StringBuilder vs StringBuffer vs String.

---

### Q20.
Why is String concatenation inside loops expensive?

---

### Q21.
How does autoboxing affect performance?

---

### Q22.
Escape Analysis.

---

### Q23.
Inlining in JVM.

---

### Q24.
JIT Compilation.

---

### Q25.
Tiered Compilation.

---

### Q26.
Object Pooling.

---

### Q27.
Memory Allocation Rate.

---

### Q28.
GC pauses.

---

### Q29.
Young GC vs Full GC.

---

### Q30.
How would you reduce GC pressure?

---

### Q31.
Memory leaks in Java.

---

### Q32.
CPU profiling tools.

---

### Q33.
Memory profiling tools.

---

### Q34.
JFR (Java Flight Recorder).

---

### Q35.
VisualVM vs JProfiler vs YourKit.

---

### Q36.
Thread contention.

---

### Q37.
False sharing.

---

### Q38.
Lock contention.

---

### Q39.
How do concurrent collections improve performance?

---

### Q40.
Common Java performance mistakes.

---

# 3. Spring Boot Performance

### Q41.
Spring Boot startup optimization.

---

### Q42.
Lazy Initialization.

---

### Q43.
Bean creation overhead.

---

### Q44.
Tomcat thread pool tuning.

---

### Q45.
Undertow vs Tomcat.

---

### Q46.
Connection Pooling.

---

### Q47.
HikariCP tuning.

---

### Q48.
Reactive vs Servlet performance.

---

### Q49.
Blocking vs Non-blocking APIs.

---

### Q50.
Virtual Threads vs Reactive Programming.

---

### Q51.
@ResponseBody optimization.

---

### Q52.
Jackson serialization optimization.

---

### Q53.
Pagination performance.

---

### Q54.
Streaming responses.

---

### Q55.
Spring Boot performance best practices.

---

# 4. Database Performance

## Highest Priority

### Q56.
Why are indexes important?

---

### Q57.
How do indexes improve performance?

---

### Q58.
When do indexes hurt performance?

---

### Q59.
Clustered vs Non-clustered indexes.

---

### Q60.
Covering indexes.

---

### Q61.
Composite indexes.

---

### Q62.
How do you optimize slow SQL queries?

---

### Q63.
N+1 Query Problem.

---

### Q64.
Batch Inserts.

---

### Q65.
Batch Updates.

---

### Q66.
Connection Pool tuning.

---

### Q67.
Read Replicas.

---

### Q68.
Database Partitioning.

---

### Q69.
Database Sharding.

---

### Q70.
How do you profile SQL performance?

---

### Q71.
EXPLAIN plans.

---

### Q72.
Why does SELECT * hurt performance?

---

### Q73.
MongoDB indexing optimization.

---

### Q74.
Redis latency optimization.

---

### Q75.
Database performance best practices.

---

# 5. Caching

### Q76.
When should caching be used?

---

### Q77.
Cache Aside.

---

### Q78.
Read Through Cache.

---

### Q79.
Write Through Cache.

---

### Q80.
Write Behind Cache.

---

### Q81.
Cache TTL tuning.

---

### Q82.
Cache stampede.

---

### Q83.
Cache penetration.

---

### Q84.
Cache avalanche.

---

### Q85.
Distributed caching.

---

### Q86.
Local cache vs Redis.

---

### Q87.
Caffeine vs Redis.

---

### Q88.
Serialization overhead in Redis.

---

### Q89.
Cache hit ratio.

---

### Q90.
Cache optimization best practices.

---

# 6. Kafka Performance

### Q91.
Kafka throughput optimization.

---

### Q92.
Producer batching.

---

### Q93.
Compression.

---

### Q94.
acks configuration.

---

### Q95.
linger.ms tuning.

---

### Q96.
Batch size tuning.

---

### Q97.
Consumer parallelism.

---

### Q98.
Consumer lag.

---

### Q99.
Partition count optimization.

---

### Q100.
Kafka performance best practices.

---

# 7. Network Performance

### Q101.
HTTP Keep-Alive.

---

### Q102.
Connection Pooling.

---

### Q103.
HTTP/2 advantages.

---

### Q104.
gRPC performance.

---

### Q105.
Serialization formats.

---

### Q106.
JSON vs Protobuf.

---

### Q107.
Compression.

---

### Q108.
GZIP vs Brotli.

---

### Q109.
CDN optimization.

---

### Q110.
Network latency optimization.

---

# 8. Distributed Systems Performance

### Q111.
Horizontal Scaling.

---

### Q112.
Vertical Scaling.

---

### Q113.
Autoscaling.

---

### Q114.
Load Balancing.

---

### Q115.
Rate Limiting.

---

### Q116.
Backpressure.

---

### Q117.
Bulkheads.

---

### Q118.
Circuit Breakers.

---

### Q119.
Request batching.

---

### Q120.
Distributed caching optimization.

---

# 9. Performance Testing

### Q121.
Load Testing.

---

### Q122.
Stress Testing.

---

### Q123.
Spike Testing.

---

### Q124.
Soak Testing.

---

### Q125.
Benchmarking.

---

### Q126.
JMH.

---

### Q127.
Apache JMeter.

---

### Q128.
Gatling.

---

### Q129.
Locust.

---

### Q130.
Performance testing best practices.

---

# 10. Production Optimization

### Q131.
How do you investigate a production latency spike?

---

### Q132.
CPU reaches 100%. What do you check?

---

### Q133.
Memory usage suddenly doubles. What do you investigate?

---

### Q134.
GC pauses increase significantly. What could be the reasons?

---

### Q135.
Database becomes the bottleneck. What actions would you take?

---

### Q136.
Kafka consumer lag keeps increasing. How do you debug it?

---

### Q137.
Redis latency suddenly increases. What could be the reasons?

---

### Q138.
Spring Boot service takes 30 seconds to start. How do you optimize it?

---

### Q139.
A Kubernetes deployment slows down after scaling. Why?

---

### Q140.
Describe a real performance optimization you implemented.

---

# 11. Production Experience Questions

### Q141.
Have you optimized a Java application in production?

---

### Q142.
Describe the biggest performance issue you've solved.

---

### Q143.
Have you optimized SQL queries?

---

### Q144.
Have you optimized MongoDB queries?

---

### Q145.
Have you tuned Kafka producers or consumers?

---

### Q146.
Have you optimized Redis usage?

---

### Q147.
How do you profile Spring Boot applications?

---

### Q148.
Have you optimized JVM memory settings?

---

### Q149.
What performance monitoring tools does your team use?

---

### Q150.
What metrics do you continuously monitor?

---

# 12. "Why" Questions

### Q151.
Why is premature optimization discouraged?

---

### Q152.
Why is measuring before optimizing important?

---

### Q153.
Why are indexes not always beneficial?

---

### Q154.
Why are averages misleading for latency?

---

### Q155.
Why are P95 and P99 metrics preferred?

---

### Q156.
Why is connection pooling important?

---

### Q157.
Why is object allocation expensive?

---

### Q158.
Why do unnecessary locks reduce throughput?

---

### Q159.
Why should expensive computations be cached?

---

### Q160.
Why should optimization be data-driven?

---

# 13. Trade-off Questions

### Q161.
Latency vs Throughput.

---

### Q162.
Memory vs CPU.

---

### Q163.
Cache vs Database.

---

### Q164.
Reactive vs Virtual Threads.

---

### Q165.
Redis vs Local Cache.

---

### Q166.
Compression vs CPU usage.

---

### Q167.
Batch Processing vs Real-time Processing.

---

### Q168.
Read Replica vs Sharding.

---

### Q169.
Horizontal vs Vertical Scaling.

---

### Q170.
Performance vs Maintainability.

---

# 14. Common Interview Follow-up Questions

## If you mention JVM Optimization
- Which GC was used?
- Heap size?
- GC logs?
- Memory leaks?
- JFR?

---

## If you mention Database Optimization
- Which indexes?
- Execution plan?
- Query latency?
- Connection pool?
- N+1 issue?

---

## If you mention Redis
- Cache hit ratio?
- TTL?
- Eviction policy?
- Serialization?
- Stampede?

---

## If you mention Kafka
- Consumer lag?
- Batch size?
- Compression?
- Partitions?
- Throughput?

---

## If you mention Spring Boot
- Thread pools?
- HikariCP?
- Reactive?
- Startup time?
- Bean initialization?

---

# Staff Engineer Discussion Questions

### Q171.
How would you optimize a backend platform serving 100 million users?

---

### Q172.
How would you establish performance budgets across engineering teams?

---

### Q173.
How would you design an organization-wide performance benchmarking strategy?

---

### Q174.
How would you reduce cloud infrastructure costs without sacrificing performance?

---

### Q175.
How would you identify performance regressions before production deployments?

---

### Q176.
How would you design dashboards to continuously monitor system performance?

---

### Q177.
How would you optimize JVM settings across hundreds of microservices?

---

### Q178.
How would you establish performance SLAs for different APIs?

---

### Q179.
How would you prioritize optimization work across multiple services?

---

### Q180.
If you were the principal engineer responsible for platform performance, what standards and practices would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Latency
- [ ] Throughput
- [ ] Bottleneck Analysis
- [ ] Benchmarking
- [ ] Profiling

## Java
- [ ] JIT
- [ ] GC Tuning
- [ ] Escape Analysis
- [ ] Memory Optimization
- [ ] Thread Contention

## Spring Boot
- [ ] HikariCP
- [ ] Thread Pools
- [ ] Reactive
- [ ] Startup Optimization
- [ ] Serialization

## Database
- [ ] Indexes
- [ ] EXPLAIN Plans
- [ ] Query Optimization
- [ ] Connection Pooling
- [ ] Sharding

## Caching
- [ ] Redis
- [ ] Cache Patterns
- [ ] TTL
- [ ] Stampede Prevention
- [ ] Cache Hit Ratio

## Kafka
- [ ] Producer Tuning
- [ ] Consumer Tuning
- [ ] Batch Processing
- [ ] Compression
- [ ] Consumer Lag

## Networking
- [ ] HTTP/2
- [ ] gRPC
- [ ] Compression
- [ ] Connection Reuse
- [ ] Serialization

## Production
- [ ] Profiling
- [ ] Load Testing
- [ ] Monitoring
- [ ] Capacity Planning
- [ ] Cost Optimization

## Interview Readiness
- [ ] Can identify bottlenecks using profiling tools.
- [ ] Can optimize JVM, databases, caches, and messaging systems.
- [ ] Can explain real production performance improvements with measurable impact.
- [ ] Can discuss trade-offs between latency, throughput, scalability, and cost.
- [ ] Can design performance optimization strategies for large-scale distributed systems.

---

**Total Questions:** **180**

**Recommended Study Time:** **6–7 Days**

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** JVM Tuning, GC Optimization, JIT Compilation, Thread Pools, HikariCP, SQL Optimization, Indexing, Redis Performance, Kafka Tuning, Connection Pooling, HTTP Performance, Reactive Programming, Profiling, Load Testing, Capacity Planning