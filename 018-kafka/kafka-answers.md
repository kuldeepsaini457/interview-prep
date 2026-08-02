## Q1. What is Apache Kafka?

### Answer

Apache Kafka is a distributed event streaming platform used to publish, store, and consume streams of events at high throughput with low latency. It is designed to build scalable, fault-tolerant, and event-driven systems.

The key idea is that producers write events to Kafka topics, and consumers read them independently. Kafka persists events on disk, so multiple consumers can process the same data at different times without affecting each other.

Unlike traditional message queues, Kafka retains data for a configurable period instead of deleting it immediately after consumption. This makes it suitable for use cases like event-driven microservices, log aggregation, real-time analytics, and data pipelines.

From a backend perspective, Kafka is commonly used to decouple services. For example, when an order is placed, the Order Service publishes an `OrderCreated` event, while services like Notification, Inventory, and Analytics consume it asynchronously.

### Expected Follow-up Questions

* Why was Kafka created?
* What problems does Kafka solve?
* Kafka vs RabbitMQ?
* What is an event?
* How does Kafka guarantee scalability?

### Common Mistakes

* Calling Kafka just a message queue.
* Saying Kafka deletes messages immediately after consumers read them.
* Assuming consumers own the data instead of Kafka.

### Important Interview Keywords

* Event Streaming
* Publish-Subscribe
* Distributed Log
* High Throughput
* Fault Tolerance
* Event-Driven Architecture

---

## Q2. What are the core components of Kafka?

### Answer

The core components of Kafka are:

* **Producer** – Publishes events to Kafka topics.
* **Topic** – A logical category where events are stored.
* **Partition** – A topic is divided into partitions for scalability and parallelism.
* **Broker** – A Kafka server that stores partitions and serves client requests.
* **Consumer** – Reads events from topics.
* **Consumer Group** – Multiple consumers working together to process partitions in parallel.
* **Controller** – Manages cluster metadata and leader election.
* **Replication** – Keeps copies of partitions across brokers for fault tolerance.

These components work together to provide scalable, durable, and fault-tolerant event processing.

### Expected Follow-up Questions

* What is a broker?
* Why are partitions needed?
* What is a consumer group?
* What is the controller?
* What is ISR?

### Common Mistakes

* Confusing topics with partitions.
* Assuming each consumer gets every message regardless of consumer groups.

### Important Interview Keywords

* Producer
* Consumer
* Topic
* Partition
* Broker
* Consumer Group
* Controller
* Replication

---

## Q3. Kafka vs Traditional Message Queue

### Answer

The biggest difference is that Kafka is designed for event streaming, while traditional message queues are designed for reliable message delivery.

In Kafka:

* Messages are persisted on disk for a configurable retention period.
* Consumers track their own offsets.
* Multiple consumer groups can independently read the same events.
* It is optimized for very high throughput.

In a traditional message queue:

* Messages are typically removed once acknowledged.
* The queue manages message consumption.
* It is better suited for task distribution and work queues.

Kafka is generally preferred for event-driven architectures, audit logs, analytics pipelines, and streaming systems, whereas traditional queues are often used for background jobs and task processing.

### Expected Follow-up Questions

* Kafka vs RabbitMQ?
* Event Streaming vs Message Queue?
* Why doesn't Kafka delete messages after consumption?

### Common Mistakes

* Saying Kafka replaces every message queue.
* Ignoring that different messaging systems solve different problems.

### Important Interview Keywords

* Event Streaming
* Retention
* Offset
* Consumer Groups
* Work Queue

---

## Q4. Kafka vs RabbitMQ

### Answer

Kafka and RabbitMQ solve different problems.

Kafka is optimized for high-throughput event streaming, while RabbitMQ is optimized for reliable message routing and task queues.

| Kafka                                | RabbitMQ                              |
| ------------------------------------ | ------------------------------------- |
| Event streaming platform             | Message broker                        |
| Stores events for a retention period | Removes messages after acknowledgment |
| Very high throughput                 | Lower throughput but flexible routing |
| Partition-based scalability          | Queue-based scalability               |
| Pull-based consumers                 | Push-based consumers                  |

For microservices that publish business events consumed by multiple services, Kafka is usually the better choice.

For workflows requiring complex routing, request-reply patterns, or work queues, RabbitMQ is often a better fit.

### Expected Follow-up Questions

* When would you choose RabbitMQ?
* Can both be used together?
* Kafka vs SQS?

### Common Mistakes

* Saying Kafka is always better.
* Ignoring RabbitMQ's routing capabilities.

### Important Interview Keywords

* Event Streaming
* Work Queue
* Publish-Subscribe
* Routing
* Throughput

---

## Q5. Event Streaming vs Message Queue

### Answer

In event streaming, events are stored and can be consumed multiple times by different consumer groups.

In a message queue, a message is typically processed once and then removed after acknowledgment.

Event streaming is ideal when multiple independent systems need the same data. For example, an `OrderCreated` event may be consumed by Inventory, Billing, Analytics, and Notifications.

Message queues are ideal when a task should be processed by only one worker, such as image processing or email sending.

The main difference is that event streaming focuses on distributing immutable events, while message queues focus on distributing work.

### Expected Follow-up Questions

* Why does Kafka retain messages?
* Can Kafka be used as a queue?
* What is replay?

### Common Mistakes

* Treating event streaming and work queues as identical.
* Assuming replay is possible in all messaging systems.

### Important Interview Keywords

* Event Streaming
* Replay
* Consumer Groups
* Immutable Events
* Work Distribution

---

## Q6. What is an event?

### Answer

An event is an immutable record describing something that happened in the system.

It typically contains:

* A key (optional)
* A value (business data)
* Timestamp
* Headers (optional)

For example:

```text
OrderCreated
{
  orderId: 123,
  customerId: 45,
  amount: 500
}
```

Events represent facts that have already occurred and should not be modified. Producers publish events, and consumers react to them independently.

