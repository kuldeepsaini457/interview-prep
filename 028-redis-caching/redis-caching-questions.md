# Redis & Caching Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Google, Uber, LinkedIn, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Technology Focus:** Redis, Spring Boot, Spring Cache, Distributed Systems, Microservices, Performance Optimization
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Redis and caching are among the most frequently asked backend interview topics. Interviewers expect candidates to understand caching strategies, Redis data structures, eviction policies, distributed caching, cache consistency, Redis Cluster, replication, persistence, Pub/Sub, distributed locking, rate limiting, and production troubleshooting.

---

# Table of Contents

1. Caching Fundamentals
2. Redis Fundamentals
3. Redis Architecture
4. Redis Data Structures
5. Caching Strategies
6. Cache Consistency & Invalidation
7. Redis Persistence
8. Replication & High Availability
9. Redis Cluster & Scaling
10. Distributed Locking
11. Redis Pub/Sub & Streams
12. Redis with Spring Boot
13. Performance & Monitoring
14. Advanced Redis Concepts
15. Scenario-Based Questions
16. Production Experience
17. Why Questions
18. Trade-offs
19. Common Follow-up Questions

---

# 1. Caching Fundamentals

## Basic

### Q1.
What is caching?

**Follow-ups**
- Why is caching required?
- What problems does caching solve?

---

### Q2.
Types of caching.

---

### Q3.
Client-side cache vs Server-side cache.

---

### Q4.
Application cache vs Database cache.

---

### Q5.
Local cache vs Distributed cache.

---

### Q6.
In-memory cache vs Disk cache.

---

### Q7.
Benefits of caching.

---

### Q8.
Disadvantages of caching.

---

### Q9.
When should caching be used?

---

### Q10.
When should caching NOT be used?

---

### Q11.
Cache hit.

---

### Q12.
Cache miss.

---

### Q13.
Cache hit ratio.

---

### Q14.
Cache warm-up.

---

### Q15.
Cold cache vs Warm cache.

---

# 2. Redis Fundamentals

## Intermediate

### Q16.
What is Redis?

---

### Q17.
Why is Redis so fast?

---

### Q18.
Redis architecture.

---

### Q19.
Single-threaded execution model.

---

### Q20.
Redis I/O model.

---

### Q21.
Redis memory management.

---

### Q22.
Redis use cases.

---

### Q23.
Redis vs Memcached.

---

### Q24.
Redis vs MongoDB.

---

### Q25.
Redis production architecture.

---

# 3. Redis Architecture

### Q26.
Redis server architecture.

---

### Q27.
Event loop.

---

### Q28.
Networking model.

---

### Q29.
Command execution.

---

### Q30.
Memory allocator.

---

### Q31.
Key expiration.

---

### Q32.
Lazy deletion.

---

### Q33.
Active expiration.

---

### Q34.
Memory fragmentation.

---

### Q35.
Architecture best practices.

---

# 4. Redis Data Structures

## Highest Priority

### Q36.
Strings.

---

### Q37.
Lists.

---

### Q38.
Sets.

---

### Q39.
Sorted Sets (ZSET).

---

### Q40.
Hashes.

---

### Q41.
Bitmaps.

---

### Q42.
HyperLogLog.

---

### Q43.
Streams.

---

### Q44.
Geospatial indexes.

---

### Q45.
Bloom Filters.

---

### Q46.
Which Redis data structure would you choose for a leaderboard?

---

### Q47.
Which Redis data structure is best for session storage?

---

### Q48.
Which Redis data structure supports rate limiting?

---

### Q49.
Memory characteristics of Redis data structures.

---

### Q50.
Data structure best practices.

---

# 5. Caching Strategies

## Highest Priority

### Q51.
Cache Aside (Lazy Loading).

---

### Q52.
Read Through Cache.

---

### Q53.
Write Through Cache.

---

### Q54.
Write Behind Cache.

---

### Q55.
Write Around Cache.

---

### Q56.
Cache invalidation.

---

### Q57.
TTL strategy.

---

### Q58.
Refresh Ahead.

---

### Q59.
Cache warming.

---

### Q60.
Choosing the right caching strategy.

---

# 6. Cache Consistency & Invalidation

### Q61.
Why is cache invalidation difficult?

---

### Q62.
Cache consistency.

---

### Q63.
Strong consistency vs Eventual consistency.

---

### Q64.
TTL-based invalidation.

---

### Q65.
Explicit invalidation.

---

### Q66.
Version-based invalidation.

---

### Q67.
Cache synchronization.

---

### Q68.
Cache coherence.

---

### Q69.
Double delete pattern.

---

### Q70.
Consistency best practices.

---

# 7. Redis Persistence

### Q71.
Why does Redis support persistence?

---

### Q72.
RDB snapshots.

---

### Q73.
AOF (Append Only File).

---

### Q74.
RDB vs AOF.

---

### Q75.
Hybrid persistence.

---

### Q76.
Snapshot intervals.

---

### Q77.
AOF rewrite.

