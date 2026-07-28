# Apache Kafka Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, LinkedIn, Uber, Google, Adobe, Atlassian, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Zomato, Meesho, etc.
>
> **Kafka Version:** Apache Kafka 3.x+
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Kafka is one of the most frequently asked backend interview topics because it is the backbone of modern event-driven architectures. Interviewers expect candidates to understand Kafka architecture, producers, consumers, partitions, replication, delivery guarantees, transactions, performance tuning, monitoring, and real-world production challenges.

---

# Table of Contents

1. Kafka Fundamentals
2. Kafka Architecture
3. Topics & Partitions
4. Producers
5. Consumers
6. Consumer Groups
7. Offsets
8. Replication & Fault Tolerance
9. Delivery Semantics
10. Kafka Transactions
11. Kafka Streams
12. Schema Management
13. Performance Tuning
14. Monitoring & Operations
15. Spring Kafka
16. Advanced Kafka Concepts
17. Scenario-Based Questions
18. Production Experience
19. Why Questions
20. Trade-offs
21. Common Follow-up Questions

---

# 1. Kafka Fundamentals

## Basic

### Q1.
What is Apache Kafka?

**Follow-ups**
- Why was Kafka created?
- What problems does it solve?

---

### Q2.
What are the core components of Kafka?

---

### Q3.
Kafka vs Traditional Message Queue.

---

### Q4.
Kafka vs RabbitMQ.

---

### Q5.
Event Streaming vs Message Queue.

---

### Q6.
What is an event?

---

### Q7.
What is a topic?

---

### Q8.
What is a partition?

---

### Q9.
What is a broker?

---

### Q10.
Why is Kafka highly scalable?

---

# 2. Kafka Architecture

## Intermediate

### Q11.
Explain Kafka architecture.

---

### Q12.
Broker.

---

### Q13.
Controller.

---

### Q14.
Cluster.

---

### Q15.
Metadata.

---

### Q16.
ZooKeeper (legacy).

---

### Q17.
KRaft mode.

---

### Q18.
Metadata quorum.

---

### Q19.
How does Kafka store data?

---

### Q20.
Log segments.

---

### Q21.
Retention.

---

### Q22.
Compaction.

---

### Q23.
Segment rolling.

---

### Q24.
Broker startup process.

---

### Q25.
Kafka request flow.

---

# 3. Topics & Partitions

### Q26.
Why are topics partitioned?

---

### Q27.
Partitioning strategy.

---

### Q28.
Round-robin partitioning.

---

### Q29.
Key-based partitioning.

---

### Q30.
Custom partitioner.

---

### Q31.
Ordering guarantees.

---

### Q32.
Increasing partition count.

---

### Q33.
Decreasing partition count.

---

### Q34.
Hot partitions.

---

### Q35.
Partition rebalancing.

---

### Q36.
Leader partition.

---

### Q37.
Follower partition.

---

### Q38.
ISR (In-Sync Replicas).

---

### Q39.
Preferred leader.

---

### Q40.
Partition best practices.

---

# 4. Producers

### Q41.
Kafka Producer.

---

### Q42.
Producer workflow.

---

### Q43.
Producer configuration.

---

### Q44.
acks configuration.

---

### Q45.
batch.size.

---

### Q46.
linger.ms.

---

### Q47.
compression.type.

---

### Q48.
max.in.flight.requests.

---

### Q49.
Idempotent producer.

---

### Q50.
Producer retries.

---

### Q51.
Producer interceptors.

---

### Q52.
Producer buffering.

---

### Q53.
Asynchronous sending.

---

### Q54.
Synchronous sending.

---

### Q55.
Producer performance tuning.

---

# 5. Consumers

### Q56.
Kafka Consumer.

---

### Q57.
Consumer workflow.

---

### Q58.
Polling mechanism.

---

### Q59.
Fetch requests.

---

### Q60.
Consumer configuration.

---

### Q61.
max.poll.records.

---

### Q62.
max.poll.interval.ms.

---

