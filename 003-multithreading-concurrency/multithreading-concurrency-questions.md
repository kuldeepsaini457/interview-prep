# Multithreading & Concurrency Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Most SDE-2 backend interviews spend significant time on Java concurrency because production systems are highly concurrent.

---

# Table of Contents

1. Thread Fundamentals
2. Thread Lifecycle
3. Creating Threads
4. Synchronization
5. Locks
6. Visibility & Memory Model
7. volatile
8. Atomic Classes
9. Executor Framework
10. Thread Pools
11. Callable & Future
12. CompletableFuture
13. Concurrent Collections
14. Common Concurrency Problems
15. Producer-Consumer
16. Deadlock, Livelock & Starvation
17. Java Memory Model
18. Intermediate Questions
19. Advanced Questions
20. Scenario-Based Questions
21. Production Experience
22. Why Questions
23. Trade-offs
24. Common Follow-up Questions

---

# 1. Thread Fundamentals

## Basic

### Q1.
What is a thread?

**Follow-ups**
- Difference between thread and process.
- Why do we need multithreading?

---

### Q2.
What is multithreading?

---

### Q3.
Benefits of multithreading.

---

### Q4.
Draw the lifecycle of a Java thread.

---

### Q5.
Difference between concurrency and parallelism.

---

### Q6.
Difference between multitasking and multithreading.

---

### Q7.
What is context switching?

---

### Q8.
Why is context switching expensive?

---

### Q9.
What determines how many threads run simultaneously?

---

### Q10.
How many threads can execute simultaneously on a 4-core CPU?

---

# 2. Thread Lifecycle

### Q11.
Explain every state in the Thread lifecycle.

---

### Q12.
Difference between NEW and RUNNABLE.

---

### Q13.
Difference between BLOCKED and WAITING.

---

### Q14.
Difference between WAITING and TIMED_WAITING.

---

### Q15.
When does a thread enter BLOCKED state?

---

### Q16.
When does a thread terminate?

---

### Q17.
Can a terminated thread restart?

---

### Q18.
How do you check thread state?

---

### Q19.
What happens if start() is called twice?

---

### Q20.
Difference between start() and run().

---

# 3. Creating Threads

### Q21.
Different ways to create threads.

---

### Q22.
Runnable vs Thread class.

---

### Q23.
Runnable vs Callable.

---

### Q24.
Why is implementing Runnable generally preferred?

---

### Q25.
Can one Runnable be shared across multiple threads?

---

### Q26.
Can Thread class be extended multiple times?

---

### Q27.
When should Thread class be extended?

---

### Q28.
How do Spring Boot applications usually create background threads?

---

### Q29.
How would you execute thousands of independent tasks?

---

### Q30.
Why is creating new Thread() repeatedly discouraged?

---

# 4. Synchronization

## Basic

### Q31.
What is synchronization?

---

### Q32.
Why do we need synchronization?

---

### Q33.
What is a critical section?

---

### Q34.
Explain race condition.

---

### Q35.
What is mutual exclusion?

---

### Q36.
How does synchronized work?

---

### Q37.
Object lock vs Class lock.

---

### Q38.
Difference between synchronized method and synchronized block.

---

### Q39.
Can synchronized methods execute concurrently?

---

### Q40.
Can synchronized static methods execute concurrently?

---

### Q41.
Can two synchronized methods run simultaneously?

---

### Q42.
Can synchronized block improve performance?

---

### Q43.
What object should be used as lock?

---

### Q44.
What are the dangers of synchronizing on String literals?

---

### Q45.
What happens if synchronized is removed?

---

# 5. Locks

### Q46.
Difference between synchronized and Lock interface.

---

### Q47.
Why was ReentrantLock introduced?

---

### Q48.
Advantages of ReentrantLock.

---

### Q49.
What is lock fairness?

---

### Q50.
What is tryLock()?

---

### Q51.
What is lockInterruptibly()?

---

### Q52.
What is ReentrantReadWriteLock?

---

### Q53.
When should ReadWriteLock be used?

---

### Q54.
StampedLock vs ReadWriteLock.

---

### Q55.
When should synchronized still be preferred?

---

# 6. Visibility & Java Memory Model

### Q56.
What is thread visibility?

---

### Q57.
Why can one thread fail to see another thread's changes?

---

### Q58.
What is CPU cache?

---

### Q59.
What is cache coherence?

---

### Q60.
How does Java ensure visibility?