---

### Q78.
Recovery process.

---

### Q79.
Durability trade-offs.

---

### Q80.
Production recommendations.

---

# 8. Replication & High Availability

### Q81.
Master-Replica replication.

---

### Q82.
Replication process.

---

### Q83.
Read replicas.

---

### Q84.
Redis Sentinel.

---

### Q85.
Automatic failover.

---

### Q86.
Replication lag.

---

### Q87.
Consistency during failover.

---

### Q88.
Split-brain scenarios.

---

### Q89.
Sentinel architecture.

---

### Q90.
Production HA best practices.

---

# 9. Redis Cluster & Scaling

## Advanced

### Q91.
Redis Cluster.

---

### Q92.
Hash slots.

---

### Q93.
Sharding.

---

### Q94.
Cluster topology.

---

### Q95.
Cluster rebalancing.

---

### Q96.
Cross-slot operations.

---

### Q97.
Scaling Redis.

---

### Q98.
Horizontal vs Vertical scaling.

---

### Q99.
Large key management.

---

### Q100.
Cluster best practices.

---

# 10. Distributed Locking

### Q101.
Why are distributed locks needed?

---

### Q102.
SET NX EX.

---

### Q103.
Lock expiration.

---

### Q104.
Redlock algorithm.

---

### Q105.
Distributed lock failure scenarios.

---

### Q106.
Lock renewal.

---

### Q107.
Deadlocks.

---

### Q108.
Idempotency with Redis.

---

### Q109.
Leader election.

---

### Q110.
Distributed locking best practices.

---

# 11. Redis Pub/Sub & Streams

### Q111.
Redis Pub/Sub.

---

### Q112.
Publishers.

---

### Q113.
Subscribers.

---

### Q114.
Redis Streams.

---

### Q115.
Consumer Groups.

---

### Q116.
Message acknowledgment.

---

### Q117.
Pending Entries List (PEL).

---

### Q118.
Redis Streams vs Kafka.

---

### Q119.
Redis Pub/Sub vs Streams.

---

### Q120.
Messaging best practices.

---

# 12. Redis with Spring Boot

### Q121.
Spring Data Redis.

---

### Q122.
RedisTemplate.

---

### Q123.
StringRedisTemplate.

---

### Q124.
Spring Cache.

---

### Q125.
@Cacheable.

---

### Q126.
@CachePut.

---

### Q127.
@CacheEvict.

---

### Q128.
CacheManager.

---

### Q129.
Redis serialization.

---

### Q130.
Production recommendations.

---

# 13. Performance & Monitoring

### Q131.
Memory usage analysis.

---

### Q132.
Slow Log.

---

### Q133.
Latency monitoring.

---

### Q134.
Big keys.

---

### Q135.
Hot keys.

---

### Q136.
Memory optimization.

---

### Q137.
Eviction policies.

---

### Q138.
Connection pooling.

---

### Q139.
Monitoring metrics.

---

### Q140.
Performance tuning checklist.

---

# 14. Advanced Redis Concepts

### Q141.
Lua scripting.

---

### Q142.
Redis Functions.

---

### Q143.
Transactions.

---

### Q144.
MULTI/EXEC.

---

### Q145.
WATCH.

---

### Q146.
Pipeline.

---

### Q147.
Pub/Sub scaling.

---

### Q148.
Modules.

---

### Q149.
RedisJSON.

---

### Q150.
RedisSearch.

---

### Q151.
RedisBloom.

---

### Q152.
RedisTimeSeries.

---

### Q153.
RedisGraph (legacy).

---

### Q154.
Redis Enterprise features.

---

### Q155.
Advanced optimization.

---

# 15. Scenario-Based Questions

### Q156.
A frequently accessed database table overloads the database. How would you introduce Redis caching?

---

### Q157.
Users sometimes see stale data after updates. How would you solve the cache consistency issue?

---

### Q158.
Your Redis memory usage reaches 100%. What would you investigate?

---

### Q159.
How would you design session management for millions of concurrent users?

---

### Q160.
How would you implement a distributed rate limiter?

---

### Q161.
How would you design a leaderboard for an online game?

---

### Q162.
How would you prevent cache stampede during traffic spikes?

---

### Q163.
How would you prevent cache penetration caused by invalid requests?

---

### Q164.
How would you prevent cache avalanche after simultaneous TTL expiration?

---

### Q165.
How would you design a distributed lock for inventory reservation?

---

### Q166.
A Redis primary fails unexpectedly. What happens next?

---

### Q167.
How would you migrate from a single Redis instance to Redis Cluster?

---

### Q168.
How would you optimize Spring Cache for a high-traffic API?

---

### Q169.
How would you troubleshoot increasing Redis latency?

---

### Q170.
How would you review Redis usage during a code review?

---

# 16. Production Experience Questions

### Q171.
Have you used Redis in production?

---

### Q172.
Which caching strategy have you implemented?

---

### Q173.
How do you choose cache TTL?

---

