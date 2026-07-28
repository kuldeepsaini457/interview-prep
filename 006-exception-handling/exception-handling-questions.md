# Exception Handling Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Interview Weight:** ⭐⭐⭐⭐☆ (High)
>
> Exception Handling is heavily tested in Java backend interviews because it reflects code quality, API design, production debugging, transaction management, and distributed system resilience.

---

# Table of Contents

1. Exception Fundamentals
2. Exception Hierarchy
3. Checked vs Unchecked Exceptions
4. try-catch-finally
5. throw vs throws
6. Custom Exceptions
7. Exception Propagation
8. Try-with-Resources
9. Suppressed Exceptions
10. Exception Handling Best Practices
11. Spring Boot Exception Handling
12. Transactions & Exceptions
13. Logging Exceptions
14. Intermediate Questions
15. Advanced Questions
16. Scenario-Based Questions
17. Production Experience
18. Why Questions
19. Trade-offs
20. Common Follow-up Questions

---

# 1. Exception Fundamentals

## Basic

### Q1.
What is an exception?

**Follow-ups**
- Why do we need exception handling?
- What problems does it solve?

---

### Q2.
Difference between Exception and Error.

---

### Q3.
What is Throwable?

---

### Q4.
Explain the Java exception hierarchy.

---

### Q5.
What happens when an exception occurs?

---

### Q6.
What is stack unwinding?

---

### Q7.
What is a stack trace?

---

### Q8.
Can a program continue after an exception?

---

### Q9.
What happens if an exception is never caught?

---

### Q10.
Difference between compile-time and runtime exceptions.

---

# 2. Exception Hierarchy

## Basic

### Q11.
Draw the exception hierarchy.

---

### Q12.
Difference between Error and Exception.

---

### Q13.
Difference between Exception and RuntimeException.

---

### Q14.
Examples of checked exceptions.

---

### Q15.
Examples of unchecked exceptions.

---

### Q16.
Examples of Errors.

---

### Q17.
Should applications catch Error?

---

### Q18.
Can RuntimeException be ignored?

---

### Q19.
Can checked exceptions occur at runtime?

---

### Q20.
Can unchecked exceptions be declared with throws?

---

# 3. Checked vs Unchecked Exceptions

## Intermediate

### Q21.
Difference between checked and unchecked exceptions.

---

### Q22.
When should checked exceptions be used?

---

### Q23.
When should unchecked exceptions be preferred?

---

### Q24.
Why are RuntimeExceptions called unchecked?

---

### Q25.
Why did Java introduce checked exceptions?

---

### Q26.
Criticisms of checked exceptions.

---

### Q27.
Why do many modern frameworks prefer RuntimeException?

---

### Q28.
Should business validation failures use checked or unchecked exceptions?

---

### Q29.
Should REST APIs expose checked exceptions?

---

### Q30.
When would you convert a checked exception into an unchecked exception?

---

# 4. try-catch-finally

## Basic

### Q31.
How does try-catch work?

---

### Q32.
Can a try block exist without catch?

---

### Q33.
Can a try block exist without finally?

---

### Q34.
Can finally exist without catch?

---

### Q35.
When is finally executed?

---

### Q36.
Can finally block be skipped?

---

### Q37.
What happens if finally throws an exception?

---

### Q38.
Can multiple catch blocks exist?

---

### Q39.
Why should catch blocks be ordered from specific to general?

---

### Q40.
What happens if the order is incorrect?

---

### Q41.
Can one catch block catch multiple exception types?

---

### Q42.
How does multi-catch work?

---

### Q43.
Can you rethrow an exception?

---

### Q44.
What happens when you throw an exception inside catch?

---

### Q45.
Can return statements inside finally cause problems?

---

# 5. throw vs throws

### Q46.
Difference between throw and throws.

---

### Q47.
When should throw be used?

---

### Q48.
When should throws be used?

---

### Q49.
Can methods declare multiple exceptions?

---

### Q50.
Can overridden methods throw broader exceptions?

---

### Q51.
Exception rules during method overriding.

---

### Q52.
Can constructors throw exceptions?

---

### Q53.
Can main() throw exceptions?