---

### Q61.
Difference between visibility and atomicity.

---

### Q62.
Difference between atomicity and synchronization.

---

### Q63.
What is instruction reordering?

---

### Q64.
Why does instruction reordering happen?

---

### Q65.
How does Java Memory Model address these issues?

---

# 7. volatile

### Q66.
What is volatile?

---

### Q67.
When should volatile be used?

---

### Q68.
When should volatile NOT be used?

---

### Q69.
Can volatile solve race conditions?

---

### Q70.
Difference between volatile and synchronized.

---

### Q71.
Can volatile guarantee atomicity?

---

### Q72.
How does volatile prevent instruction reordering?

---

### Q73.
Can multiple variables be made volatile atomically?

---

### Q74.
When is volatile sufficient?

---

### Q75.
Real production examples of volatile usage.

---

# 8. Atomic Classes

### Q76.
What are Atomic classes?

---

### Q77.
How does AtomicInteger work internally?

---

### Q78.
What is CAS (Compare-And-Set)?

---

### Q79.
Advantages of CAS.

---

### Q80.
CAS vs synchronized.

---

### Q81.
What is ABA problem?

---

### Q82.
How does AtomicReference work?

---

### Q83.
LongAdder vs AtomicLong.

---

### Q84.
When should LongAdder be preferred?

---

### Q85.
Can AtomicInteger replace synchronized everywhere?

---

# 9. Executor Framework

### Q86.
What is Executor Framework?

---

### Q87.
Why was Executor introduced?

---

### Q88.
Executor vs ExecutorService.

---

### Q89.
Lifecycle of ExecutorService.

---

### Q90.
Difference between shutdown() and shutdownNow().

---

### Q91.
How do you wait for task completion?

---

### Q92.
What happens if ExecutorService isn't shut down?

---

### Q93.
How would you configure ExecutorService in Spring Boot?

---

### Q94.
Can ExecutorService reject tasks?

---

### Q95.
What is RejectedExecutionException?

---

# 10. Thread Pools

### Q96.
Why are thread pools important?

---

### Q97.
How does ThreadPoolExecutor work internally?

---

### Q98.
Difference between corePoolSize and maximumPoolSize.

---

### Q99.
What is keepAliveTime?

---

### Q100.
What is BlockingQueue inside ThreadPoolExecutor?

---

### Q101.
Difference between FixedThreadPool and CachedThreadPool.

---

### Q102.
SingleThreadExecutor vs FixedThreadPool.

---

### Q103.
ScheduledThreadPool use cases.

---

### Q104.
How do you determine optimal thread pool size?

---

### Q105.
CPU-bound vs IO-bound thread pools.

---

### Q106.
Why can oversized thread pools reduce performance?

---

### Q107.
Thread pool exhaustion.

---

### Q108.
What is queue saturation?

---

### Q109.
How do you monitor thread pools?

---

### Q110.
Production mistakes involving thread pools.

---

# 11. Callable & Future

### Q111.
Difference between Runnable and Callable.

---

### Q112.
What is Future?

---

### Q113.
How does Future.get() behave?

---

### Q114.
Can Future be cancelled?

---

### Q115.
Limitations of Future.

---

### Q116.
How do you execute multiple Callables?

---

### Q117.
invokeAll() vs invokeAny().

---

### Q118.
Future timeout handling.

---

### Q119.
How do exceptions propagate from Future?

---

### Q120.
Production use cases.

---

# 12. CompletableFuture

### Q121.
Why was CompletableFuture introduced?

---

### Q122.
Future vs CompletableFuture.

---

### Q123.
thenApply() vs thenCompose().

---

### Q124.
thenApply() vs thenAccept().

---

### Q125.
thenRun() vs thenAccept().

---

### Q126.
thenCombine() vs allOf().

---

### Q127.
allOf() vs anyOf().

---

### Q128.
Exception handling with exceptionally().

---

### Q129.
handle() vs whenComplete().

---

### Q130.
How would you combine results from three microservices?

---

### Q131.
How do you avoid blocking with CompletableFuture?

---

### Q132.
Common mistakes with CompletableFuture.

---

# 13. Concurrent Collections

### Q133.
Why are concurrent collections needed?

---

### Q134.
ConcurrentHashMap vs HashMap.

---

### Q135.
How did ConcurrentHashMap change in Java 8?

---

### Q136.
CopyOnWriteArrayList use cases.

---

