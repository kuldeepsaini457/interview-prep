# Testing Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with 2–5 Years of Experience
>
> **Focus:** Amazon, Google, Microsoft, Uber, LinkedIn, Netflix, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Meesho, etc.
>
> **Technology Focus:** Java, Spring Boot, JUnit 5, Mockito, Testcontainers, Integration Testing, TDD, Microservices
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Modern backend interviews expect engineers to understand not only how to write code but also how to verify its correctness. This guide covers unit testing, integration testing, contract testing, performance testing, testing in distributed systems, Testcontainers, CI/CD testing, and production testing strategies.

---

# Table of Contents

## Part I — Testing Fundamentals
1. Software Testing Basics
2. Testing Pyramid
3. Test Types
4. Test Design Principles
5. Test Coverage

---

## Part II — Unit Testing
6. JUnit 5
7. Assertions
8. Lifecycle Methods
9. Parameterized Tests
10. Dynamic Tests
11. Nested Tests
12. Exception Testing
13. Time-based Testing

---

## Part III — Mockito
14. Mocking
15. Stubbing
16. Verification
17. Argument Matchers
18. Argument Captors
19. Spies
20. Static Mocking
21. MockBean & SpyBean

---

## Part IV — Spring Boot Testing
22. @SpringBootTest
23. WebMvcTest
24. DataJpaTest
25. JsonTest
26. RestClientTest
27. Context Configuration
28. Test Slices
29. Embedded Servers

---

## Part V — Integration Testing
30. Database Testing
31. REST API Testing
32. Kafka Testing
33. Redis Testing
34. MongoDB Testing
35. PostgreSQL Testing
36. Testcontainers
37. End-to-End Testing

---

## Part VI — Microservices Testing
38. Contract Testing
39. Consumer Driven Contracts
40. WireMock
41. Mock Servers
42. API Gateway Testing
43. Distributed Transactions
44. Event Testing

---

## Part VII — Advanced Testing
45. TDD
46. BDD
47. Mutation Testing
48. Property-Based Testing
49. Snapshot Testing
50. Chaos Testing
51. Load Testing
52. Stress Testing

---

## Part VIII — CI/CD Testing
53. Test Automation
54. Pipeline Testing
55. Test Reporting
56. Flaky Tests
57. Parallel Test Execution

---

## Part IX — Production Testing
58. Canary Testing
59. Feature Flags
60. Shadow Testing
61. Synthetic Monitoring
62. Smoke Testing
63. Health Checks

---

## Part X — Scenario-Based Questions
64. Production Scenarios
65. Debugging Test Failures
66. Legacy Code Testing
67. Large Codebase Testing

---

## Part XI — Production Experience
68. Real Testing Stories
69. Team Practices
70. Code Review Discussions

---

## Part XII — Trade-offs
71. Unit vs Integration
72. Mock vs Real Dependencies
73. Testcontainers vs Embedded DB
74. TDD vs Test-Last

---

## Part XIII — Staff Engineer Discussion
75. Organization-wide Testing Strategy
76. Test Infrastructure
77. Engineering Standards

---

# 1. Testing Fundamentals

## Basic

### Q1.
What is software testing?

**Follow-ups**
- Why is testing important?
- What problems does testing solve?

---

### Q2.
What are the different types of software testing?

---

### Q3.
What is the Testing Pyramid?

---

### Q4.
Explain the Testing Trophy.

---

### Q5.
Unit Testing vs Integration Testing.

---

### Q6.
Integration Testing vs End-to-End Testing.

---

### Q7.
Functional vs Non-functional Testing.

---

### Q8.
Regression Testing.

---

### Q9.
Smoke Testing.

---

### Q10.
Sanity Testing.

---

### Q11.
Acceptance Testing.

---

### Q12.
Black Box vs White Box Testing.

---

### Q13.
Manual Testing vs Automated Testing.

---

### Q14.
Shift Left Testing.

---

### Q15.
What should NOT be unit tested?

---

### Q16.
Characteristics of a good test.