---

### Q54.
Can interfaces declare throws?

---

### Q55.
How should APIs document exceptions?

---

# 6. Custom Exceptions

## Intermediate

### Q56.
Why create custom exceptions?

---

### Q57.
How do you design a custom exception?

---

### Q58.
Should custom exceptions extend Exception or RuntimeException?

---

### Q59.
How many custom exceptions are too many?

---

### Q60.
Should custom exceptions include error codes?

---

### Q61.
Should custom exceptions carry business data?

---

### Q62.
How do you preserve the original cause?

---

### Q63.
Difference between wrapping and replacing exceptions.

---

### Q64.
How should exception names be chosen?

---

### Q65.
How do you organize exception classes in large applications?

---

# 7. Exception Propagation

## Intermediate

### Q66.
How does exception propagation work?

---

### Q67.
What is stack unwinding?

---

### Q68.
How does the JVM search for a matching catch block?

---

### Q69.
Can exceptions cross thread boundaries?

---

### Q70.
How do exceptions propagate in ExecutorService?

---

### Q71.
How do exceptions propagate through Future?

---

### Q72.
How do exceptions propagate through CompletableFuture?

---

### Q73.
How do async exceptions differ from synchronous exceptions?

---

### Q74.
Can exceptions propagate across microservices?

---

### Q75.
How should distributed systems propagate errors?

---

# 8. Try-with-Resources

## Intermediate

### Q76.
What is try-with-resources?

---

### Q77.
Why was try-with-resources introduced?

---

### Q78.
Which objects can be used with try-with-resources?

---

### Q79.
What is AutoCloseable?

---

### Q80.
Difference between Closeable and AutoCloseable.

---

### Q81.
How does JVM close resources automatically?

---

### Q82.
What happens if close() throws an exception?

---

### Q83.
Multiple resources in try-with-resources.

---

### Q84.
Resource closing order.

---

### Q85.
Why is try-with-resources preferred over finally?

---

# 9. Suppressed Exceptions

## Advanced

### Q86.
What are suppressed exceptions?

---

### Q87.
Why were suppressed exceptions introduced?

---

### Q88.
How do suppressed exceptions occur?

---

### Q89.
How do you retrieve suppressed exceptions?

---

### Q90.
How do try-with-resources use suppressed exceptions?

---

# 10. Exception Handling Best Practices

### Q91.
What are common exception handling best practices?

---

### Q92.
Why should exceptions not be swallowed?

---

### Q93.
Why is catching Exception generally discouraged?

---

### Q94.
Why is catching Throwable dangerous?

---

### Q95.
Why should exceptions include meaningful messages?

---

### Q96.
Should exceptions be logged everywhere?

---

### Q97.
How many times should an exception be logged?

---

### Q98.
Why should exceptions preserve the original cause?

---

### Q99.
Should exceptions be used for control flow?

---

### Q100.
How do you design exception hierarchies?

---

# 11. Spring Boot Exception Handling

## Intermediate

### Q101.
How does Spring Boot handle uncaught exceptions?

---

### Q102.
What is @ExceptionHandler?

---

### Q103.
What is @ControllerAdvice?

---

### Q104.
Difference between @ExceptionHandler and @ControllerAdvice.

---

### Q105.
How do you create a global exception handler?

---

### Q106.
How do you return proper HTTP status codes?

---

### Q107.
How do you return standardized error responses?

---

### Q108.
How should validation exceptions be handled?

---

### Q109.
How should business exceptions be mapped to HTTP responses?

---

### Q110.
How do you avoid exposing internal exception details?

---

# 12. Transactions & Exceptions

## Advanced

### Q111.
How do exceptions affect Spring transactions?

---

### Q112.
Which exceptions trigger rollback by default?

---

### Q113.
Why doesn't Spring roll back checked exceptions by default?

---

### Q114.
How does rollbackFor work?

---

### Q115.
How do nested transactions behave during exceptions?

---

### Q116.
What happens when an exception is caught inside a transactional method?

---

### Q117.
How can catching an exception accidentally prevent rollback?

---

### Q118.
How should transaction boundaries influence exception handling?

---