### Q137.
Advantages and disadvantages of CopyOnWriteArrayList.

---

### Q138.
BlockingQueue implementations.

---

### Q139.
ArrayBlockingQueue vs LinkedBlockingQueue.

---

### Q140.
ConcurrentLinkedQueue.

---

### Q141.
ConcurrentSkipListMap.

---

### Q142.
ConcurrentSkipListSet.

---

### Q143.
When should synchronized collections be avoided?

---

### Q144.
Collections.synchronizedList() vs CopyOnWriteArrayList.

---

### Q145.
Concurrent collection selection strategy.

---

# 14. Common Concurrency Problems

### Q146.
Race condition.

---

### Q147.
Data race vs race condition.

---

### Q148.
Lost update problem.

---

### Q149.
Visibility problem.

---

### Q150.
Thread interference.

---

### Q151.
Memory consistency errors.

---

### Q152.
False sharing.

---

### Q153.
Priority inversion.

---

### Q154.
Busy waiting.

---

### Q155.
Thread leakage.

---

# 15. Producer-Consumer

### Q156.
Explain Producer-Consumer problem.

---

### Q157.
How would you implement Producer-Consumer?

---

### Q158.
Why is BlockingQueue preferred?

---

### Q159.
wait()/notify() implementation vs BlockingQueue.

---

### Q160.
Bounded vs unbounded queues.

---

# 16. Deadlock, Livelock & Starvation

### Q161.
What is deadlock?

---

### Q162.
Necessary conditions for deadlock.

---

### Q163.
How do you prevent deadlocks?

---

### Q164.
How do you detect deadlocks?

---

### Q165.
Real production examples of deadlocks.

---

### Q166.
Difference between deadlock and livelock.

---

### Q167.
Difference between starvation and deadlock.

---

### Q168.
How does lock ordering prevent deadlocks?

---

### Q169.
Can tryLock() help prevent deadlocks?

---

### Q170.
How would you debug a deadlocked JVM?

---

# 17. Advanced Questions

### Q171.
How does synchronized work internally after Java 6 optimizations?

---

### Q172.
Biased locking, lightweight locking and heavyweight locking.

---

### Q173.
What is lock inflation?

---

### Q174.
Monitor enter and monitor exit bytecode.

---

### Q175.
How does CAS work at the CPU level?

---

### Q176.
Memory barriers.

---

### Q177.
Happens-before relationship.

---

### Q178.
Safe publication.

---

### Q179.
Double-checked locking.

---

### Q180.
Why does double-checked locking require volatile?

---

### Q181.
ForkJoinPool.

---

### Q182.
Work stealing algorithm.

---

### Q183.
Parallel Stream internals.

---

### Q184.
Virtual Threads (Project Loom).

---

### Q185.
When would virtual threads be beneficial?

---

# 18. Scenario-Based Questions

### Q186.
Your Spring Boot application creates one thread per request. What problems can occur?

---

### Q187.
Your API becomes slow under high concurrency. How would you investigate?

---

### Q188.
A shared counter gives incorrect values under load. What are possible reasons?

---

### Q189.
A thread pool queue grows continuously. What could be happening?

---

### Q190.
Multiple threads update the same order record. How would you prevent inconsistencies?

---

### Q191.
One thread blocks for several minutes. What effect can it have on the application?

---

### Q192.
Your application experiences random deadlocks in production. What steps would you take?

---

### Q193.
CPU utilization reaches 100% while throughput drops. What concurrency issues would you suspect?

---

### Q194.
A REST endpoint calls five downstream services. How would you execute them concurrently?

---

### Q195.
You need to process one million Kafka messages concurrently. How would you design the consumer?

---

# 19. Production Experience Questions

### Q196.
Have you used ExecutorService in production? Where?

---

### Q197.
Have you tuned thread pool sizes? How?

---

### Q198.
Have you debugged deadlocks?

---

### Q199.
Have you encountered race conditions?

---

### Q200.
Have you used CompletableFuture in production?

---

### Q201.
How do you configure async execution in Spring Boot?

---

### Q202.
How do you monitor thread pools?

---

### Q203.
Have you used ConcurrentHashMap in production?

---

### Q204.
Have you optimized blocking operations?

---

### Q205.
What concurrency bug took you the longest to debug?

---

# 20. "Why" Questions

### Q206.
Why is Thread.stop() deprecated?

---

### Q207.
Why is wait() defined in Object instead of Thread?