---

### Q17.
FIRST principles of testing.

---

### Q18.
Arrange-Act-Assert pattern.

---

### Q19.
What is code coverage?

---

### Q20.
Is 100% code coverage sufficient?

---

# 2. Unit Testing (JUnit 5)

## Highest Priority

### Q21.
What is JUnit 5?

---

### Q22.
JUnit 4 vs JUnit 5.

---

### Q23.
@Test annotation.

---

### Q24.
@BeforeEach vs @BeforeAll.

---

### Q25.
@AfterEach vs @AfterAll.

---

### Q26.
Assertions.

---

### Q27.
assertThrows().

---

### Q28.
assertAll().

---

### Q29.
assertTimeout().

---

### Q30.
Parameterized Tests.

---

### Q31.
Dynamic Tests.

---

### Q32.
Nested Tests.

---

### Q33.
Repeated Tests.

---

### Q34.
Test lifecycle.

---

### Q35.
Test naming conventions.

---

### Q36.
How do you test private methods?

---

### Q37.
How do you test exceptions?

---

### Q38.
How do you test time-dependent code?

---

### Q39.
How do you test random values?

---

### Q40.
Unit testing best practices.

---

# 3. Mockito

## Highest Priority

### Q41.
What is Mockito?

---

### Q42.
Mock vs Stub.

---

### Q43.
Mock vs Spy.

---

### Q44.
when() vs doReturn().

---

### Q45.
verify().

---

### Q46.
Argument Matchers.

---

### Q47.
ArgumentCaptor.

---

### Q48.
BDDMockito.

---

### Q49.
@Mock.

---

### Q50.
@InjectMocks.

---

### Q51.
@Spy.

---

### Q52.
@Captor.

---

### Q53.
Mocking void methods.

---

### Q54.
Mocking exceptions.

---

### Q55.
Mocking static methods.

---

### Q56.
Mocking final classes.

---

### Q57.
MockitoExtension.

---

### Q58.
Common Mockito mistakes.

---

### Q59.
Over-mocking.

---

### Q60.
Mockito best practices.

---

# 4. Spring Boot Testing

### Q61.
@SpringBootTest.

---

### Q62.
@WebMvcTest.

---

### Q63.
@DataJpaTest.

---

### Q64.
@JsonTest.

---

### Q65.
@RestClientTest.

---

### Q66.
@TestConfiguration.

---

### Q67.
@MockBean.

---

### Q68.
@SpyBean.

---

### Q69.
Testing Controllers.

---

### Q70.
Testing Services.

---

### Q71.
Testing Repositories.

---

### Q72.
Testing Security.

---

### Q73.
Testing Validation.

---

### Q74.
Testing Exception Handlers.

---

### Q75.
Spring Boot testing best practices.

---

# 5. Integration Testing

## Highest Priority

### Q76.
What is Integration Testing?

---

### Q77.
Testing with real databases.

---

### Q78.
H2 vs PostgreSQL in tests.

---

### Q79.
Testing MongoDB.

---

### Q80.
Testing Redis.

---

### Q81.
Testing Kafka.

---

### Q82.
Testing RabbitMQ.

---

### Q83.
REST API Integration Tests.

---

### Q84.
Database migration testing.

---

### Q85.
Transaction rollback during tests.

---

### Q86.
Testcontainers.

---

### Q87.
Why Testcontainers instead of embedded databases?

---

### Q88.
Container lifecycle.

---

### Q89.
Docker dependency.

---

### Q90.
Integration testing best practices.

---

# 6. Microservices Testing

### Q91.
Testing microservices.

---

### Q92.
Contract Testing.

---

### Q93.
Consumer Driven Contracts.

---

### Q94.
Spring Cloud Contract.

---

### Q95.
WireMock.

---

### Q96.
MockWebServer.

---

### Q97.
Testing asynchronous APIs.

---

### Q98.
Testing Kafka consumers.

---

### Q99.
Testing Kafka producers.

---

### Q100.
Testing Saga workflows.