### Q119.
How should exceptions be handled in Saga-based systems?

---

### Q120.
How should distributed transactions propagate failures?

---

# 13. Logging Exceptions

### Q121.
How should exceptions be logged?

---

### Q122.
What information should be logged?

---

### Q123.
Should stack traces always be logged?

---

### Q124.
Should sensitive information be included in exception messages?

---

### Q125.
How do structured logs help debugging?

---

### Q126.
How do correlation IDs improve exception tracking?

---

### Q127.
How do distributed tracing systems capture exceptions?

---

### Q128.
How do logging frameworks handle exceptions?

---

### Q129.
How should production logging differ from development logging?

---

### Q130.
How do you avoid duplicate exception logs?

---

# 14. Advanced Questions

### Q131.
Exception chaining.

---

### Q132.
initCause().

---

### Q133.
Stack trace generation overhead.

---

### Q134.
Performance impact of exceptions.

---

### Q135.
Why are exceptions expensive?

---

### Q136.
FastThrow optimization.

---

### Q137.
StackWalker API.

---

### Q138.
Exceptions inside Streams.

---

### Q139.
Exceptions inside Lambda expressions.

---

### Q140.
Exception handling in Parallel Streams.

---

### Q141.
Exceptions inside CompletableFuture chains.

---

### Q142.
How should retry mechanisms interact with exceptions?

---

### Q143.
Circuit Breakers and exception handling.

---

### Q144.
Exception translation pattern.

---

### Q145.
DAO exception translation in Spring.

---

### Q146.
How does Spring convert SQLExceptions into DataAccessException?

---

### Q147.
Should APIs expose implementation-specific exceptions?

---

### Q148.
Domain exceptions vs infrastructure exceptions.

---

### Q149.
Recoverable vs unrecoverable exceptions.

---

### Q150.
Fail-fast vs fail-safe exception handling.

---

# 15. Scenario-Based Questions

### Q151.
Your REST API returns HTTP 500 for every exception. How would you redesign the exception handling strategy?

---

### Q152.
A service catches Exception and ignores it. What risks does this create?

---

### Q153.
A transaction commits even though an error occurred. What could be the cause?

---

### Q154.
Your application logs the same exception five times. How would you fix it?

---

### Q155.
A downstream microservice is unavailable. How should your service handle the exception?

---

### Q156.
A file upload leaves file handles open after failures. How would you redesign the code?

---

### Q157.
An asynchronous task fails silently. How would you detect and handle the failure?

---

### Q158.
Users receive detailed SQL exception messages in API responses. Why is this a problem?

---

### Q159.
A retry mechanism repeatedly retries a validation error. What is wrong with this design?

---

### Q160.
A production incident reveals thousands of swallowed exceptions. How would you investigate and prevent this in the future?

---

# 16. Production Experience Questions

### Q161.
Have you implemented global exception handling in Spring Boot?

---

### Q162.
Have you designed custom business exceptions?

---

### Q163.
Have you debugged transaction rollback issues?

---

### Q164.
Have you investigated production failures using stack traces?

---

### Q165.
How do you standardize error responses across microservices?

---

### Q166.
Have you used exception translation in DAO or service layers?

---

### Q167.
Have you optimized code that relied heavily on exceptions?

---

### Q168.
Have you integrated exception handling with monitoring systems?

---

### Q169.
How do you test exception scenarios?

---

### Q170.
What production incident taught you the most about exception handling?

---

# 17. "Why" Questions

### Q171.
Why are checked exceptions controversial?

---

### Q172.
Why are RuntimeExceptions preferred in Spring applications?

---

### Q173.
Why should exceptions preserve the root cause?

---

### Q174.
Why shouldn't exceptions be swallowed?

---

### Q175.
Why shouldn't exceptions be used for normal control flow?

---

### Q176.
Why is try-with-resources preferred?

---

### Q177.
Why are exceptions expensive compared to normal execution?

---

### Q178.
Why should APIs return business-friendly error messages instead of stack traces?

---

### Q179.
Why should logging happen only once?

---

### Q180.
Why are global exception handlers considered a best practice?

---

# 18. Trade-off Questions

