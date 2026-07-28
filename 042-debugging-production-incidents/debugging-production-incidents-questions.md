# Debugging & Production Incidents Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with 2–5 Years of Experience
>
> **Focus:** Amazon, Google, Microsoft, Uber, Netflix, LinkedIn, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Meesho
>
> **Technology Focus:** Java, Spring Boot, Microservices, Kafka, Redis, PostgreSQL, MongoDB, Kubernetes, Docker, Linux, JVM, Observability
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Production debugging is one of the most valuable skills for an SDE-2. Interviewers evaluate how you investigate failures, isolate root causes, analyze logs, use metrics and traces, prioritize fixes, communicate during incidents, and prevent recurrence.

---

# Table of Contents

## Part I — Debugging Fundamentals
1. Debugging Process
2. Root Cause Analysis (RCA)
3. Incident Severity
4. Production Mindset
5. Troubleshooting Framework

---

## Part II — Application Debugging
6. Spring Boot
7. Java
8. JVM
9. Threading
10. Memory

---

## Part III — Database Debugging
11. PostgreSQL
12. MongoDB
13. Redis
14. Connection Pools
15. Query Performance

---

## Part IV — Distributed Systems
16. Microservices
17. Kafka
18. REST APIs
19. Network Failures
20. Distributed Transactions

---

## Part V — Infrastructure
21. Docker
22. Kubernetes
23. Linux
24. Load Balancers
25. Cloud

---

## Part VI — Observability
26. Logging
27. Metrics
28. Tracing
29. Dashboards
30. Alerting

---

## Part VII — Production Incidents
31. Outages
32. High Latency
33. Memory Leaks
34. Scaling
35. Recovery

---

## Part VIII — Communication
36. Incident Response
37. Stakeholder Communication
38. On-call
39. Postmortems
40. Prevention

---

## Part IX — Real-world Scenarios
41. Incident Simulation
42. Production Case Studies
43. Troubleshooting Playbooks
44. Chaos Scenarios
45. Recovery Planning

---

## Part X — Staff Engineer Discussion
46. Incident Management
47. Platform Reliability
48. Engineering Standards
49. Operational Excellence
50. Organizational Learning

---

# 1. Debugging Fundamentals

## Basic

### Q1.
What is debugging?

---

### Q2.
What is Root Cause Analysis (RCA)?

---

### Q3.
How do you approach debugging in production?

---

### Q4.
What information do you gather first during an incident?

---

### Q5.
How do you prioritize investigation during an outage?

---

### Q6.
How do you distinguish symptoms from root causes?

---

### Q7.
How do you reproduce a production issue?

---

### Q8.
When should you avoid reproducing an issue in production?

---

### Q9.
How do you minimize customer impact while debugging?

---

### Q10.
What is your general troubleshooting framework?

---

### Q11.
How do you form and validate hypotheses?

---

### Q12.
How do you narrow down the failure domain?

---

### Q13.
What makes debugging distributed systems difficult?

---

### Q14.
What tools do you use during production debugging?

---

### Q15.
Production debugging best practices.

---

# 2. Java & Spring Boot Debugging

## Highest Priority

### Q16.
Application starts but fails health checks. Where do you begin?

---

### Q17.
A Spring Boot application suddenly starts returning HTTP 500 errors. How do you investigate?

---

### Q18.
CPU usage reaches 100%. What would you inspect?

---

### Q19.
Memory usage keeps increasing. How do you identify a memory leak?

---

### Q20.
Application startup time suddenly doubles. How would you debug it?

---

### Q21.
How do you analyze thread dumps?

---

### Q22.
How do you analyze heap dumps?

---

### Q23.
How do you identify deadlocks?

---

### Q24.
How do you diagnose excessive garbage collection?

---

### Q25.
How do you debug OutOfMemoryError?

---

### Q26.
How do you investigate high response times?

---

### Q27.
How do you debug thread pool exhaustion?

---

### Q28.
How do you debug connection pool exhaustion?

---

### Q29.
How do you identify blocking calls in reactive applications?

---

### Q30.
Spring Boot debugging best practices.

---

# 3. Database Debugging

### Q31.
Database CPU suddenly spikes. What would you check?

---

### Q32.
Queries become slow after deployment. How would you investigate?