### Expected Follow-up Questions

* What is an event key?
* Why should events be immutable?
* Event vs Command?

### Common Mistakes

* Treating events as commands.
* Updating existing events instead of creating new ones.

### Important Interview Keywords

* Immutable
* Key
* Value
* Timestamp
* Business Event

---

## Q7. What is a topic?

### Answer

A topic is a logical category where Kafka stores related events.

For example:

* `orders`
* `payments`
* `shipments`

Producers publish events to a topic, and consumers subscribe to it.

Internally, a topic is divided into one or more partitions. Kafka stores events in append-only logs within these partitions.

Topics help organize data but do not themselves provide scalability—partitions do.

### Expected Follow-up Questions

* Why are topics partitioned?
* Can multiple producers write to the same topic?
* How is data stored inside a topic?

### Common Mistakes

* Thinking a topic stores data in a single file.
* Confusing topics with partitions.

### Important Interview Keywords

* Topic
* Append-Only Log
* Producer
* Consumer
* Partition

---

## Q8. What is a partition?

### Answer

A partition is an ordered, append-only log that stores a subset of a topic's events.

Kafka partitions topics to achieve horizontal scalability and parallel processing.

Each partition maintains message order independently. Producers write to the partition leader, and consumers read from it using offsets.

For example, if a topic has six partitions, up to six consumers in the same consumer group can process data in parallel.

### Production Considerations

Increasing partitions improves throughput but changes key-to-partition mapping for new messages, which can affect ordering guarantees for the same key if not planned carefully.

### Expected Follow-up Questions

* Why are partitions needed?
* How does Kafka choose a partition?
* Is ordering guaranteed?
* Can partitions be decreased?

### Common Mistakes

* Saying Kafka guarantees ordering across the entire topic.
* Assuming more partitions always improve performance.

### Important Interview Keywords

* Partition
* Parallelism
* Ordering
* Offset
* Leader Partition

---

## Q9. What is a broker?

### Answer

A broker is a Kafka server that stores topic partitions and handles requests from producers and consumers.

A Kafka cluster typically consists of multiple brokers. Partitions are distributed across them, and each partition has one leader responsible for handling reads and writes.

Brokers also replicate partition data to other brokers for fault tolerance.

### Production Considerations

Using multiple brokers improves scalability, load distribution, and high availability. If one broker fails, leadership can move to another in-sync replica.

### Expected Follow-up Questions

* What is a Kafka cluster?
* How does leader election work?
* What happens if a broker crashes?

### Common Mistakes

* Assuming a broker stores every partition.
* Confusing a broker with the entire Kafka cluster.

### Important Interview Keywords

* Broker
* Cluster
* Leader
* Replica
* Fault Tolerance

---

## Q10. Why is Kafka highly scalable?

### Answer

Kafka is highly scalable because it distributes data and workload across multiple brokers and partitions.

Its scalability comes from several design choices:

* **Partitioning** enables parallel reads and writes.
* **Multiple brokers** allow horizontal scaling by adding more servers.
* **Consumer groups** allow parallel message processing.
* **Sequential disk writes** and an append-only log provide high throughput.
* **Replication** improves availability without sacrificing scalability.

As traffic grows, we typically increase the number of brokers and partitions to handle higher throughput.

### Trade-offs

Increasing partitions improves scalability but can increase operational complexity, rebalance time, and affect ordering guarantees if partitioning strategy is not considered carefully.

### Expected Follow-up Questions

* Why are partitions required?
* How do consumer groups scale?
* What limits Kafka scalability?
* How do you decide the number of partitions?

### Common Mistakes

* Saying scalability comes only from adding brokers.
* Ignoring the role of partitions and consumer groups.

### Important Interview Keywords

* Horizontal Scaling
* Partitioning
* Consumer Groups
* Throughput
* Append-Only Log
* Replication


## Q11. Explain Kafka architecture.

### Answer

Kafka follows a distributed architecture where producers publish events to topics, brokers store them, and consumers read them independently.

The high-level flow is:

```text
Producer
    │
    ▼
Kafka Broker Cluster
    │
    ├── Topic
    │      ├── Partition 0
    │      ├── Partition 1
    │      └── Partition 2
    │
    ▼
Consumer Group
    ├── Consumer A
    ├── Consumer B
    └── Consumer C
```

Here's how it works:

* **Producers** publish events to a topic.
* Each **topic** is divided into **partitions**.
* Partitions are distributed across multiple **brokers**.
* Every partition has one **leader** and zero or more **followers**.
* Consumers read messages using **offsets**.
* Consumers in the same **consumer group** divide partitions among themselves for parallel processing.
* The **controller** manages cluster metadata and leader elections.

This architecture provides horizontal scalability, fault tolerance, and high throughput.

### Expected Follow-up Questions

* What is a broker?
* What is a controller?
* How does leader election work?
* Why are partitions required?

### Common Mistakes

* Saying producers send data directly to consumers.
* Ignoring the role of partitions in scalability.

### Important Interview Keywords

* Broker Cluster
* Topic
* Partition
* Producer
* Consumer Group
* Leader Replica
* Offset

---

## Q12. Broker.

### Answer

A broker is a Kafka server responsible for storing topic partitions and handling requests from producers and consumers.

Each broker can host many partitions from different topics. Producers send data to the leader partition on a broker, and consumers fetch data from that leader.

Brokers also replicate partition data to follower replicas on other brokers to provide fault tolerance.

In a Kafka cluster, data is distributed across brokers, allowing the system to scale horizontally by simply adding more brokers.

### Production Considerations

A healthy cluster balances partitions across brokers to avoid hotspots and ensure even resource utilization.

### Expected Follow-up Questions

* What happens when a broker fails?
* How are partitions assigned to brokers?
* What is leader election?

### Common Mistakes

* Thinking one broker stores all topic data.
* Confusing a broker with a Kafka cluster.

### Important Interview Keywords