### Q181.
Checked Exception vs RuntimeException.

---

### Q182.
Custom Exception vs Generic Exception.

---

### Q183.
Exception vs Optional.

---

### Q184.
Exception vs Error Code.

---

### Q185.
Fail Fast vs Graceful Degradation.

---

### Q186.
Local Exception Handling vs Global Exception Handling.

---

### Q187.
Wrapping Exceptions vs Rethrowing Original Exceptions.

---

### Q188.
Retry vs Immediate Failure.

---

### Q189.
Validation Exception vs Business Exception.

---

### Q190.
Logging at Service Layer vs Controller Layer.

---

# 19. Common Interview Follow-up Questions

## If you mention Checked Exceptions
- Why were they introduced?
- Why are they controversial?
- Why does Spring prefer RuntimeException?
- When would you still use them?

---

## If you mention RuntimeException
- Rollback behavior?
- Business validation?
- Framework usage?
- Best practices?

---

## If you mention finally
- Can it be skipped?
- What if finally throws?
- Return inside finally?
- System.exit()?

---

## If you mention try-with-resources
- AutoCloseable?
- Suppressed exceptions?
- Closing order?
- Difference from finally?

---

## If you mention Spring Exception Handling
- @ControllerAdvice?
- @ExceptionHandler?
- ErrorResponse?
- Validation?
- HTTP status mapping?

---

## If you mention Transactions
- Rollback rules?
- Checked exceptions?
- rollbackFor?
- Nested transactions?
- Catching exceptions?

---

# Staff Engineer Discussion Questions

### Q191.
How would you design a consistent exception handling strategy across dozens of microservices?

---

### Q192.
How do you separate business exceptions from infrastructure exceptions?

---

### Q193.
How would you balance observability and security when exposing API errors?

---

### Q194.
How should retries, circuit breakers, and exception handling work together?

---

### Q195.
How would you design an organization-wide error response standard?

---

### Q196.
How do you ensure exceptions provide enough debugging information without leaking sensitive data?

---

### Q197.
How would you review a codebase for poor exception handling practices?

---

### Q198.
What metrics would you monitor to detect exception-related production issues?

---

### Q199.
How do exception handling strategies evolve as a system grows into a distributed architecture?

---

### Q200.
If you were designing Java's exception mechanism today, what would you change and why?

---

# Completion Checklist

## Fundamentals
- [ ] Exception Hierarchy
- [ ] Throwable
- [ ] Error vs Exception
- [ ] Checked vs Unchecked
- [ ] Stack Unwinding

## Core Language Features
- [ ] try-catch-finally
- [ ] throw vs throws
- [ ] Multi-catch
- [ ] Rethrowing
- [ ] Exception Propagation

## Modern Java
- [ ] Try-with-Resources
- [ ] AutoCloseable
- [ ] Suppressed Exceptions
- [ ] Exception Chaining

## Spring Boot
- [ ] @ExceptionHandler
- [ ] @ControllerAdvice
- [ ] Global Exception Handling
- [ ] Error Responses
- [ ] Validation Errors

## Transactions
- [ ] Rollback Rules
- [ ] rollbackFor
- [ ] Checked vs Runtime Rollback
- [ ] Nested Transactions

## Production
- [ ] Logging Strategy
- [ ] Monitoring
- [ ] Distributed Error Handling
- [ ] Retry & Circuit Breaker
- [ ] Security of Error Messages

## Interview Readiness
- [ ] Can explain the full exception hierarchy.
- [ ] Can compare checked and unchecked exceptions with real-world examples.
- [ ] Can design a global exception handling strategy for Spring Boot.
- [ ] Can explain transaction rollback behavior with exceptions.
- [ ] Can discuss production incidents involving exception handling and debugging.

---

**Total Questions:** 200
**Recommended Time:** 2–3 Days
**Interview Weight:** ⭐⭐⭐⭐☆ (High)
**Most Frequently Asked Topics:** Checked vs Unchecked Exceptions, try-catch-finally, try-with-resources, Custom Exceptions, Spring Global Exception Handling, Transaction Rollback, Exception Propagation, Logging Best Practices