---

### Q33.
How do you debug missing indexes?

---

### Q34.
Connection pool exhaustion.

---

### Q35.
Deadlocks in PostgreSQL.

---

### Q36.
Lock contention.

---

### Q37.
Slow MongoDB aggregation.

---

### Q38.
Redis latency suddenly increases.

---

### Q39.
Cache misses increase dramatically.

---

### Q40.
Database debugging best practices.

---

# 4. Distributed Systems Debugging

### Q41.
One microservice becomes significantly slower than others.

---

### Q42.
A downstream dependency starts timing out.

---

### Q43.
A circuit breaker begins opening continuously.

---

### Q44.
Kafka consumer lag increases rapidly.

---

### Q45.
Kafka messages are duplicated.

---

### Q46.
Events stop flowing between services.

---

### Q47.
How do you debug distributed transactions?

---

### Q48.
How do you debug eventual consistency issues?

---

### Q49.
How do you investigate API failures across services?

---

### Q50.
Distributed debugging best practices.

---

# 5. Kubernetes & Infrastructure

### Q51.
Pods repeatedly restart.

---

### Q52.
CrashLoopBackOff investigation.

---

### Q53.
OOMKilled investigation.

---

### Q54.
Pending Pods.

---

### Q55.
Node resource exhaustion.

---

### Q56.
Readiness probe failures.

---

### Q57.
Ingress routing failures.

---

### Q58.
DNS failures.

---

### Q59.
Container image issues.

---

### Q60.
Infrastructure debugging best practices.

---

# 6. Observability

## Highest Priority

### Q61.
Which logs do you check first?

---

### Q62.
Which metrics matter most?

---

### Q63.
How do traces help debugging?

---

### Q64.
Correlation IDs.

---

### Q65.
Distributed tracing.

---

### Q66.
Grafana dashboards.

---

### Q67.
Prometheus metrics.

---

### Q68.
Alert fatigue.

---

### Q69.
Log sampling.

---

### Q70.
Observability best practices.

---

# 7. Production Incident Scenarios

### Q71.
Latency doubles immediately after deployment.

---

### Q72.
Production returns intermittent HTTP 500 errors.

---

### Q73.
Memory usage continuously increases.

---

### Q74.
A Kafka topic backlog reaches millions of messages.

---

### Q75.
One database replica becomes unavailable.

---

### Q76.
Redis suddenly becomes unavailable.

---

### Q77.
Users experience random authentication failures.

---

### Q78.
The application is healthy but users cannot access it.

---

### Q79.
An entire Kubernetes node becomes unavailable.

---

### Q80.
How do you recover a degraded production system?

---

# 8. Production Experience Questions

### Q81.
Describe the most difficult production incident you've handled.

---

### Q82.
How did you identify the root cause?

---

### Q83.
What tools did you use?

---

### Q84.
How long did the investigation take?

---

### Q85.
What was the business impact?

---

### Q86.
How did you communicate during the incident?

---

### Q87.
What preventive measures were implemented afterward?

---

### Q88.
Describe an incident caused by your own code.

---

### Q89.
Describe a deployment rollback.

---

### Q90.
What production metrics do you monitor daily?

---

# 9. Scenario-Based Questions

### Q91.
A deployment succeeds but customer traffic immediately drops by 40%.

---

### Q92.
CPU usage spikes only on one instance.

---

### Q93.
Memory usage is normal, but latency increases continuously.

---

### Q94.
Only one customer is affected. How do you investigate?

---

### Q95.
A deployment causes intermittent failures that disappear after retries.

---

### Q96.
A service works locally but fails only in production.

---

### Q97.
One region experiences failures while another is healthy.

---

### Q98.
A cache cluster becomes unavailable.

---

### Q99.
Logs show no obvious errors, but users report failures.

---

### Q100.
How would you lead an incident bridge during a Sev-1 outage?

---

# 10. "Why" Questions

### Q101.
Why should you avoid making multiple changes during debugging?

---

### Q102.
Why should production incidents have a single incident commander?

---

### Q103.
Why are metrics insufficient without logs?

---

### Q104.
Why are logs insufficient without traces?

---

### Q105.
Why should every incident have a postmortem?

---

### Q106.
Why should incidents be blameless?