* Broker
* Partition
* Leader
* Replica
* Cluster

---

## Q13. Controller.

### Answer

The controller is the broker responsible for managing the Kafka cluster's metadata and coordinating administrative operations.

Its primary responsibilities include:

* Electing partition leaders.
* Detecting broker failures.
* Reassigning leadership after failures.
* Managing topic and partition metadata.

Only one controller is active at a time. If it fails, another broker is elected as the new controller automatically.

The controller does **not** handle normal producer or consumer traffic. It only manages cluster coordination.

### Expected Follow-up Questions

* How is the controller elected?
* What happens if the controller crashes?
* What changed in KRaft mode?

### Common Mistakes

* Saying every broker acts as the controller simultaneously.
* Thinking producers communicate directly with the controller.

### Important Interview Keywords

* Controller
* Leader Election
* Metadata
* Broker Failure
* Cluster Coordination

---

## Q14. Cluster.

### Answer

A Kafka cluster is a group of brokers working together to provide scalable and fault-tolerant event streaming.

Data is distributed across brokers using partitions, and replicas are placed on different brokers to survive failures.

Clients view the cluster as a single Kafka system, while internally the brokers coordinate metadata, leader elections, and replication.

As traffic grows, new brokers can be added to the cluster to increase storage capacity and throughput.

### Production Considerations

A production cluster should have multiple brokers and an appropriate replication factor to avoid a single point of failure.

### Expected Follow-up Questions

* How do brokers communicate?
* What happens when a broker joins or leaves?
* How does Kafka scale?

### Common Mistakes

* Assuming a cluster is just multiple independent brokers.
* Ignoring replication across brokers.

### Important Interview Keywords

* Kafka Cluster
* Broker
* Replication
* Horizontal Scaling
* Fault Tolerance

---

## Q15. Metadata.

### Answer

Metadata is the information Kafka maintains about the cluster rather than the actual event data.

It includes details such as:

* Topics
* Partitions
* Partition leaders
* Replica assignments
* ISR (In-Sync Replicas)
* Brokers
* Controller information

Clients fetch metadata before producing or consuming messages so they know which broker is the leader for each partition.

Metadata changes whenever brokers fail, leaders change, or topics and partitions are created or modified.

### Expected Follow-up Questions

* Who stores metadata?
* How do clients obtain metadata?
* What happens when metadata changes?

### Common Mistakes

* Confusing metadata with message data.
* Assuming clients contact every broker for every request.

### Important Interview Keywords

* Metadata
* Leader
* Partition
* ISR
* Broker Discovery

---

## Q16. ZooKeeper (legacy).

### Answer

In older Kafka versions, ZooKeeper was used to coordinate the Kafka cluster.

Its responsibilities included:

* Controller election.
* Broker registration.
* Cluster metadata management.
* Detecting broker failures.

Kafka brokers communicated with ZooKeeper to maintain cluster state.

However, ZooKeeper added operational complexity because it was a separate distributed system that also needed to be deployed and managed.

Starting with newer Kafka versions, ZooKeeper has been replaced by **KRaft mode**, where Kafka manages its own metadata internally.

### Expected Follow-up Questions

* Why was ZooKeeper removed?
* What is KRaft mode?
* Does Kafka still require ZooKeeper?

### Common Mistakes

* Saying modern Kafka always requires ZooKeeper.
* Confusing ZooKeeper with message storage.

### Important Interview Keywords

* ZooKeeper
* Controller Election
* Metadata
* Broker Registration
* Legacy Architecture

---

## Q17. KRaft mode.

### Answer

KRaft (Kafka Raft) is the modern architecture where Kafka manages its own metadata without requiring ZooKeeper.

Instead of relying on an external system, Kafka uses the Raft consensus protocol to maintain cluster metadata across dedicated controller nodes.

The benefits are:

* Simpler deployment.
* Fewer components to manage.
* Faster controller failover.
* Better scalability.
* Reduced operational overhead.

KRaft is the recommended deployment model for Kafka 3.x and later.

### Expected Follow-up Questions

* What is the metadata quorum?
* How does Raft work?
* KRaft vs ZooKeeper?

### Common Mistakes

* Saying KRaft changes how messages are stored.
* Assuming all brokers become controllers.

### Important Interview Keywords

* KRaft
* Raft Consensus
* Metadata
* Controller Quorum
* ZooKeeper Replacement

---

## Q18. Metadata quorum.

### Answer

The metadata quorum is the group of controller nodes in KRaft mode that collectively maintain Kafka's cluster metadata.

These controllers use the Raft consensus protocol to ensure metadata changes are committed only after receiving agreement from a majority of the quorum.

This prevents split-brain scenarios and ensures consistent cluster metadata even if some controller nodes fail.

Normal producer and consumer traffic does not go through the metadata quorum—it is only responsible for metadata management.

### Expected Follow-up Questions

* Why is a quorum required?
* What happens if a controller fails?
* How does Raft achieve consistency?

### Common Mistakes

* Confusing metadata quorum with ISR.
* Thinking all brokers participate in metadata voting.

### Important Interview Keywords

* Metadata Quorum
* Raft
* Majority Consensus
* Controller Nodes
* High Availability

---

## Q19. How does Kafka store data?

### Answer

Kafka stores data as an append-only log on disk.

Each topic is divided into partitions, and every partition is stored as a sequence of log files called segments.

When a producer sends a message, Kafka appends it to the end of the partition log and assigns it a sequential offset.

Messages are not updated in place. They remain on disk until they expire based on the configured retention policy or are removed by log compaction.

This append-only design enables sequential disk writes, which is one of the main reasons Kafka achieves high throughput.

### Expected Follow-up Questions

* What are log segments?
* What is retention?
* What is log compaction?
* Why is Kafka append-only?

### Common Mistakes

* Thinking Kafka stores data in a database.
* Assuming consumed messages are immediately deleted.

### Important Interview Keywords

* Append-Only Log
* Partition
* Offset
* Log Segment
* Sequential Writes