### Q63.
session.timeout.ms.

---

### Q64.
heartbeat.interval.ms.

---

### Q65.
Consumer lag.

---

### Q66.
Long processing.

---

### Q67.
Consumer backpressure.

---

### Q68.
Consumer pause/resume.

---

### Q69.
Rebalancing.

---

### Q70.
Consumer best practices.

---

# 6. Consumer Groups

## Advanced

### Q71.
What is a Consumer Group?

---

### Q72.
Group Coordinator.

---

### Q73.
Group membership.

---

### Q74.
Partition assignment.

---

### Q75.
Assignment strategies.

---

### Q76.
Range Assignor.

---

### Q77.
RoundRobin Assignor.

---

### Q78.
Sticky Assignor.

---

### Q79.
Cooperative Sticky Assignor.

---

### Q80.
Consumer group rebalance.

---

### Q81.
Static membership.

---

### Q82.
Rebalance listeners.

---

### Q83.
Scaling consumer groups.

---

### Q84.
Consumer group failures.

---

### Q85.
Production recommendations.

---

# 7. Offsets

### Q86.
What is an offset?

---

### Q87.
Offset commit.

---

### Q88.
Auto commit.

---

### Q89.
Manual commit.

---

### Q90.
commitSync().

---

### Q91.
commitAsync().

---

### Q92.
Offset storage.

---

### Q93.
__consumer_offsets topic.

---

### Q94.
Offset reset.

---

### Q95.
earliest vs latest.

---

### Q96.
Consumer recovery.

---

### Q97.
Duplicate processing.

---

### Q98.
Offset management.

---

### Q99.
Offset retention.

---

### Q100.
Best practices.

---

# 8. Replication & Fault Tolerance

### Q101.
Replication Factor.

---

### Q102.
Leader election.

---

### Q103.
ISR.

---

### Q104.
min.insync.replicas.

---

### Q105.
Unclean leader election.

---

### Q106.
Broker failure.

---

### Q107.
Leader failover.

---

### Q108.
Replica synchronization.

---

### Q109.
High availability.

---

### Q110.
Data durability.

---

# 9. Delivery Semantics

## Advanced

### Q111.
At-most-once delivery.

---

### Q112.
At-least-once delivery.

---

### Q113.
Exactly-once delivery.

---

### Q114.
Idempotent Producer.

---

### Q115.
Transactions.

---

### Q116.
Duplicate messages.

---

### Q117.
Message loss.

---

### Q118.
Retry handling.

---

### Q119.
Ordering guarantees.

---

### Q120.
Production trade-offs.

---

# 10. Kafka Transactions

### Q121.
Kafka Transactions.

---

### Q122.
Transactional Producer.

---

### Q123.
transactional.id.

---

### Q124.
Producer fencing.

---

### Q125.
Exactly-once processing.

---

### Q126.
Read Committed.

---

### Q127.
Read Uncommitted.

---

### Q128.
Transactional Consumers.

---

### Q129.
Failure handling.

---

### Q130.
Transaction best practices.

---

# 11. Kafka Streams

### Q131.
Kafka Streams.

---

### Q132.
Streams vs Consumers.

---

### Q133.
KTable.

---

### Q134.
KStream.

---

### Q135.
GlobalKTable.

---

### Q136.
Windowing.

---

### Q137.
Joins.

---

### Q138.
State Stores.

---

### Q139.
Stream Processing guarantees.

---

### Q140.
Production use cases.

---

# 12. Schema Management

### Q141.
Schema Registry.

---

### Q142.
Avro.

---

### Q143.
Protobuf.

---

### Q144.
JSON Schema.

---

### Q145.
Schema evolution.

---

### Q146.
Backward compatibility.

---

### Q147.
Forward compatibility.

---

### Q148.
Full compatibility.

---

### Q149.
Producer/Consumer compatibility.

---

### Q150.
Production recommendations.

---

# 13. Performance Tuning

### Q151.
Throughput optimization.

---

### Q152.
Latency optimization.

---

### Q153.
Compression.