---

### Q107.
Why is rollback usually safer than patching live systems?

---

### Q108.
Why should runbooks exist?

---

### Q109.
Why should alerts be actionable?

---

### Q110.
Why should production fixes be followed by permanent solutions?

---

# 11. Trade-off Questions

### Q111.
Restart vs Rollback.

---

### Q112.
Horizontal Scaling vs Vertical Scaling.

---

### Q113.
Fail Fast vs Graceful Degradation.

---

### Q114.
Logs vs Metrics vs Traces.

---

### Q115.
Hotfix vs Full Release.

---

### Q116.
Feature Flag Disable vs Rollback.

---

### Q117.
Manual Investigation vs Automated Detection.

---

### Q118.
Circuit Breaker vs Retry.

---

### Q119.
Immediate Recovery vs Full RCA.

---

### Q120.
Availability vs Consistency during incidents.

---

# 12. Common Interview Follow-up Questions

## If you mention RCA
- Five Whys?
- Fishbone Analysis?
- Corrective actions?
- Preventive actions?
- Postmortem?

---

## If you mention Kubernetes
- CrashLoopBackOff?
- OOMKilled?
- Readiness probe?
- Logs?
- kubectl commands?

---

## If you mention JVM
- Heap dump?
- Thread dump?
- GC logs?
- JFR?
- VisualVM?

---

## If you mention Kafka
- Consumer lag?
- Rebalancing?
- Offsets?
- Dead-letter topics?
- Broker metrics?

---

## If you mention Production
- Incident timeline?
- Stakeholder communication?
- Rollback?
- Monitoring?
- Prevention?

---

# Staff Engineer Discussion Questions

### Q121.
How would you build an organization-wide incident management process?

---

### Q122.
How would you reduce Mean Time To Detect (MTTD)?

---

### Q123.
How would you reduce Mean Time To Recovery (MTTR)?

---

### Q124.
How would you standardize postmortems across engineering teams?

---

### Q125.
How would you improve operational excellence across hundreds of services?

---

### Q126.
How would you design a company-wide on-call process?

---

### Q127.
How would you identify recurring production issues automatically?

---

### Q128.
How would you prioritize reliability engineering work?

---

### Q129.
Which operational metrics would you review weekly?

---

### Q130.
If you were responsible for platform reliability, what production standards would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Debugging Framework
- [ ] Root Cause Analysis
- [ ] Incident Prioritization
- [ ] Troubleshooting Process
- [ ] Hypothesis-Driven Debugging

## JVM & Spring
- [ ] Heap Dumps
- [ ] Thread Dumps
- [ ] GC Analysis
- [ ] Thread Pools
- [ ] Connection Pools

## Databases
- [ ] Slow Queries
- [ ] Locks
- [ ] Deadlocks
- [ ] MongoDB
- [ ] Redis

## Distributed Systems
- [ ] Kafka
- [ ] Microservices
- [ ] REST APIs
- [ ] Timeouts
- [ ] Eventual Consistency

## Kubernetes
- [ ] CrashLoopBackOff
- [ ] OOMKilled
- [ ] Pod Debugging
- [ ] Ingress
- [ ] Networking

## Observability
- [ ] Logs
- [ ] Metrics
- [ ] Traces
- [ ] Dashboards
- [ ] Alerts

## Incident Response
- [ ] RCA
- [ ] Rollbacks
- [ ] Postmortems
- [ ] Runbooks
- [ ] Stakeholder Communication

## Interview Readiness
- [ ] Can systematically debug production issues under pressure.
- [ ] Can analyze JVM, database, Kubernetes, and distributed system failures.
- [ ] Can explain real production incidents with clear RCA and preventive actions.
- [ ] Can lead incident response and communicate effectively with stakeholders.
- [ ] Can design operational processes to improve reliability and reduce MTTR.

---

**Total Questions:** **130** *(Recommended expansion: 220–250 for a flagship repository)*

**Recommended Study Time:** **6–8 Days**

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** Root Cause Analysis, JVM Debugging, Heap Dumps, Thread Dumps, Kafka Consumer Lag, Database Performance, CrashLoopBackOff, OOMKilled, Logs vs Metrics vs Traces, Incident Response, MTTR, Postmortems, Production Outages