# Garbage Collection Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Garbage Collection is one of the most frequently asked JVM topics in SDE-2 backend interviews. Interviewers expect candidates to understand not only how GC works, but also how it affects latency, throughput, memory usage, and production systems.

---

# Table of Contents

1. Garbage Collection Fundamentals
2. Heap Memory Layout
3. Object Lifecycle
4. Reachability Analysis
5. Reference Types
6. Garbage Collection Algorithms
7. Garbage Collectors
8. GC Tuning
9. GC Logs & Monitoring
10. Memory Leaks
11. OutOfMemoryError
12. Intermediate Questions
13. Advanced Questions
14. Scenario-Based Questions
15. Production Experience
16. Why Questions
17. Trade-offs
18. Common Follow-up Questions

---

# 1. Garbage Collection Fundamentals

## Basic

### Q1.
What is Garbage Collection?

**Follow-ups**
- Why does Java need Garbage Collection?
- What problems does it solve?

---

### Q2.
Who performs Garbage Collection?

---

### Q3.
Why doesn't Java require manual memory management?

---

### Q4.
When does Garbage Collection occur?

---

### Q5.
Can developers explicitly trigger Garbage Collection?

---

### Q6.
What does `System.gc()` actually do?

---

### Q7.
Is `System.gc()` guaranteed to run GC?

---

### Q8.
Can Garbage Collection stop application execution?

---

### Q9.
What is a GC pause?

---

### Q10.
Why are GC pauses important in backend applications?

---

# 2. Heap Memory Layout

## Basic

### Q11.
Explain the Java Heap.

---

### Q12.
What are Young Generation and Old Generation?

---

### Q13.
What is Eden Space?

---

### Q14.
What are Survivor Spaces?

---

### Q15.
Why are there two Survivor spaces?

---

### Q16.
What happens when Eden becomes full?

---

### Q17.
When does an object move to Survivor Space?

---

### Q18.
When is an object promoted to Old Generation?

---

### Q19.
Why are most objects short-lived?

---

### Q20.
How does the Generational Hypothesis influence JVM design?

---

# 3. Object Lifecycle

## Basic

### Q21.
What happens from object creation until collection?

---

### Q22.
How does an object become eligible for Garbage Collection?

---

### Q23.
Can an object without references still exist in memory?

---

### Q24.
Can an object be collected immediately after becoming unreachable?

---

### Q25.
What is object promotion?

---

### Q26.
What is object aging?

---

### Q27.
What is the Tenuring Threshold?

---

### Q28.
Can objects move back from Old Generation to Young Generation?

---

### Q29.
Why are long-lived objects promoted?

---

### Q30.
How do temporary objects affect GC performance?

---

# 4. Reachability Analysis

## Intermediate

### Q31.
How does JVM determine whether an object is garbage?

---

### Q32.
What are GC Roots?

---

### Q33.
Examples of GC Roots.

---

### Q34.
Reachability Analysis vs Reference Counting.

---

### Q35.
Why doesn't Java use Reference Counting?

---

### Q36.
What problem does Reference Counting fail to solve?

---

### Q37.
How are cyclic references handled?

---

### Q38.
Can cyclic references cause memory leaks?

---

### Q39.
How does JVM traverse the object graph?

---

### Q40.
What happens if an object is reachable through multiple references?

---

# 5. Reference Types

## Intermediate

### Q41.
What are the different reference types in Java?

---

### Q42.
Strong Reference.

---

### Q43.
Soft Reference.

---

### Q44.
Weak Reference.

---

### Q45.
Phantom Reference.

---

### Q46.
When should SoftReference be used?

---

### Q47.
When should WeakReference be used?

---

### Q48.
What is ReferenceQueue?

---

### Q49.
How does WeakHashMap work?

---

### Q50.
Which reference type is suitable for caching?

---

# 6. Garbage Collection Algorithms

## Intermediate

### Q51.
What are the major GC algorithms?

---

### Q52.
Mark-Sweep Algorithm.

---

### Q53.
Problems with Mark-Sweep.