### Q174.
How do you invalidate cache entries?

---

### Q175.
Have you implemented Redis Cluster?

---

### Q176.
How do you monitor Redis?

---

### Q177.
How do you troubleshoot cache misses?

---

### Q178.
How do you optimize Redis memory usage?

---

### Q179.
Have you implemented distributed locking?

---

### Q180.
What Redis-related production incident taught you the most?

---

# 17. "Why" Questions

### Q181.
Why is Redis primarily memory-based?

---

### Q182.
Why is Redis faster than traditional databases?

---

### Q183.
Why is cache invalidation considered difficult?

---

### Q184.
Why should cache TTLs be randomized?

---

### Q185.
Why should cache keys follow naming conventions?

---

### Q186.
Why is Cache Aside the most commonly used strategy?

---

### Q187.
Why are Redis transactions different from database transactions?

---

### Q188.
Why should large keys be avoided?

---

### Q189.
Why should hot keys be monitored?

---

### Q190.
Why shouldn't every query be cached?

---

# 18. Trade-off Questions

### Q191.
Redis vs Memcached.

---

### Q192.
Local Cache vs Distributed Cache.

---

### Q193.
Cache Aside vs Read Through.

---

### Q194.
Write Through vs Write Behind.

---

### Q195.
Redis Pub/Sub vs Kafka.

---

### Q196.
Redis Streams vs Kafka.

---

### Q197.
RDB vs AOF.

---

### Q198.
Redis Sentinel vs Redis Cluster.

---

### Q199.
Pipeline vs Transaction.

---

### Q200.
Redis vs Hazelcast.

---

# 19. Common Interview Follow-up Questions

## If you mention Redis
- Single-threaded?
- Persistence?
- Memory model?
- Expiration?
- Replication?

---

## If you mention Caching
- Cache Aside?
- Write Through?
- TTL?
- Invalidation?
- Warm-up?

---

## If you mention Data Structures
- Strings?
- Hashes?
- Lists?
- Sorted Sets?
- Streams?

---

## If you mention Redis Cluster
- Hash slots?
- Sharding?
- Cross-slot?
- Failover?
- Rebalancing?

---

## If you mention Spring Cache
- @Cacheable?
- @CacheEvict?
- RedisTemplate?
- CacheManager?
- Serialization?

---

## If you mention Distributed Locking
- SET NX EX?
- Redlock?
- Lock expiration?
- Deadlock?
- Leader election?

---

# Staff Engineer Discussion Questions

### Q201.
How would you design a caching platform serving billions of requests per day?

---

### Q202.
How would you establish organization-wide cache key standards?

---

### Q203.
How would you decide which services should use Redis and which should not?

---

### Q204.
How would you prevent cache-related outages across hundreds of microservices?

---

### Q205.
How would you design Redis Cluster for global applications?

---

### Q206.
How would you reduce Redis infrastructure costs while maintaining performance?

---

### Q207.
How would you design a multi-region Redis deployment?

---

### Q208.
How would you review caching strategies across engineering teams?

---

### Q209.
Which Redis metrics would you continuously monitor?

---

### Q210.
If you were designing a distributed caching platform today, what architectural principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Caching Basics
- [ ] Redis Architecture
- [ ] Redis Data Structures
- [ ] Memory Model
- [ ] Expiration

## Caching
- [ ] Cache Aside
- [ ] Read Through
- [ ] Write Through
- [ ] Write Behind
- [ ] Cache Invalidation

## Scalability
- [ ] Replication
- [ ] Sentinel
- [ ] Redis Cluster
- [ ] Hash Slots
- [ ] Sharding

## Reliability
- [ ] Persistence
- [ ] RDB
- [ ] AOF
- [ ] Failover
- [ ] Recovery

## Advanced
- [ ] Distributed Locking
- [ ] Redis Streams
- [ ] Pub/Sub
- [ ] Lua Scripting
- [ ] Pipelining

## Spring Boot
- [ ] RedisTemplate
- [ ] Spring Cache
- [ ] @Cacheable
- [ ] CacheManager
- [ ] Serialization

## Performance
- [ ] Hot Keys
- [ ] Big Keys
- [ ] Eviction Policies
- [ ] Monitoring
- [ ] Performance Tuning

## Interview Readiness
- [ ] Can explain Redis architecture and why it is fast.
- [ ] Can choose the appropriate Redis data structure for different use cases.
- [ ] Can design scalable caching strategies with proper invalidation.
- [ ] Can implement distributed locking, rate limiting, and messaging using Redis.
- [ ] Can confidently troubleshoot production Redis performance and consistency issues.

---

**Total Questions:** 210

**Recommended Time:** 6–7 Days

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** Cache Aside Pattern, Cache Invalidation, Redis Data Structures, Redis Cluster, Redis Sentinel, Distributed Locking, Redlock, Redis Streams, Pub/Sub, Persistence (RDB vs AOF), Hot Keys, Cache Stampede, Cache Avalanche, Spring Cache, Redis Performance Tuning