---

## Q20. Log segments.

### Answer

A log segment is a portion of a partition's append-only log stored as a separate file on disk.

Instead of storing an entire partition in one continuously growing file, Kafka splits it into multiple segment files.

When the active segment reaches a configured size or age, Kafka rolls over to a new segment. Older segments become read-only.

Using segments makes retention and log compaction efficient because Kafka can delete or compact entire segment files instead of scanning one massive log.

### Production Considerations

Segment size and rolling configuration affect recovery time, retention efficiency, and disk management. Extremely small segments increase file overhead, while very large segments can delay cleanup and recovery.

### Expected Follow-up Questions

* What is segment rolling?
* How does retention work?
* How does log compaction work?

### Common Mistakes

* Thinking each message is stored in a separate file.
* Confusing partitions with log segments.

### Important Interview Keywords

* Log Segment
* Segment Rolling
* Append-Only Log
* Retention
* Log Compaction

## Q21. Retention.

### Answer

Retention defines **how long Kafka keeps messages** before deleting them. It is independent of whether consumers have read the messages.

Kafka supports two primary retention policies:

* **Time-based retention** – Keep data for a configured duration (e.g., 7 days).
* **Size-based retention** – Keep data until the topic reaches a configured size limit.

When the retention policy is exceeded, Kafka deletes **old log segments**, not individual messages.

This allows consumers to replay historical events as long as the data is still retained.

### Production Considerations

Retention should be configured based on business requirements. Longer retention enables replay and recovery but requires more disk space.

### Expected Follow-up Questions

* Does Kafka delete messages after consumption?
* How is retention different from log compaction?
* How are old messages deleted?

### Common Mistakes

* Saying messages are deleted immediately after consumers read them.
* Confusing retention with offset retention.

### Important Interview Keywords

* Retention Policy
* Time-based Retention
* Size-based Retention
* Log Segments
* Replay

---

## Q22. Compaction.

### Answer

Log compaction is a retention strategy where Kafka keeps **only the latest value for each message key** instead of keeping every historical event.

For example:

```text
Key=A → Balance=100
Key=A → Balance=200
Key=A → Balance=300
```

After compaction:

```text
Key=A → Balance=300
```

Compaction is useful when consumers need the **latest state** rather than the complete event history.

Typical use cases include:

* User profiles
* Product catalog
* Configuration data
* Account balances

Unlike time-based retention, compaction is based on **message keys**, not message age.

### Production Considerations

Log compaction runs in the background and is not immediate. Multiple versions of the same key may exist until compaction occurs.

### Expected Follow-up Questions

* Retention vs log compaction?
* Can a topic use both?
* Why are message keys required?

### Common Mistakes

* Thinking compaction keeps only the latest message in the topic.
* Assuming compaction happens instantly.

### Important Interview Keywords

* Log Compaction
* Message Key
* Latest State
* Background Cleaner
* Stateful Data

---

## Q23. Segment rolling.

### Answer

Segment rolling is the process of closing the current active log segment and creating a new one.

Kafka rolls a segment when it reaches configured limits such as:

* Maximum segment size
* Maximum segment age

Once rolled:

* The old segment becomes read-only.
* New messages are written to the new active segment.

Segment rolling makes retention and compaction efficient because Kafka operates on complete segment files instead of one continuously growing file.

### Production Considerations

Choosing the right segment size is important. Very small segments increase file management overhead, while very large segments can delay retention cleanup and recovery.

### Expected Follow-up Questions

* What triggers segment rolling?
* Why doesn't Kafka use one large file?
* How does rolling affect retention?

### Common Mistakes

* Thinking rolling means deleting old data.
* Confusing segment rolling with partition creation.

### Important Interview Keywords

* Segment Rolling
* Active Segment
* Read-only Segment
* Retention
* Log Segments

---

## Q24. Broker startup process.

### Answer

When a Kafka broker starts, it performs several initialization steps before serving client requests.

The typical startup sequence is:

1. Load configuration.
2. Start networking and internal services.
3. Recover partition logs from disk.
4. Register with the cluster.
5. Load metadata and determine partition leadership.
6. Start replication for follower partitions.
7. Begin accepting producer and consumer requests.

In KRaft mode, the broker communicates with the metadata quorum instead of ZooKeeper to obtain cluster metadata.

### Production Considerations

Recovery time depends on the number of partitions, log segments, and unclean shutdowns. Proper shutdowns help reduce startup time.

### Expected Follow-up Questions

* What happens after a broker crash?
* How does leader election occur?
* How are partitions reassigned?

### Common Mistakes

* Assuming brokers immediately become leaders for all partitions.
* Ignoring metadata synchronization during startup.

### Important Interview Keywords

* Broker Startup
* Metadata
* Leader Election
* Log Recovery
* KRaft

---

## Q25. Kafka request flow.

### Answer

The request flow depends on whether the client is producing or consuming data.

For a **producer**:

```text
Producer
    ↓
Fetch Metadata
    ↓
Identify Partition Leader
    ↓
Send Record
    ↓
Leader Writes to Log
    ↓
Replicate to Followers (if required)
    ↓
Acknowledgment Returned
```

For a **consumer**:

```text
Consumer
    ↓
Join Consumer Group
    ↓
Receive Partition Assignment
    ↓
Poll Leader Broker
    ↓
Fetch Records
    ↓
Process Records
    ↓
Commit Offset
```

Kafka clients communicate directly with the broker that is the leader for the target partition.

### Expected Follow-up Questions

* What is `acks`?
* How does polling work?
* What are offsets?
* How are partitions selected?

### Common Mistakes

* Thinking all requests go through the controller.
* Assuming consumers receive pushed messages.

### Important Interview Keywords

* Metadata
* Partition Leader
* Poll
* Offset Commit
* Replication

---

## Q26. Why are topics partitioned?

### Answer

Topics are partitioned to enable **horizontal scalability, parallel processing, and higher throughput**.