---

### Q54.
Mark-Compact Algorithm.

---

### Q55.
Copying Algorithm.

---

### Q56.
Generational Garbage Collection.

---

### Q57.
What is memory fragmentation?

---

### Q58.
How does Mark-Compact eliminate fragmentation?

---

### Q59.
Why is the Copying algorithm fast?

---

### Q60.
Why isn't Copying used for the entire heap?

---

### Q61.
Stop-the-World (STW).

---

### Q62.
Why are STW pauses necessary?

---

### Q63.
Can Garbage Collection occur concurrently?

---

### Q64.
Incremental GC.

---

### Q65.
Concurrent GC.

---

# 7. Garbage Collectors

## Intermediate

### Q66.
What Garbage Collectors are available in modern JVMs?

---

### Q67.
Serial GC.

---

### Q68.
Parallel GC.

---

### Q69.
CMS Garbage Collector.

---

### Q70.
Why was CMS deprecated?

---

### Q71.
G1 Garbage Collector.

---

### Q72.
How does G1 divide the heap?

---

### Q73.
What are G1 Regions?

---

### Q74.
How does G1 reduce pause times?

---

### Q75.
Mixed Collection in G1.

---

### Q76.
Z Garbage Collector (ZGC).

---

### Q77.
Shenandoah GC.

---

### Q78.
Difference between G1 and ZGC.

---

### Q79.
When would you choose Parallel GC?

---

### Q80.
When would you choose G1 GC?

---

### Q81.
When would you choose ZGC?

---

### Q82.
Which GC is the default in Java 17?

---

### Q83.
Can GC be changed at runtime?

---

### Q84.
How do you configure a Garbage Collector?

---

### Q85.
How do different collectors affect latency and throughput?

---

# 8. GC Tuning

## Advanced

### Q86.
What JVM parameters influence Garbage Collection?

---

### Q87.
How do you set heap size?

---

### Q88.
Difference between -Xms and -Xmx.

---

### Q89.
Should Xms and Xmx always be equal?

---

### Q90.
How do you choose heap size?

---

### Q91.
How do you reduce GC frequency?

---

### Q92.
How do you reduce GC pause times?

---

### Q93.
How do object allocation rates affect GC?

---

### Q94.
How does excessive allocation impact application performance?

---

### Q95.
How does thread count influence GC?

---

### Q96.
How do large objects affect GC?

---

### Q97.
How do caches affect Garbage Collection?

---

### Q98.
How do object pools affect Garbage Collection?

---

### Q99.
Can increasing heap size reduce latency?

---

### Q100.
Can increasing heap size increase pause time?

---

# 9. GC Logs & Monitoring

### Q101.
Why should GC logs be enabled?

---

### Q102.
What information is available in GC logs?

---

### Q103.
How do you identify frequent Young GCs?

---

### Q104.
How do you identify Full GCs?

---

### Q105.
How do you identify memory pressure?

---

### Q106.
How do you detect long GC pauses?

---

### Q107.
Which JVM tools help analyze GC?

---

### Q108.
How do Java Flight Recorder (JFR) and Java Mission Control (JMC) help?

---

### Q109.
How does VisualVM help with memory analysis?

---

### Q110.
How do you monitor GC in production?

---

# 10. Memory Leaks

## Advanced

### Q111.
Can Java applications have memory leaks?

---

### Q112.
Common causes of memory leaks.

---

### Q113.
Static collections causing memory leaks.

---

### Q114.
ThreadLocal memory leaks.

---

### Q115.
ClassLoader memory leaks.

---

### Q116.
Listener registration leaks.

---

### Q117.
Cache-related memory leaks.

---

### Q118.
Improper collection usage causing leaks.

---

### Q119.
How do memory leaks differ from high memory usage?

---

### Q120.
How would you investigate a memory leak?

---

# 11. OutOfMemoryError

### Q121.
Different types of OutOfMemoryError.

---

### Q122.
Java Heap Space OOM.

---

### Q123.
GC Overhead Limit Exceeded.

---

