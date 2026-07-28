# Java Collections Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Adobe, Salesforce, Uber, Flipkart, PhonePe, Razorpay, LinkedIn, Google, etc.

---

# Table of Contents

1. Collection Framework Fundamentals
2. List
3. Set
4. Queue & Deque
5. Map
6. HashMap Deep Dive
7. TreeMap & TreeSet
8. Comparable & Comparator
9. Iterators
10. Fail-Fast & Fail-Safe
11. Internal Working
12. Complexity Analysis
13. Intermediate
14. Advanced
15. Scenario-Based
16. Production Experience
17. Why Questions
18. Trade-offs
19. Common Follow-up Questions

---

# 1. Collection Framework Fundamentals

## Basic

### Q1.
What is the Java Collections Framework?

**Follow-ups**
- Why was it introduced?
- What problems does it solve?

---

### Q2.
Difference between Collection and Collections.

---

### Q3.
Difference between Collection and Map.

---

### Q4.
What are the major interfaces in the Collection Framework?

---

### Q5.
Explain the hierarchy of the Collection Framework.

---

### Q6.
When would you use a Collection instead of an array?

---

### Q7.
What limitations of arrays are solved by collections?

---

### Q8.
Can collections store primitive data types?

**Follow-ups**
- Why not?
- What happens internally?

---

### Q9.
How does Generics improve collections?

---

### Q10.
Why were Generics introduced?

---

### Q11.
What happens if Generics are not used?

---

### Q12.
Difference between Iterable and Collection.

---

### Q13.
What methods are inherited from Collection?

---

### Q14.
Difference between size(), isEmpty(), contains().

---

### Q15.
How do collections grow dynamically?

---

# 2. List

## Basic

### Q16.
What is a List?

---

### Q17.
Properties of List.

---

### Q18.
Difference between ArrayList and LinkedList.

---

### Q19.
Internal structure of ArrayList.

---

### Q20.
Internal structure of LinkedList.

---

### Q21.
How does ArrayList resize itself?

---

### Q22.
What is the default capacity of ArrayList?

---

### Q23.
Difference between capacity and size.

---

### Q24.
Can ArrayList contain null values?

---

### Q25.
Can LinkedList contain duplicates?

---

### Q26.
Complexities of add(), remove(), get() in ArrayList.

---

### Q27.
Complexities of LinkedList operations.

---

### Q28.
When is LinkedList faster than ArrayList?

---

### Q29.
When is ArrayList a poor choice?

---

### Q30.
Why is random access fast in ArrayList?

---

### Q31.
Why is insertion slow in ArrayList?

---

### Q32.
Why is searching slow in LinkedList?

---

### Q33.
Difference between remove(index) and remove(object).

---

### Q34.
How does indexOf() work?

---

### Q35.
How would you remove duplicates from a List?

---

# 3. Set

## Basic

### Q36.
What is Set?

---

### Q37.
Properties of Set.

---

### Q38.
Difference between HashSet, LinkedHashSet and TreeSet.

---

### Q39.
Can Set contain null values?

---

### Q40.
How does HashSet ensure uniqueness?

---

### Q41.
Can duplicate objects exist inside HashSet?

---

### Q42.
How does TreeSet maintain order?

---

### Q43.
Natural ordering vs custom ordering.

---

### Q44.
Complexity of TreeSet operations.

---

### Q45.
When would you use LinkedHashSet?

---

# 4. Queue & Deque

### Q46.
Difference between Queue and Deque.

---

### Q47.
Difference between offer() and add().

---

### Q48.
Difference between poll() and remove().

---

### Q49.
Difference between peek() and element().

---

### Q50.
PriorityQueue internal working.

---

### Q51.
When would you use PriorityQueue?

---

### Q52.
Can PriorityQueue contain null?

---

### Q53.
How does PriorityQueue maintain ordering?

---

### Q54.
Deque vs Stack.

---

### Q55.
Why is Stack considered legacy?

---

# 5. Map

## Basic

### Q56.
What is Map?

---

### Q57.
Difference between HashMap, Hashtable, LinkedHashMap and TreeMap.