Without partitions, all reads and writes would go through a single log, creating a bottleneck.

Partitions allow:

* Multiple producers to write concurrently.
* Multiple consumers in the same consumer group to process data in parallel.
* Distribution of data across multiple brokers.

Ordering is guaranteed **within a partition**, not across the entire topic.

### Production Considerations

The number of partitions should be chosen carefully. Too few can limit throughput, while too many increase metadata, file handles, and rebalance overhead.

### Expected Follow-up Questions

* How many partitions should a topic have?
* Is ordering guaranteed?
* Can partitions be increased later?

### Common Mistakes

* Saying partitions exist only for storage.
* Claiming Kafka guarantees ordering across the whole topic.

### Important Interview Keywords

* Horizontal Scaling
* Parallelism
* Throughput
* Ordering
* Consumer Groups

---

## Q27. Partitioning strategy.

### Answer

A partitioning strategy determines **which partition a message is written to**.

The common strategies are:

* **Key-based partitioning** – Messages with the same key always go to the same partition.
* **Round-robin partitioning** – Messages are distributed evenly when no key is provided.
* **Custom partitioning** – Application-specific logic determines the partition.

The choice depends on whether you prioritize **ordering** or **load balancing**.

### Production Considerations

For business events where ordering per entity is important, key-based partitioning is usually preferred.

### Expected Follow-up Questions

* How does Kafka hash the key?
* When should a custom partitioner be used?
* What causes hot partitions?

### Common Mistakes

* Randomly choosing keys without considering distribution.
* Using a constant key for all messages.

### Important Interview Keywords

* Partitioner
* Key-based
* Round-robin
* Load Balancing
* Ordering

---

## Q28. Round-robin partitioning.

### Answer

Round-robin partitioning distributes messages evenly across all available partitions when **no message key is provided**.

For example, with three partitions:

```text
Message1 → P0
Message2 → P1
Message3 → P2
Message4 → P0
```

This provides good load distribution and high throughput.

However, since related messages can go to different partitions, **ordering is not guaranteed** for those messages.

### Trade-offs

* **Pros:** Even distribution, avoids hotspots.
* **Cons:** No ordering guarantee for related events.

### Expected Follow-up Questions

* When does Kafka use round-robin?
* Why is ordering lost?
* How is this different from key-based partitioning?

### Common Mistakes

* Expecting ordering across all messages.
* Using round-robin when per-entity ordering is required.

### Important Interview Keywords

* Round-robin
* Even Distribution
* Throughput
* No Key
* Load Balancing

---

## Q29. Key-based partitioning.

### Answer

In key-based partitioning, Kafka hashes the **message key** to determine the target partition.

As long as the number of partitions remains the same, messages with the same key always go to the same partition.

For example:

```text
Customer-101 → Partition 2
Customer-101 → Partition 2
Customer-101 → Partition 2
```

This guarantees ordering for events belonging to that key, making it the preferred strategy for business entities such as orders, users, or accounts.

### Production Considerations

Choose keys with high cardinality to distribute traffic evenly. Poor key selection can create hot partitions.

### Expected Follow-up Questions

* How does Kafka calculate the partition?
* What happens if partitions increase?
* What are hot partitions?

### Common Mistakes

* Assuming ordering is guaranteed across different keys.
* Using low-cardinality keys that overload one partition.

### Important Interview Keywords

* Message Key
* Hashing
* Ordering
* Hot Partition
* Partitioner

---

## Q30. Custom partitioner.

### Answer

A custom partitioner allows applications to implement their own logic for selecting the target partition instead of using Kafka's default strategy.

It's useful when partitioning depends on business rules rather than just the message key.

For example:

* Route premium customers to dedicated partitions.
* Partition by geographic region.
* Partition by tenant in a multi-tenant system.

A custom partitioner should maintain a balanced distribution while preserving any required ordering guarantees.

### Trade-offs

A custom partitioner provides flexibility but increases complexity. Poor partitioning logic can lead to uneven load and hot partitions.

### Expected Follow-up Questions

* When should you use a custom partitioner?
* How do you avoid hot partitions?
* Can you preserve ordering with a custom partitioner?

### Common Mistakes

* Writing custom logic when the default key-based partitioner is sufficient.
* Ignoring load distribution while implementing business-specific routing.

### Important Interview Keywords

* Custom Partitioner
* Business Rules
* Load Balancing
* Ordering
* Hot Partitions

## Q31. Ordering guarantees.

### Answer

Kafka guarantees **message ordering only within a single partition**, not across an entire topic.

If all events for the same business entity (for example, an `orderId` or `customerId`) are sent with the same key, Kafka hashes that key to the same partition. Consumers will then read those events in the exact order they were written.

For example:

```text
Order-101 Created
Order-101 Paid
Order-101 Shipped
```

If all three events go to the same partition, consumers will always process them in this order.

However, if related events are distributed across different partitions, Kafka cannot guarantee their relative ordering.

### Production Considerations

For workflows where ordering matters, always use a stable partition key. Also, avoid increasing the partition count without understanding its impact on future message routing.

### Expected Follow-up Questions

* Why is ordering guaranteed only within a partition?
* Does retry affect ordering?
* What happens after increasing partitions?

### Common Mistakes

* Saying Kafka guarantees ordering across the entire topic.
* Not using a key when ordering is required.

### Important Interview Keywords

* Ordering Guarantee
* Partition
* Message Key
* Sequential Log
* Offset

---

## Q32. Increasing partition count.

### Answer

Kafka allows increasing the number of partitions to improve scalability and parallelism.

New messages are distributed across the new partition set, while existing messages remain in their original partitions.

The main impact is that **key-to-partition mapping changes for future messages** because the hash is calculated over the new partition count.

As a result, future events for the same key may be routed to a different partition, so ordering is only preserved within the old and new partitions separately.

### Production Considerations