---

### Q154.
Batching.

---

### Q155.
Large messages.

---

### Q156.
Message size limits.

---

### Q157.
Page cache.

---

### Q158.
Zero-copy.

---

### Q159.
Disk I/O optimization.

---

### Q160.
Performance tuning checklist.

---

# 14. Monitoring & Operations

### Q161.
Consumer lag monitoring.

---

### Q162.
Broker metrics.

---

### Q163.
JMX metrics.

---

### Q164.
Prometheus.

---

### Q165.
Grafana.

---

### Q166.
Disk usage.

---

### Q167.
Retention monitoring.

---

### Q168.
Broker balancing.

---

### Q169.
Topic management.

---

### Q170.
Production troubleshooting.

---

# 15. Spring Kafka

### Q171.
Spring for Apache Kafka.

---

### Q172.
KafkaTemplate.

---

### Q173.
@KafkaListener.

---

### Q174.
ConcurrentKafkaListenerContainerFactory.

---

### Q175.
Acknowledgment modes.

---

### Q176.
Error handlers.

---

### Q177.
RetryTopic.

---

### Q178.
Dead Letter Topic.

---

### Q179.
Seeking offsets.

---

### Q180.
Spring Kafka transactions.

---

# 16. Advanced Kafka Concepts

### Q181.
Log compaction.

---

### Q182.
Retention policies.

---

### Q183.
MirrorMaker.

---

### Q184.
Geo replication.

---

### Q185.
Rack awareness.

---

### Q186.
Tiered storage.

---

### Q187.
Quota management.

---

### Q188.
Kafka Connect.

---

### Q189.
Kafka Connect Source vs Sink.

---

### Q190.
Kafka ecosystem overview.

---

# 17. Scenario-Based Questions

### Q191.
A consumer processes duplicate payment events. How would you guarantee correctness?

---

### Q192.
Your consumer lag keeps increasing under heavy traffic. How would you investigate?

---

### Q193.
One partition receives almost all traffic while others remain idle. How would you redesign the partitioning strategy?

---

### Q194.
A broker crashes during peak traffic. What happens to producers and consumers?

---

### Q195.
How would you migrate a topic from 6 partitions to 12 partitions without breaking ordering guarantees?

---

### Q196.
Your Kafka topic stores billions of events. How would you optimize storage?

---

### Q197.
A consumer repeatedly fails to process a poison message. How would you handle it?

---

### Q198.
How would you implement reliable event publishing from a Spring Boot application using the Outbox Pattern?

---

### Q199.
Your application requires exactly-once processing for financial transactions. How would you design the solution?

---

### Q200.
Kafka throughput suddenly drops after deployment. What metrics and configurations would you investigate first?

---

# 18. Production Experience Questions

### Q201.
Have you designed Kafka-based event-driven systems?

---

### Q202.
How have you optimized producer throughput?

---

### Q203.
How do you minimize consumer lag?

---

### Q204.
Have you implemented idempotent consumers?

---

### Q205.
How do you monitor Kafka clusters in production?

---

### Q206.
How do you handle schema evolution?

---

### Q207.
Have you used Dead Letter Topics?

---

### Q208.
How do you debug Kafka rebalancing issues?

---

### Q209.
How do you perform capacity planning for Kafka?

---

### Q210.
What Kafka production incident taught you the most?

---

# 19. "Why" Questions

### Q211.
Why is Kafka append-only?

---

### Q212.
Why are partitions required for scalability?

---

### Q213.
Why can't Kafka decrease partition count?

---

### Q214.
Why is ordering guaranteed only within a partition?

---

### Q215.
Why is manual offset management preferred for critical applications?

---

### Q216.
Why should producer retries be configured carefully?

---

### Q217.
Why are idempotent producers important?

---

### Q218.
Why is exactly-once semantics difficult to achieve?

---

### Q219.
Why should large messages be avoided?

---

### Q220.
Why is Schema Registry important in enterprise systems?

---

# 20. Trade-off Questions