---

### Q58.
Properties of HashMap.

---

### Q59.
Properties of TreeMap.

---

### Q60.
Properties of LinkedHashMap.

---

### Q61.
Can HashMap have null keys?

---

### Q62.
Can TreeMap have null keys?

---

### Q63.
Can HashMap have duplicate keys?

---

### Q64.
Can HashMap have duplicate values?

---

### Q65.
Difference between keySet(), values() and entrySet().

---

### Q66.
When should entrySet() be preferred?

---

### Q67.
How do putIfAbsent() and computeIfAbsent() work?

---

### Q68.
Difference between replace() and put().

---

### Q69.
Difference between merge() and compute().

---

### Q70.
How do you safely update a value inside HashMap?

---

# 6. HashMap Deep Dive

## Intermediate

### Q71.
Explain the internal working of HashMap.

---

### Q72.
What happens during put()?

---

### Q73.
What happens during get()?

---

### Q74.
How is bucket index calculated?

---

### Q75.
Why should hashCode() be evenly distributed?

---

### Q76.
What is a collision?

---

### Q77.
How does HashMap resolve collisions?

---

### Q78.
What is separate chaining?

---

### Q79.
What happens when too many collisions occur?

---

### Q80.
What is treeification?

---

### Q81.
When does HashMap convert a bucket into a Red-Black Tree?

---

### Q82.
When does it convert back to LinkedList?

---

### Q83.
What is load factor?

---

### Q84.
Default load factor?

---

### Q85.
What happens during resizing?

---

### Q86.
Why is resizing expensive?

---

### Q87.
How does rehashing work?

---

### Q88.
Can resizing impact application latency?

---

### Q89.
How do you reduce resizing overhead?

---

### Q90.
Why are immutable keys recommended?

---

### Q91.
What happens if key's hashCode changes?

---

### Q92.
Can mutable objects be safely used as keys?

---

### Q93.
How can poor hashCode implementation affect performance?

---

### Q94.
Difference between equals() and hashCode() during lookup.

---

### Q95.
How do HashMap lookups remain O(1) on average?

---

# 7. TreeMap & TreeSet

### Q96.
How does TreeMap maintain ordering?

---

### Q97.
What data structure backs TreeMap?

---

### Q98.
What is a Red-Black Tree?

---

### Q99.
Why Red-Black Tree instead of AVL Tree?

---

### Q100.
Complexity of TreeMap operations.

---

### Q101.
Difference between TreeMap and HashMap.

---

### Q102.
Difference between TreeSet and HashSet.

---

### Q103.
How are custom objects sorted inside TreeSet?

---

### Q104.
What happens if compareTo() is inconsistent with equals()?

---

### Q105.
When should TreeMap be avoided?

---

# 8. Comparable & Comparator

### Q106.
Difference between Comparable and Comparator.

---

### Q107.
When should Comparable be implemented?

---

### Q108.
When should Comparator be preferred?

---

### Q109.
Can multiple Comparators exist?

---

### Q110.
How do you sort custom objects?

---

### Q111.
How do you perform multi-level sorting?

---

### Q112.
How would you sort by multiple fields?

---

### Q113.
Can Comparator violate transitivity?

---

### Q114.
What happens if compare() always returns zero?

---

### Q115.
What problems occur with inconsistent comparison logic?

---

# 9. Iterators

### Q116.
Difference between Iterator and ListIterator.

---

### Q117.
Difference between Enumeration and Iterator.

---

### Q118.
How does Iterator remove() work?

---

### Q119.
Why shouldn't you modify a collection during iteration?

---

### Q120.
How does enhanced for-loop use Iterator?

---

### Q121.
When should ListIterator be preferred?

---

### Q122.
Can Iterator iterate backward?

---

### Q123.
How do you safely remove elements during iteration?

---

# 10. Fail-Fast & Fail-Safe

### Q124.
What is ConcurrentModificationException?

---

### Q125.
Explain fail-fast iterator.

---

### Q126.
Explain fail-safe iterator.

---

### Q127.
Which collections provide fail-safe iterators?

---