Increase partitions only when additional throughput or consumer parallelism is needed. If per-key ordering is critical, plan partition increases carefully.

### Trade-offs

* **Pros:** Higher throughput and consumer parallelism.
* **Cons:** Existing data is not redistributed automatically, and future ordering for a key may be affected.

### Expected Follow-up Questions

* Why can't Kafka rebalance existing messages?
* Does increasing partitions move old data?
* How do you migrate safely?

### Common Mistakes

* Assuming existing messages are automatically redistributed.
* Assuming ordering is unaffected.

### Important Interview Keywords

* Partition Scaling
* Hashing
* Throughput
* Parallelism
* Ordering

---

## Q33. Decreasing partition count.

### Answer

Kafka does **not support decreasing the number of partitions** for an existing topic.

Reducing partitions would require moving messages from multiple partitions into fewer partitions while preserving offsets and ordering, which Kafka cannot do safely.

If fewer partitions are required, the common approach is:

1. Create a new topic with the desired partition count.
2. Copy or republish the data.
3. Migrate producers and consumers.
4. Decommission the old topic.

### Production Considerations

Choose the initial partition count carefully because reducing it later requires migration.

### Expected Follow-up Questions

* Why can't Kafka merge partitions?
* How do you migrate to fewer partitions?
* Does increasing partitions have the same limitation?

### Common Mistakes

* Saying Kafka supports both increasing and decreasing partitions.
* Ignoring ordering and offset challenges.

### Important Interview Keywords

* Partition Migration
* Ordering
* Offset
* Topic Migration
* Immutable Partition Layout

---

## Q34. Hot partitions.

### Answer

A hot partition is a partition that receives significantly more traffic than others, creating an uneven workload.

Common causes include:

* Using a low-cardinality key, such as `country`.
* Using a constant key for all messages.
* Poor custom partitioning logic.

Hot partitions can lead to:

* Higher producer latency.
* Increased consumer lag.
* Uneven broker resource utilization.

The preferred solution is to choose a partition key with high cardinality so data is distributed more evenly.

### Production Considerations

Monitor partition-level throughput and consumer lag to identify hot partitions early.

### Expected Follow-up Questions

* How do you detect hot partitions?
* How can you redesign the partition key?
* Can adding partitions fix the problem?

### Common Mistakes

* Using business keys with very few distinct values.
* Assuming more partitions alone solve uneven traffic.

### Important Interview Keywords

* Hot Partition
* Key Distribution
* Consumer Lag
* Throughput
* High Cardinality

---

## Q35. Partition rebalancing.

### Answer

Partition rebalancing is the process of redistributing partitions across consumers in a consumer group when group membership changes.

A rebalance happens when:

* A consumer joins the group.
* A consumer leaves or crashes.
* The number of partitions changes.

During a rebalance:

1. Consumers temporarily stop processing.
2. Kafka redistributes partitions.
3. Consumers resume processing with their new assignments.

This ensures each partition is owned by only one consumer within a consumer group.

### Production Considerations

Frequent rebalances reduce throughput because consumers pause processing. Features like **Cooperative Sticky Assignor** and **static membership** help minimize disruption.

### Expected Follow-up Questions

* What triggers a rebalance?
* How can rebalances be reduced?
* What are assignment strategies?

### Common Mistakes

* Thinking rebalancing moves partition data.
* Assuming consumers continue processing during every rebalance.

### Important Interview Keywords

* Rebalance
* Consumer Group
* Partition Assignment
* Group Coordinator
* Cooperative Sticky Assignor

---

## Q36. Leader partition.

### Answer

Every Kafka partition has one **leader replica** and zero or more follower replicas.

The leader replica is responsible for:

* Handling all producer writes.
* Serving consumer read requests.
* Coordinating replication to followers.

Neither producers nor consumers communicate directly with follower replicas under normal operation.

If the leader fails, Kafka elects a new leader from the In-Sync Replicas (ISR).

### Expected Follow-up Questions

* What is ISR?
* How is a new leader selected?
* Why don't consumers read from followers?

### Common Mistakes

* Thinking every replica accepts writes.
* Confusing broker leadership with partition leadership.

### Important Interview Keywords

* Leader Replica
* Partition Leader
* ISR
* Replication
* Failover

---

## Q37. Follower partition.

### Answer

A follower replica is a copy of a partition maintained on another broker.

Its responsibilities are:

* Continuously fetch data from the leader.
* Stay synchronized with the leader.
* Take over if elected as the new leader after a failure.

Followers do not serve normal producer writes or consumer reads.

Having follower replicas improves fault tolerance and availability.

### Expected Follow-up Questions

* How do followers stay synchronized?
* What happens if a follower falls behind?
* Can consumers read from followers?

### Common Mistakes

* Saying followers accept writes.
* Assuming followers always have identical data instantly.

### Important Interview Keywords

* Follower Replica
* Replication
* Synchronization
* Leader Failover
* High Availability

---

## Q38. ISR (In-Sync Replicas).

### Answer

ISR (In-Sync Replicas) is the set of replicas that are fully caught up, or sufficiently caught up, with the leader partition.

For example, if a partition has a replication factor of three:

```text
Leader  → Broker 1
Follower → Broker 2
Follower → Broker 3
```

If both followers are keeping up with the leader, the ISR contains all three replicas.

If one follower falls too far behind, Kafka removes it from the ISR until it catches up.

ISR is important because Kafka elects a new leader from the ISR during a leader failure, helping avoid data loss.

### Expected Follow-up Questions

* How does Kafka decide if a replica leaves the ISR?
* What is `min.insync.replicas`?
* What happens if ISR becomes too small?

### Common Mistakes

* Confusing ISR with all replicas.
* Assuming every replica is always in sync.

### Important Interview Keywords

* ISR
* Replication
* Leader Election
* Replica Lag
* Fault Tolerance

---

## Q39. Preferred leader.

### Answer

The preferred leader is the replica that Kafka ideally wants to act as the leader for a partition.