---

### Q101.
Testing distributed transactions.

---

### Q102.
Testing eventual consistency.

---

### Q103.
Testing retries.

---

### Q104.
Testing circuit breakers.

---

### Q105.
Microservice testing best practices.

---

# 7. Advanced Testing

### Q106.
Test Driven Development (TDD).

---

### Q107.
Red-Green-Refactor.

---

### Q108.
Behavior Driven Development (BDD).

---

### Q109.
Mutation Testing.

---

### Q110.
Property-Based Testing.

---

### Q111.
Snapshot Testing.

---

### Q112.
Golden Master Testing.

---

### Q113.
Chaos Testing.

---

### Q114.
Fault Injection Testing.

---

### Q115.
Load Testing.

---

### Q116.
Stress Testing.

---

### Q117.
Spike Testing.

---

### Q118.
Soak Testing.

---

### Q119.
Performance Benchmarking.

---

### Q120.
Advanced testing best practices.

---

# 8. CI/CD Testing

### Q121.
Testing in CI/CD pipelines.

---

### Q122.
Fast feedback principle.

---

### Q123.
Parallel test execution.

---

### Q124.
Flaky tests.

---

### Q125.
Test retries.

---

### Q126.
Test reporting.

---

### Q127.
Coverage reporting.

---

### Q128.
Pipeline optimization.

---

### Q129.
Build failures.

---

### Q130.
CI testing best practices.

---

# 9. Production Testing

### Q131.
Canary testing.

---

### Q132.
Blue-Green validation.

---

### Q133.
Shadow Testing.

---

### Q134.
Feature Flag testing.

---

### Q135.
Health checks.

---

### Q136.
Synthetic monitoring.

---

### Q137.
Smoke tests after deployment.

---

### Q138.
Production verification.

---

### Q139.
Rollback validation.

---

### Q140.
Production testing best practices.

---

# 10. Scenario-Based Questions

### Q141.
A flaky integration test fails randomly. How would you investigate?

---

### Q142.
Your unit tests pass but production fails. What could be the reasons?

---

### Q143.
A Spring Boot test suite takes 30 minutes to execute. How would you optimize it?

---

### Q144.
How would you test a payment service interacting with multiple external providers?

---

### Q145.
How would you test a Kafka-based event-driven architecture?

---

### Q146.
How would you test a distributed Saga?

---

### Q147.
How would you verify cache consistency using Redis?

---

### Q148.
How would you test retry and circuit breaker logic?

---

### Q149.
How would you introduce tests into a legacy codebase with almost no test coverage?

---

### Q150.
How would you review tests during a code review?

---

# 11. Production Experience Questions

### Q151.
What testing strategy do you follow in your current project?

---

### Q152.
What percentage of your code is covered by unit tests?

---

### Q153.
Have you written integration tests using Testcontainers?

---

### Q154.
How do you test Spring Boot microservices?

---

### Q155.
How do you test Kafka consumers?

---

### Q156.
How do you test MongoDB repositories?

---

### Q157.
How do you prevent flaky tests?

---

### Q158.
How do you speed up CI test execution?

---

### Q159.
What testing practices does your team follow?

---

### Q160.
Describe a production bug that your tests failed to catch.

---

# 12. "Why" Questions

### Q161.
Why are unit tests faster than integration tests?

---

### Q162.
Why shouldn't everything be mocked?

---

### Q163.
Why should integration tests use real infrastructure whenever possible?

---

### Q164.
Why are flaky tests dangerous?

---

### Q165.
Why should tests be deterministic?

---

### Q166.
Why should each test verify a single behavior?

---

### Q167.
Why should production bugs become automated tests?

---

### Q168.
Why should tests avoid implementation details?

---

### Q169.
Why is Testcontainers becoming the industry standard?

---

### Q170.
Why is code coverage an imperfect metric?

---

# 13. Trade-off Questions

### Q171.
Unit Testing vs Integration Testing.

---

### Q172.
Integration Testing vs End-to-End Testing.