### Q124.
Metaspace OutOfMemoryError.

---

### Q125.
Direct Buffer Memory OutOfMemoryError.

---

### Q126.
Unable to Create Native Thread.

---

### Q127.
StackOverflowError vs OutOfMemoryError.

---

### Q128.
How do you debug Heap OOM?

---

### Q129.
What is a Heap Dump?

---

### Q130.
How do you analyze a Heap Dump?

---

# 12. Advanced Questions

### Q131.
How does G1 determine which regions to collect?

---

### Q132.
Remembered Sets in G1.

---

### Q133.
Card Tables.

---

### Q134.
Write Barriers.

---

### Q135.
Read Barriers.

---

### Q136.
SATB (Snapshot At The Beginning).

---

### Q137.
Concurrent Marking.

---

### Q138.
Concurrent Refinement Threads.

---

### Q139.
Humongous Objects in G1.

---

### Q140.
Compressed OOPs and heap sizing.

---

### Q141.
TLAB (Thread Local Allocation Buffer).

---

### Q142.
PLAB (Promotion Local Allocation Buffer).

---

### Q143.
Object Allocation Fast Path.

---

### Q144.
Allocation Failure.

---

### Q145.
GC Safepoints.

---

### Q146.
Promotion Failure.

---

### Q147.
Evacuation Failure.

---

### Q148.
Floating Garbage.

---

### Q149.
GC Ergonomics.

---

### Q150.
How does JVM automatically choose GC behavior?

---

# 13. Scenario-Based Questions

### Q151.
Your API latency suddenly increases every few minutes. What GC-related issues would you investigate?

---

### Q152.
Your application performs well initially but slows down after several hours. What memory problems would you suspect?

---

### Q153.
Frequent Full GCs appear in production. What could be causing them?

---

### Q154.
A service frequently throws `OutOfMemoryError: Java heap space`. How would you investigate?

---

### Q155.
Your application has sufficient heap but still experiences long GC pauses. Why?

---

### Q156.
A cache causes continuous memory growth. How would you redesign it?

---

### Q157.
GC logs show excessive object promotion. What might be happening?

---

### Q158.
A Spring Boot service running inside Kubernetes gets OOMKilled. What JVM and container factors would you examine?

---

### Q159.
Your service creates millions of temporary objects every second. How would you optimize it?

---

### Q160.
An application experiences low throughput despite low CPU utilization. Could GC be involved? How would you verify it?

---

# 14. Production Experience Questions

### Q161.
Have you ever analyzed GC logs in production?

---

### Q162.
Which Garbage Collector have you used in production?

---

### Q163.
Have you ever tuned JVM heap settings?

---

### Q164.
Have you investigated Full GC issues?

---

### Q165.
Have you diagnosed memory leaks?

---

### Q166.
Have you analyzed Heap Dumps?

---

### Q167.
Have you used Eclipse MAT, VisualVM, JMC, or JFR?

---

### Q168.
Have you optimized object allocation patterns?

---

### Q169.
Have you dealt with Kubernetes OOMKilled containers?

---

### Q170.
What GC-related production incident taught you the most?

---

# 15. "Why" Questions

### Q171.
Why does Java use Garbage Collection instead of manual memory management?

---

### Q172.
Why is the Generational Hypothesis effective?

---

### Q173.
Why doesn't Java use Reference Counting?

---

### Q174.
Why are most objects allocated in Eden?

---

### Q175.
Why does G1 divide the heap into regions?

---

### Q176.
Why are GC pauses unavoidable?

---

### Q177.
Why are Full GCs significantly more expensive than Young GCs?

---

### Q178.
Why can a larger heap increase pause times?

---

### Q179.
Why do memory leaks still occur in a Garbage-Collected language?

---

### Q180.
Why isn't `System.gc()` recommended in production applications?

---

# 16. Trade-off Questions

### Q181.
Serial GC vs Parallel GC.

---

### Q182.
Parallel GC vs G1 GC.

---

### Q183.
G1 GC vs ZGC.

---