By default, this is typically the first replica assigned when the partition is created.

After broker failures and recoveries, leadership may move to another replica. Kafka can later perform a preferred leader election to restore leadership to the preferred replica.

This helps distribute leadership evenly across brokers and prevents some brokers from becoming overloaded.

### Production Considerations

Balanced leadership improves resource utilization because leader replicas handle all client traffic.

### Expected Follow-up Questions

* Why is preferred leader election needed?
* Does it move partition data?
* How is leader balancing performed?

### Common Mistakes

* Confusing preferred leader with the controller.
* Assuming preferred leader election copies data.

### Important Interview Keywords

* Preferred Leader
* Leader Election
* Load Balancing
* Broker Utilization
* Partition Leadership

---

## Q40. Partition best practices.

### Answer

Some important partition best practices are:

* Choose the partition count based on expected throughput and future growth.
* Use **key-based partitioning** when ordering is required.
* Choose **high-cardinality keys** to avoid hot partitions.
* Avoid creating an excessive number of partitions because they increase metadata, open files, and rebalance overhead.
* Set an appropriate replication factor for fault tolerance.
* Monitor partition-level metrics such as throughput and consumer lag.

A well-designed partition strategy improves scalability while maintaining balanced load and predictable ordering.

### Expected Follow-up Questions

* How do you decide the number of partitions?
* What causes hot partitions?
* Can partitions be changed later?

### Common Mistakes

* Creating hundreds of partitions without a scalability need.
* Using poor partition keys.
* Ignoring future growth while choosing the initial partition count.

### Important Interview Keywords

* Partition Strategy
* High Cardinality
* Key-based Partitioning
* Consumer Parallelism
* Replication Factor

## Q41. Kafka Producer.

### Answer

A Kafka Producer is the client responsible for publishing events to Kafka topics.

When sending a message, the producer:

1. Fetches cluster metadata.
2. Determines the target partition.
3. Batches records in memory.
4. Sends the batch to the partition leader.
5. Receives an acknowledgment based on the configured `acks` setting.

The producer supports asynchronous sending, batching, compression, retries, and idempotency, allowing it to achieve high throughput while maintaining reliability.

### Production Considerations

In production, it's common to enable idempotence, use asynchronous sends, configure retries appropriately, and choose a partition key carefully to balance throughput and ordering.

### Expected Follow-up Questions

* How does the producer choose a partition?
* What is `acks`?
* What is an idempotent producer?
* How do retries work?

### Common Mistakes

* Thinking producers send data to all brokers.
* Ignoring partition key selection.

### Important Interview Keywords

* Producer
* Partition Leader
* Metadata
* Asynchronous Send
* Batching
* Idempotence

---

## Q42. Producer workflow.

### Answer

The producer workflow is the sequence of steps Kafka follows to publish a message.

```text
Application
     │
     ▼
Producer API
     │
Fetch Metadata
     │
Choose Partition
     │
Batch Records
     │
Send to Partition Leader
     │
Replication (if required)
     │
Receive Acknowledgment
```

The producer first fetches metadata to identify the leader broker for the target partition. It buffers records into batches, sends them to the leader, and waits for acknowledgments based on the configured reliability level.

By default, sending is asynchronous, allowing the application to continue without waiting for every request to complete.

### Expected Follow-up Questions

* What happens if the leader is unavailable?
* How does batching improve performance?
* What is `linger.ms`?

### Common Mistakes

* Assuming every send results in a separate network request.
* Forgetting that producers cache metadata.

### Important Interview Keywords

* Metadata
* Partitioner
* Batch
* Leader
* Acknowledgment

---

## Q43. Producer configuration.

### Answer

Some of the most important producer configurations are:

| Configuration                           | Purpose                                               |
| --------------------------------------- | ----------------------------------------------------- |
| `acks`                                  | Controls delivery durability.                         |
| `retries`                               | Number of retry attempts on transient failures.       |
| `enable.idempotence`                    | Prevents duplicate messages caused by retries.        |
| `batch.size`                            | Maximum batch size before sending.                    |
| `linger.ms`                             | Time to wait before sending a partially filled batch. |
| `compression.type`                      | Compresses batches to reduce network usage.           |
| `max.in.flight.requests.per.connection` | Controls concurrent requests per connection.          |
| `delivery.timeout.ms`                   | Maximum time allowed for message delivery.            |

The right configuration depends on whether the application prioritizes throughput, latency, or durability.

### Production Considerations

For critical applications, a common combination is:

* `acks=all`
* `enable.idempotence=true`
* Appropriate retries
* Compression enabled

### Expected Follow-up Questions

* Which settings affect throughput?
* Which settings affect ordering?
* Which settings improve reliability?

### Common Mistakes

* Changing one configuration without understanding its impact on others.
* Optimizing only for throughput while ignoring durability.

### Important Interview Keywords

* `acks`
* `retries`
* `batch.size`
* `linger.ms`
* `compression.type`
* `enable.idempotence`

---

## Q44. acks configuration.

### Answer

The `acks` configuration determines **when the producer considers a message successfully written**.

There are three options:

* **`acks=0`** – The producer does not wait for any acknowledgment. Highest throughput but messages can be lost.
* **`acks=1`** – The leader acknowledges after writing the message locally. If the leader fails before followers replicate it, data can be lost.
* **`acks=all`** (or `-1`) – The leader waits for all required in-sync replicas (ISR) before acknowledging. This provides the highest durability.

### Production Considerations

For most production systems where data loss is unacceptable, `acks=all` is the recommended choice. It is often combined with `min.insync.replicas` and idempotent producers.

### Trade-offs

* `acks=0` → Maximum throughput, lowest reliability.
* `acks=1` → Balanced performance.
* `acks=all` → Highest durability with slightly higher latency.

### Expected Follow-up Questions

* What is `min.insync.replicas`?
* Can `acks=all` still lose data?
* How does this affect latency?

### Common Mistakes