---

### Q173.
Mock vs Spy.

---

### Q174.
MockBean vs SpyBean.

---

### Q175.
Testcontainers vs Embedded Database.

---

### Q176.
WireMock vs MockWebServer.

---

### Q177.
TDD vs Test-Last Development.

---

### Q178.
BDD vs TDD.

---

### Q179.
JUnit vs TestNG.

---

### Q180.
High Coverage vs High Confidence.

---

# 14. Common Interview Follow-up Questions

## If you mention Unit Testing
- JUnit lifecycle?
- Assertions?
- Parameterized tests?
- Exception testing?
- Time-based testing?

---

## If you mention Mockito
- Mock vs Spy?
- verify()?
- ArgumentCaptor?
- Static mocking?
- Over-mocking?

---

## If you mention Spring Testing
- @SpringBootTest?
- @MockBean?
- @WebMvcTest?
- Test slices?
- Context caching?

---

## If you mention Integration Testing
- Testcontainers?
- Real databases?
- Kafka testing?
- Rollback?
- Docker?

---

## If you mention TDD
- Red-Green-Refactor?
- Unit first?
- Refactoring?
- Legacy code?
- Productivity?

---

## If you mention Production Testing
- Canary?
- Shadow testing?
- Smoke tests?
- Feature flags?
- Rollback?

---

# Staff Engineer Discussion Questions

### Q181.
How would you establish testing standards across hundreds of microservices?

---

### Q182.
How would you reduce CI execution time without reducing confidence?

---

### Q183.
How would you design a testing strategy for a distributed payment platform?

---

### Q184.
How would you measure testing effectiveness across engineering teams?

---

### Q185.
How would you enforce testing quality during code reviews?

---

### Q186.
How would you introduce testing into a legacy monolith?

---

### Q187.
How would you standardize Testcontainers usage organization-wide?

---

### Q188.
How would you design a scalable test infrastructure?

---

### Q189.
Which testing metrics would you continuously monitor?

---

### Q190.
If you were defining testing standards for a large engineering organization, what principles would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Testing Pyramid
- [ ] Test Types
- [ ] FIRST Principles
- [ ] Code Coverage
- [ ] AAA Pattern

## Unit Testing
- [ ] JUnit 5
- [ ] Assertions
- [ ] Parameterized Tests
- [ ] Exception Testing
- [ ] Lifecycle Methods

## Mockito
- [ ] Mock
- [ ] Spy
- [ ] Verification
- [ ] ArgumentCaptor
- [ ] Static Mocking

## Spring Boot Testing
- [ ] @SpringBootTest
- [ ] @WebMvcTest
- [ ] @DataJpaTest
- [ ] @MockBean
- [ ] @SpyBean

## Integration Testing
- [ ] Testcontainers
- [ ] Database Testing
- [ ] Kafka Testing
- [ ] REST API Testing
- [ ] Contract Testing

## Advanced
- [ ] TDD
- [ ] BDD
- [ ] Mutation Testing
- [ ] Chaos Testing
- [ ] Load Testing

## Production
- [ ] Canary Testing
- [ ] Feature Flags
- [ ] Smoke Tests
- [ ] Synthetic Monitoring
- [ ] Flaky Test Prevention

## Interview Readiness
- [ ] Can explain the complete testing pyramid and where each test type fits.
- [ ] Can write production-quality unit and integration tests using JUnit 5 and Mockito.
- [ ] Can test Spring Boot applications with Testcontainers and real infrastructure.
- [ ] Can design testing strategies for microservices and distributed systems.
- [ ] Can confidently discuss testing practices used in production engineering teams.

---

**Total Questions:** **190**

**Recommended Study Time:** **6–7 Days**

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** JUnit 5, Mockito, @SpringBootTest, @MockBean, @SpyBean, Testcontainers, Integration Testing, Contract Testing, TDD, Testing Pyramid, Mock vs Spy, Unit vs Integration Testing, Kafka Testing, Flaky Tests, CI/CD Testing