### Q128.
How does modCount work?

---

### Q129.
Can fail-fast guarantee detection?

---

### Q130.
Why is ConcurrentModificationException useful?

---

# 11. Complexity Analysis

### Q131.
What is the time complexity of ArrayList operations?

---

### Q132.
Complexity of LinkedList operations.

---

### Q133.
Complexity of HashMap operations.

---

### Q134.
Complexity of TreeMap operations.

---

### Q135.
Complexity of HashSet operations.

---

### Q136.
Complexity of TreeSet operations.

---

### Q137.
Complexity of PriorityQueue operations.

---

### Q138.
Which collection gives O(1) lookup?

---

### Q139.
Which collection gives O(log n) lookup?

---

### Q140.
Which collection preserves insertion order?

---

# 12. Advanced Questions

### Q141.
Why is HashMap not synchronized?

---

### Q142.
How is ConcurrentHashMap different from HashMap?

---

### Q143.
How did ConcurrentHashMap change in Java 8?

---

### Q144.
Can HashMap enter an infinite loop?

---

### Q145.
What issue existed in HashMap before Java 8?

---

### Q146.
How does LinkedHashMap implement LRU cache?

---

### Q147.
How would you implement your own HashMap?

---

### Q148.
How would you design a memory-efficient collection?

---

### Q149.
How do hash collisions affect CPU cache performance?

---

### Q150.
What collection would you choose for millions of records?

---

# 13. Scenario-Based Questions

### Q151.
Your application slows down after adding millions of entries to a HashMap. What would you investigate?

---

### Q152.
You observe frequent HashMap resizing in production. How would you optimize it?

---

### Q153.
A HashSet contains duplicate business objects. What could be wrong?

---

### Q154.
A TreeSet unexpectedly removes some objects. Why might this happen?

---

### Q155.
You need ordered unique elements with fast lookup. Which collection would you choose?

---

### Q156.
Your service performs 99% reads and 1% writes. Which collection is appropriate?

---

### Q157.
You need to maintain insertion order while eliminating duplicates. What would you use?

---

### Q158.
A REST endpoint returns data in sorted order. Would you sort at query time or use a sorted collection?

---

### Q159.
You need the top 100 highest-scoring users from millions of records. Which collection fits best?

---

### Q160.
How would you detect memory waste caused by oversized collections?

---

# 14. Production Experience Questions

### Q161.
Which collections do you use most frequently in your current project?

---

### Q162.
Have you ever optimized a slow collection operation in production?

---

### Q163.
Have you encountered hash collisions causing performance issues?

---

### Q164.
Have you overridden equals() and hashCode() for entity classes? Why?

---

### Q165.
Have you used LinkedHashMap for caching?

---

### Q166.
Have you debugged a ConcurrentModificationException in production?

---

### Q167.
How do you choose the right collection during code reviews?

---

### Q168.
What mistakes do junior developers commonly make with collections?

---

### Q169.
How do you estimate initial capacity for a HashMap?

---

### Q170.
How do you profile collection-related memory usage?

---

# 15. "Why" Questions

### Q171.
Why does HashMap allow one null key?

---

### Q172.
Why doesn't TreeMap allow null keys (natural ordering)?

---

### Q173.
Why are immutable keys preferred?

---

### Q174.
Why is ArrayList usually preferred over LinkedList?

---

### Q175.
Why is HashMap generally faster than TreeMap?

---

### Q176.
Why is load factor 0.75 the default?

---

### Q177.
Why did Java 8 introduce treeification in HashMap?

---

### Q178.
Why does HashSet internally use HashMap?

---

### Q179.
Why is Stack considered obsolete?

---

### Q180.
Why is ConcurrentModificationException fail-fast instead of automatically fixing the issue?

---

# 16. Trade-off Questions

### Q181.
ArrayList vs LinkedList.

---

### Q182.
HashMap vs TreeMap.

---

### Q183.
HashSet vs TreeSet.

---

### Q184.
HashMap vs ConcurrentHashMap.

---

### Q185.
LinkedHashMap vs HashMap.

---