### Q184.
Throughput vs Latency.

---

### Q185.
Heap Size vs GC Pause Time.

---

### Q186.
Large Heap vs Frequent GC.

---

### Q187.
Caching vs Memory Consumption.

---

### Q188.
Object Pooling vs Modern Garbage Collectors.

---

### Q189.
SoftReference Cache vs Explicit Cache Eviction.

---

### Q190.
High Allocation Rate vs Object Reuse.

---

# 17. Common Interview Follow-up Questions

## If you mention Garbage Collection
- How does GC work?
- When does GC run?
- What are GC Roots?
- Which algorithm is used?
- Which collector is active?

---

## If you mention Heap
- Young Generation?
- Old Generation?
- Eden?
- Survivor Spaces?
- Promotion?

---

## If you mention G1 GC
- Regions?
- Mixed GC?
- Remembered Sets?
- Humongous Objects?
- Why is G1 the default?

---

## If you mention Memory Leak
- Heap Dump?
- Eclipse MAT?
- Static Collections?
- ThreadLocal?
- Cache?

---

## If you mention OutOfMemoryError
- Different OOM types?
- Heap Dump?
- GC Logs?
- JVM Options?
- Root Cause Analysis?

---

## If you mention GC Tuning
- Xms/Xmx?
- Pause Goals?
- Allocation Rate?
- Heap Sizing?
- Monitoring?

---

# Staff Engineer Discussion Questions

### Q191.
How do you balance latency and throughput when selecting a Garbage Collector?

---

### Q192.
How would you optimize memory usage in a high-throughput microservice?

---

### Q193.
How do object allocation patterns influence application scalability?

---

### Q194.
How would you investigate intermittent latency spikes caused by GC?

---

### Q195.
How do container memory limits affect JVM Garbage Collection?

---

### Q196.
How would you design a caching strategy that minimizes GC pressure?

---

### Q197.
What metrics do you monitor to identify GC-related production issues?

---

### Q198.
How do you evaluate whether a JVM tuning change improved performance?

---

### Q199.
How would you explain GC behavior to a junior developer investigating latency issues?

---

### Q200.
If you were redesigning the JVM's Garbage Collector today, what would you improve?

---

# Completion Checklist

## Fundamentals
- [ ] Garbage Collection Basics
- [ ] Heap Layout
- [ ] Object Lifecycle
- [ ] Reachability Analysis
- [ ] GC Roots

## Algorithms
- [ ] Mark-Sweep
- [ ] Mark-Compact
- [ ] Copying
- [ ] Generational GC
- [ ] Concurrent GC

## Garbage Collectors
- [ ] Serial GC
- [ ] Parallel GC
- [ ] CMS
- [ ] G1 GC
- [ ] ZGC
- [ ] Shenandoah

## Tuning
- [ ] Heap Sizing
- [ ] GC Logs
- [ ] JVM Flags
- [ ] Monitoring
- [ ] Performance Optimization

## Memory Issues
- [ ] Memory Leaks
- [ ] Heap Dumps
- [ ] OutOfMemoryError
- [ ] ThreadLocal Leaks
- [ ] Cache Management

## Advanced
- [ ] TLAB
- [ ] Write Barriers
- [ ] Remembered Sets
- [ ] SATB
- [ ] Safepoints

## Production
- [ ] GC Log Analysis
- [ ] Heap Dump Analysis
- [ ] Kubernetes OOMKilled
- [ ] JVM Monitoring
- [ ] Memory Optimization

## Interview Readiness
- [ ] Can explain the complete object lifecycle.
- [ ] Can compare all major Garbage Collectors.
- [ ] Can diagnose common GC-related production issues.
- [ ] Can interpret GC logs and heap dumps.
- [ ] Can recommend GC tuning strategies based on application workload.

---

**Total Questions:** 200
**Recommended Time:** 3–4 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** Heap Layout, Generational GC, G1 GC, GC Algorithms, GC Tuning, Memory Leaks, Heap Dumps, OutOfMemoryError, GC Logs, JVM Memory Management