### Q221.
Kafka vs RabbitMQ.

---

### Q222.
Kafka vs Pulsar.

---

### Q223.
Kafka vs Amazon SQS.

---

### Q224.
REST vs Kafka.

---

### Q225.
Synchronous APIs vs Event Streaming.

---

### Q226.
Auto Commit vs Manual Commit.

---

### Q227.
At-least-once vs Exactly-once.

---

### Q228.
Avro vs JSON.

---

### Q229.
Log Compaction vs Time-based Retention.

---

### Q230.
One Large Topic vs Multiple Small Topics.

---

# 21. Common Interview Follow-up Questions

## If you mention Producers
- acks?
- batching?
- retries?
- idempotency?
- partitioning?

---

## If you mention Consumers
- offsets?
- consumer groups?
- rebalancing?
- lag?
- commits?

---

## If you mention Partitions
- ordering?
- scaling?
- hot partitions?
- leader?
- ISR?

---

## If you mention Reliability
- replication?
- transactions?
- exactly-once?
- retries?
- duplicate handling?

---

## If you mention Spring Kafka
- KafkaTemplate?
- @KafkaListener?
- retry topics?
- DLT?
- transactions?

---

## If you mention Performance
- batching?
- compression?
- page cache?
- zero-copy?
- retention?

---

# Staff Engineer Discussion Questions

### Q231.
How would you design a Kafka architecture capable of processing billions of events per day?

---

### Q232.
How would you determine the optimal number of partitions for a new topic?

---

### Q233.
How would you guarantee reliable event publishing across microservices?

---

### Q234.
How would you standardize Kafka usage across hundreds of engineering teams?

---

### Q235.
How would you design a resilient event-driven payment platform?

---

### Q236.
How would you migrate from synchronous REST communication to Kafka with minimal downtime?

---

### Q237.
How would you review Kafka architecture for scalability bottlenecks?

---

### Q238.
Which Kafka metrics would you monitor continuously, and why?

---

### Q239.
How would you educate junior engineers about Kafka ordering, offsets, and delivery guarantees?

---

### Q240.
If you were redesigning Kafka today, what architectural improvements would you introduce?

---

# Completion Checklist

## Fundamentals
- [ ] Kafka Architecture
- [ ] Brokers
- [ ] Topics
- [ ] Partitions
- [ ] Log Storage

## Producers
- [ ] acks
- [ ] Idempotent Producer
- [ ] Retries
- [ ] Batching
- [ ] Compression

## Consumers
- [ ] Consumer Groups
- [ ] Offsets
- [ ] Manual Commits
- [ ] Rebalancing
- [ ] Consumer Lag

## Reliability
- [ ] Replication
- [ ] ISR
- [ ] Leader Election
- [ ] Transactions
- [ ] Exactly-once Semantics

## Streams
- [ ] Kafka Streams
- [ ] KStream
- [ ] KTable
- [ ] Windowing
- [ ] State Stores

## Spring Kafka
- [ ] KafkaTemplate
- [ ] @KafkaListener
- [ ] Retry Topics
- [ ] Dead Letter Topics
- [ ] Transactions

## Operations
- [ ] Monitoring
- [ ] Schema Registry
- [ ] Capacity Planning
- [ ] Performance Tuning
- [ ] Troubleshooting

## Interview Readiness
- [ ] Can explain Kafka architecture from producer to consumer.
- [ ] Can design scalable topic and partition strategies.
- [ ] Can compare delivery guarantees and offset management approaches.
- [ ] Can troubleshoot consumer lag, rebalancing, and broker failures.
- [ ] Can discuss production Kafka deployments, observability, and event-driven architecture confidently.

---

**Total Questions:** 240
**Recommended Time:** 7–8 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
**Most Frequently Asked Topics:** Kafka Architecture, Producers, Consumers, Consumer Groups, Offsets, Partitions, Replication, ISR, Delivery Semantics, Kafka Transactions, Schema Registry, Spring Kafka, Performance Tuning, Consumer Lag, Rebalancing