### Q186.
Comparable vs Comparator.

---

### Q187.
Iterator vs Enhanced For Loop.

---

### Q188.
Queue vs Deque.

---

### Q189.
PriorityQueue vs TreeSet.

---

### Q190.
Array vs ArrayList.

---

# 17. Common Interview Follow-up Questions

## If you mention HashMap
- Explain put() internally.
- Explain get() internally.
- What is hashing?
- What is a bucket?
- What is a collision?
- What is treeification?
- Why Red-Black Tree?
- What is load factor?
- How does resizing work?
- What happens if hashCode() changes?

---

## If you mention HashSet
- How does it ensure uniqueness?
- Does it internally use HashMap?
- What value is stored in the backing HashMap?
- Can duplicates still appear?

---

## If you mention ArrayList
- How does resizing work?
- What is the growth factor?
- Why is insertion expensive?
- What is ensureCapacity()?
- What is trimToSize()?

---

## If you mention LinkedList
- Why is random access slow?
- Is it a doubly linked list?
- Memory overhead?
- When would you choose it?

---

## If you mention TreeMap
- What tree is used?
- Why not AVL Tree?
- Time complexity?
- How is balancing maintained?

---

## If you mention Comparator
- Can multiple comparators exist?
- How do you chain comparators?
- What if compare() is inconsistent?

---

## If you mention Iterator
- How does fail-fast work?
- What is modCount?
- How do you safely remove elements?
- Difference from ListIterator?

---

# Staff Engineer Discussion Questions

### Q191.
How do you decide the most appropriate collection for a new feature?

---

### Q192.
What collection misuse do you most often identify during code reviews?

---

### Q193.
How do you minimize GC pressure caused by large collections?

---

### Q194.
How would you design APIs that avoid unnecessary collection copying?

---

### Q195.
When should you return immutable collections from APIs?

---

### Q196.
How do you prevent accidental modification of shared collections?

---

### Q197.
How would you benchmark two different collection implementations?

---

### Q198.
How do collections influence overall application scalability?

---

### Q199.
What collection-related optimizations have had the biggest impact in your production systems?

---

### Q200.
If you had to redesign the Java Collections Framework today, what would you change and why?

---

# Completion Checklist

## Fundamentals
- [ ] Collection hierarchy
- [ ] Collection vs Collections
- [ ] Iterable
- [ ] Generics
- [ ] Arrays vs Collections

## List
- [ ] ArrayList
- [ ] LinkedList
- [ ] Complexity
- [ ] Internal resizing
- [ ] Capacity vs Size

## Set
- [ ] HashSet
- [ ] LinkedHashSet
- [ ] TreeSet
- [ ] Uniqueness

## Queue
- [ ] Queue
- [ ] Deque
- [ ] PriorityQueue

## Map
- [ ] HashMap
- [ ] TreeMap
- [ ] LinkedHashMap
- [ ] Hashtable

## HashMap Deep Dive
- [ ] Hashing
- [ ] Buckets
- [ ] Collisions
- [ ] Rehashing
- [ ] Treeification
- [ ] Load Factor
- [ ] Resizing
- [ ] Immutable Keys

## Sorting
- [ ] Comparable
- [ ] Comparator
- [ ] Multi-level sorting

## Iteration
- [ ] Iterator
- [ ] ListIterator
- [ ] Fail-fast
- [ ] Fail-safe

## Advanced
- [ ] ConcurrentHashMap
- [ ] Complexity analysis
- [ ] Collection selection
- [ ] Memory optimization
- [ ] Performance tuning

## Interview Readiness
- [ ] Can explain HashMap internals on a whiteboard.
- [ ] Can compare every major collection with trade-offs.
- [ ] Can justify collection choices using complexity analysis.
- [ ] Can discuss production incidents involving collections.
- [ ] Can answer follow-up questions without relying on memorized definitions.

---

**Total Questions:** 200
**Recommended Time:** 3–4 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** HashMap, ArrayList vs LinkedList, HashSet, TreeMap, Comparable vs Comparator, ConcurrentHashMap, Fail-Fast Iterators, Time Complexity