---

### Q208.
Why is notifyAll() often preferred over notify()?

---

### Q209.
Why is volatile not sufficient for increment operations?

---

### Q210.
Why are thread pools preferred over creating threads?

---

### Q211.
Why is synchronized reentrant?

---

### Q212.
Why do concurrent collections exist?

---

### Q213.
Why is CAS generally faster than locking?

---

### Q214.
Why does Future.get() block?

---

### Q215.
Why is lock contention harmful?

---

# 21. Trade-off Questions

### Q216.
synchronized vs ReentrantLock.

---

### Q217.
volatile vs synchronized.

---

### Q218.
AtomicInteger vs synchronized.

---

### Q219.
ExecutorService vs new Thread().

---

### Q220.
Runnable vs Callable.

---

### Q221.
Future vs CompletableFuture.

---

### Q222.
FixedThreadPool vs CachedThreadPool.

---

### Q223.
ConcurrentHashMap vs synchronized HashMap.

---

### Q224.
BlockingQueue vs wait()/notify().

---

### Q225.
Parallel Stream vs CompletableFuture.

---

# 22. Common Interview Follow-up Questions

## If you mention synchronized
- What object is locked?
- Is it reentrant?
- Can it cause deadlocks?
- Bytecode generated?
- JVM optimizations?

---

## If you mention volatile
- Atomicity?
- Visibility?
- Reordering?
- Happens-before?
- Real examples?

---

## If you mention ExecutorService
- ThreadPoolExecutor?
- Queue?
- Rejection policy?
- Shutdown?
- Monitoring?

---

## If you mention CompletableFuture
- Async vs sync methods?
- Custom Executor?
- Exception handling?
- thenCompose?
- allOf?

---

## If you mention ConcurrentHashMap
- Java 7 vs Java 8 implementation?
- Lock striping?
- CAS?
- Read performance?
- Resize behavior?

---

## If you mention Deadlock
- Detection?
- Prevention?
- Thread dump?
- Lock ordering?
- tryLock?

---

# Staff Engineer Discussion Questions

### Q226.
How do you decide whether a task should execute synchronously or asynchronously?

---

### Q227.
How do you size thread pools for CPU-bound and IO-bound workloads?

---

### Q228.
How would you design a highly concurrent order-processing service?

---

### Q229.
What concurrency anti-patterns do you commonly see during code reviews?

---

### Q230.
How do you balance throughput, latency and resource utilization in concurrent systems?

---

### Q231.
How do you minimize lock contention in large backend applications?

---

### Q232.
How do you identify unnecessary synchronization in a codebase?

---

### Q233.
How do you benchmark concurrent code?

---

### Q234.
What metrics would you monitor for concurrency-related issues in production?

---

### Q235.
What is the most difficult concurrency bug you've solved, and how did you approach debugging it?

---

# Completion Checklist

## Fundamentals
- [ ] Thread vs Process
- [ ] Concurrency vs Parallelism
- [ ] Thread Lifecycle
- [ ] Context Switching

## Synchronization
- [ ] synchronized
- [ ] Locks
- [ ] Critical Section
- [ ] Race Conditions
- [ ] Mutual Exclusion

## Java Memory Model
- [ ] Visibility
- [ ] Atomicity
- [ ] Ordering
- [ ] Happens-before
- [ ] Memory Barriers

## Modern Concurrency
- [ ] ExecutorService
- [ ] Thread Pools
- [ ] CompletableFuture
- [ ] Atomic Classes
- [ ] Concurrent Collections

## Concurrency Problems
- [ ] Deadlock
- [ ] Livelock
- [ ] Starvation
- [ ] False Sharing
- [ ] Lost Updates

## Production
- [ ] Thread Pool Tuning
- [ ] Async APIs
- [ ] Performance Debugging
- [ ] Concurrency Monitoring
- [ ] Production Incident Handling

## Interview Readiness
- [ ] Can explain synchronization internals.
- [ ] Can compare all major concurrency utilities with trade-offs.
- [ ] Can design thread-safe backend services.
- [ ] Can debug deadlocks and race conditions.
- [ ] Can discuss real production concurrency challenges.

---

**Total Questions:** 235
**Recommended Time:** 4–5 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** synchronized, volatile, ExecutorService, ThreadPoolExecutor, CompletableFuture, ConcurrentHashMap, Deadlocks, Java Memory Model, CAS, Atomic Classes, Thread Pool Sizing