* Assuming `acks=all` means every replica in the cluster acknowledges.
* Confusing `acks` with consumer acknowledgments.

### Important Interview Keywords

* `acks`
* Leader
* ISR
* Durability
* Latency

---

## Q45. batch.size.

### Answer

`batch.size` specifies the **maximum amount of data the producer buffers per partition before sending a batch**.

Instead of sending every message individually, Kafka groups multiple records into one request.

Larger batches generally improve throughput because they reduce the number of network requests.

If the batch isn't filled, Kafka may still send it after `linger.ms` expires.

### Production Considerations

Increasing `batch.size` is beneficial for high-throughput workloads, but setting it too large can increase memory usage.

### Trade-offs

* Larger batches → Higher throughput, slightly higher latency.
* Smaller batches → Lower latency, more network overhead.

### Expected Follow-up Questions

* How does `batch.size` work with `linger.ms`?
* Does it guarantee batch size?
* Does each partition have its own batch?

### Common Mistakes

* Assuming Kafka always waits until the batch is completely full.
* Confusing batch size with message size.

### Important Interview Keywords

* Batching
* Throughput
* Memory Buffer
* Network Efficiency
* `linger.ms`

---

## Q46. linger.ms.

### Answer

`linger.ms` specifies **how long the producer waits for additional records before sending a partially filled batch**.

For example:

* `linger.ms=0` → Send immediately.
* `linger.ms=10` → Wait up to 10 ms to collect more records.

Waiting briefly often results in larger batches, improving throughput and compression efficiency.

### Production Considerations

A small value, such as 5–20 ms, is commonly used in high-throughput systems to improve batching without significantly increasing latency.

### Trade-offs

* Higher `linger.ms` → Better throughput, higher latency.
* Lower `linger.ms` → Lower latency, smaller batches.

### Expected Follow-up Questions

* Difference between `linger.ms` and `batch.size`?
* Does Kafka always wait the full time?
* How does this affect latency?

### Common Mistakes

* Thinking the producer always waits for `linger.ms`.
* Ignoring its interaction with batching.

### Important Interview Keywords

* `linger.ms`
* Batching
* Latency
* Throughput
* Compression

---

## Q47. compression.type.

### Answer

`compression.type` determines how producer batches are compressed before being sent to Kafka.

Common options include:

* `none`
* `gzip`
* `snappy`
* `lz4`
* `zstd`

Compression reduces network traffic and storage usage because Kafka compresses entire batches rather than individual messages.

### Production Considerations

`zstd` and `lz4` are commonly preferred because they provide a good balance between compression ratio and CPU usage. The best choice depends on workload characteristics.

### Trade-offs

* Stronger compression → Lower network usage, higher CPU.
* Weaker compression → Lower CPU, larger network payloads.

### Expected Follow-up Questions

* Which compression algorithm is best?
* Does Kafka store compressed data?
* Is compression done per message or per batch?

### Common Mistakes

* Thinking messages are compressed individually.
* Ignoring CPU overhead.

### Important Interview Keywords

* Compression
* Batch Compression
* `gzip`
* `lz4`
* `zstd`

---

## Q48. max.in.flight.requests.

### Answer

`max.in.flight.requests.per.connection` controls the **maximum number of unacknowledged requests a producer can have on a single connection**.

Allowing multiple requests in flight improves throughput because the producer doesn't wait for each acknowledgment before sending the next request.

However, if retries occur, a later batch may succeed before an earlier retried batch, which can cause out-of-order delivery.

### Production Considerations

When using idempotent producers, Kafka safely supports multiple in-flight requests while preserving ordering within supported limits.

### Trade-offs

* Higher value → Better throughput.
* Lower value → Simpler ordering guarantees but reduced throughput.

### Expected Follow-up Questions

* How does this affect ordering?
* What happens during retries?
* How does idempotence help?

### Common Mistakes

* Ignoring ordering implications during retries.
* Setting it very high without understanding the workload.

### Important Interview Keywords

* In-flight Requests
* Ordering
* Retries
* Idempotent Producer
* Throughput

---

## Q49. Idempotent producer.

### Answer

An idempotent producer ensures that **retries do not result in duplicate messages** being written to a partition.

Normally, if a producer retries after a timeout, the original message may already have been written, leading to duplicates.

With `enable.idempotence=true`, Kafka assigns sequence numbers to producer requests. The broker detects duplicate retries and ignores them.

This provides exactly-once writes **from the producer to a Kafka partition**, even if retries occur.

### Production Considerations

Idempotence should be enabled for most production applications because it improves reliability with minimal overhead.

### Expected Follow-up Questions

* How is this different from transactions?
* Does it guarantee exactly-once processing?
* How are duplicates detected?

### Common Mistakes

* Saying idempotence guarantees end-to-end exactly-once processing.
* Confusing producer idempotence with consumer idempotency.

### Important Interview Keywords

* Idempotence
* Sequence Number
* Duplicate Prevention
* Retries
* Producer Reliability

---

## Q50. Producer retries.

### Answer

Producer retries allow Kafka to automatically resend messages when transient failures occur, such as temporary network issues or leader elections.

If a send fails with a retryable error, the producer retries according to its configuration until the message is successfully delivered or the delivery timeout is reached.

Retries improve reliability without requiring application-level retry logic.

### Production Considerations

Retries are commonly used together with:

* `enable.idempotence=true`
* `acks=all`

This combination provides reliable delivery while preventing duplicate writes caused by retries.

### Trade-offs

Retries improve reliability but may increase latency. Without idempotence, retries can also introduce duplicate messages.

### Expected Follow-up Questions

* Which failures are retryable?
* Can retries affect ordering?
* How do retries work with idempotence?

### Common Mistakes

* Enabling retries without idempotence for critical workloads.
* Assuming retries can recover every type of failure.

### Important Interview Keywords

* Retries
* Retryable Errors
* Idempotence
* `acks=all`
* Delivery Timeout
