# REST API Design Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> REST API Design is one of the most important backend interview topics because APIs are the contract between services and clients. Interviewers expect engineers to understand REST principles, HTTP semantics, resource modeling, API versioning, pagination, idempotency, security, caching, documentation, error handling, and production-scale API design.

---

# Table of Contents

1. REST Fundamentals
2. HTTP Methods
3. Resource Design
4. URI Design
5. HTTP Status Codes
6. Request & Response Design
7. API Versioning
8. Pagination, Filtering & Sorting
9. Idempotency
10. Caching
11. Error Handling
12. Security
13. API Documentation
14. Performance Optimization
15. REST Constraints
16. Advanced REST Concepts
17. Scenario-Based Questions
18. Production Experience
19. Why Questions
20. Trade-offs
21. Common Follow-up Questions

---

# 1. REST Fundamentals

## Basic

### Q1.
What is REST?

**Follow-ups**
- Who introduced REST?
- Why was REST created?

---

### Q2.
What are REST principles?

---

### Q3.
REST vs RESTful API.

---

### Q4.
REST vs SOAP.

---

### Q5.
REST vs RPC.

---

### Q6.
What makes an API RESTful?

---

### Q7.
Can REST work over protocols other than HTTP?

---

### Q8.
What is a Resource in REST?

---

### Q9.
What is Representation?

---

### Q10.
REST maturity model.

---

# 2. HTTP Methods

## Basic

### Q11.
GET.

---

### Q12.
POST.

---

### Q13.
PUT.

---

### Q14.
PATCH.

---

### Q15.
DELETE.

---

### Q16.
HEAD.

---

### Q17.
OPTIONS.

---

### Q18.
TRACE.

---

### Q19.
CONNECT.

---

### Q20.
Difference between PUT and PATCH.

---

### Q21.
POST vs PUT.

---

### Q22.
DELETE idempotency.

---

### Q23.
Safe methods.

---

### Q24.
Idempotent methods.

---

### Q25.
When should POST not be used?

---

# 3. Resource Design

## Intermediate

### Q26.
How do you identify resources?

---

### Q27.
Nouns vs Verbs in URLs.

---

### Q28.
Plural vs Singular resources.

---

### Q29.
Nested resources.

---

### Q30.
Deep nesting.

---

### Q31.
Resource relationships.

---

### Q32.
Sub-resources.

---

### Q33.
Composite resources.

---

### Q34.
Resource naming best practices.

---

### Q35.
Resource lifecycle.

---

# 4. URI Design

### Q36.
URI vs URL vs URN.

---

### Q37.
REST URI best practices.

---

### Q38.
Lowercase URLs.

---

### Q39.
Hyphens vs underscores.

---

### Q40.
Query parameters.

---

### Q41.
Path variables.

---

### Q42.
Trailing slashes.

---

### Q43.
Action endpoints.

---

### Q44.
Search endpoints.

---

### Q45.
Bulk endpoints.

---

# 5. HTTP Status Codes

## Intermediate

### Q46.
2xx Success codes.

---

### Q47.
200 OK.

---

### Q48.
201 Created.

---

### Q49.
202 Accepted.

---

### Q50.
204 No Content.

---

### Q51.
3xx Redirection codes.

---

### Q52.
301 vs 302.

---

### Q53.
304 Not Modified.

---

### Q54.
4xx Client errors.

---

### Q55.
400 Bad Request.

---

### Q56.
401 Unauthorized.

---

### Q57.
403 Forbidden.

---

### Q58.
404 Not Found.

---

### Q59.
405 Method Not Allowed.

---

### Q60.
409 Conflict.

---

### Q61.
410 Gone.

---

### Q62.
412 Precondition Failed.

---

### Q63.
415 Unsupported Media Type.

---

### Q64.
422 Unprocessable Entity.

---

### Q65.
429 Too Many Requests.

---

### Q66.
5xx Server errors.

---

### Q67.
500 Internal Server Error.

---

### Q68.
502 Bad Gateway.

---

### Q69.
503 Service Unavailable.

---

### Q70.
504 Gateway Timeout.

---

# 6. Request & Response Design

### Q71.
JSON request design.

---

### Q72.
JSON response design.

---

### Q73.
Response metadata.

---

### Q74.
Standard response envelope.

---

### Q75.
Should responses always have a wrapper object?

---

### Q76.
Returning collections.

---

### Q77.
Returning partial resources.

---

### Q78.
Field filtering.

---

### Q79.
Null vs Missing fields.

---

### Q80.
Date & time formatting.

---

### Q81.
Enum representation.

---

### Q82.
Binary data responses.

---

### Q83.
Large payload handling.

---

### Q84.
Response compression.

---

### Q85.
API consistency guidelines.

---

# 7. API Versioning

## Advanced

### Q86.
Why is API versioning needed?

---

### Q87.
URI versioning.

---

### Q88.
Header versioning.

---

### Q89.
Query parameter versioning.

---

### Q90.
Media type versioning.

---

### Q91.
Backward compatibility.

---

### Q92.
Breaking changes.

---

### Q93.
Deprecation strategy.

---

### Q94.
Sunset headers.

---

### Q95.
Versioning best practices.

---

# 8. Pagination, Filtering & Sorting

### Q96.
Offset pagination.

---

### Q97.
Cursor pagination.

---

### Q98.
Keyset pagination.

---

### Q99.
Page vs Cursor.

---

### Q100.
Sorting.

---

### Q101.
Multi-column sorting.

---

### Q102.
Filtering.

---

### Q103.
Search APIs.

---

### Q104.
Range queries.

---

### Q105.
Pagination metadata.

---

# 9. Idempotency

### Q106.
What is idempotency?

---

### Q107.
Which HTTP methods are idempotent?

---

### Q108.
POST idempotency.

---

### Q109.
Idempotency keys.

---

### Q110.
Duplicate request handling.

---

### Q111.
Payment APIs.

---

### Q112.
Retry mechanisms.

---

### Q113.
Exactly-once semantics.

---

### Q114.
At-least-once delivery.

---

### Q115.
Production best practices.

---

# 10. Caching

### Q116.
HTTP caching.

---

### Q117.
Cache-Control.

---

### Q118.
ETag.

---

### Q119.
If-None-Match.

---

### Q120.
Last-Modified.

---

### Q121.
304 Not Modified.

---

### Q122.
Browser caching.

---

### Q123.
CDN caching.

---

### Q124.
Cache invalidation.

---

### Q125.
Caching strategies.

---

# 11. Error Handling

### Q126.
REST error response design.

---

### Q127.
Standard error format.

---

### Q128.
RFC 7807 (Problem Details).

---

### Q129.
Validation errors.

---

### Q130.
Business errors.

---

### Q131.
Error codes.

---

### Q132.
Correlation IDs.

---

### Q133.
Trace IDs.

---

### Q134.
Localization of errors.

---

### Q135.
Production recommendations.

---

# 12. Security

### Q136.
HTTPS.

---

### Q137.
Authentication.

---

### Q138.
Authorization.

---

### Q139.
JWT.

---

### Q140.
OAuth2.

---

### Q141.
Rate limiting.

---

### Q142.
API Keys.

---

### Q143.
Input validation.

---

### Q144.
Output encoding.

---

### Q145.
OWASP API Security Top 10.

---

# 13. API Documentation

### Q146.
OpenAPI Specification.

---

### Q147.
Swagger.

---

### Q148.
API examples.

---

### Q149.
Contract-first development.

---

### Q150.
Code-first development.

---

### Q151.
API changelog.

---

### Q152.
SDK generation.

---

### Q153.
Developer portal.

---

### Q154.
Mock APIs.

---

### Q155.
Documentation best practices.

---

# 14. Performance Optimization

### Q156.
Payload optimization.

---

### Q157.
Compression.

---

### Q158.
Caching.

---

### Q159.
Batch APIs.

---

### Q160.
Bulk APIs.

---

### Q161.
HTTP Keep-Alive.

---

### Q162.
Connection pooling.

---

### Q163.
Streaming responses.

---

### Q164.
Async APIs.

---

### Q165.
Performance monitoring.

---

# 15. REST Constraints

### Q166.
Client-Server.

---

### Q167.
Statelessness.

---

### Q168.
Cacheability.

---

### Q169.
Uniform Interface.

---

### Q170.
Layered System.

---

### Q171.
Code-on-Demand.

---

### Q172.
Hypermedia (HATEOAS).

---

### Q173.
Self-descriptive messages.

---

### Q174.
REST maturity levels.

---

### Q175.
Real-world deviations from REST.

---

# 16. Advanced REST Concepts

### Q176.
Conditional Requests.

---

### Q177.
Optimistic concurrency with ETags.

---

### Q178.
Content Negotiation.

---

### Q179.
Media Types.

---

### Q180.
HAL.

---

### Q181.
JSON:API.

---

### Q182.
GraphQL vs REST.

---

### Q183.
gRPC vs REST.

---

### Q184.
WebSockets vs REST.

---

### Q185.
Event-driven APIs.

---

# 17. Scenario-Based Questions

### Q186.
How would you design a REST API for an e-commerce order service?

---

### Q187.
A client repeatedly sends duplicate POST requests due to retries. How would you prevent duplicate orders?

---

### Q188.
Your API serves millions of requests per day. How would you optimize latency?

---

### Q189.
A GET endpoint returns a 2 MB payload. How would you redesign it?

---

### Q190.
You need to support multiple mobile app versions simultaneously. How would you version the API?

---

### Q191.
Your API needs to expose partial updates. Would you use PUT or PATCH? Why?

---

### Q192.
A REST endpoint frequently returns stale cached data. How would you investigate?

---

### Q193.
How would you secure public APIs from abuse?

---

### Q194.
You need backward compatibility while evolving response models. How would you approach it?

---

### Q195.
How would you design APIs for bulk operations while maintaining transactional integrity?

---

# 18. Production Experience Questions

### Q196.
How have you designed REST APIs for microservices?

---

### Q197.
How do you standardize API responses across teams?

---

### Q198.
Have you implemented API versioning?

---

### Q199.
How do you document APIs?

---

### Q200.
How do you monitor API performance?

---

### Q201.
How do you implement rate limiting?

---

### Q202.
Have you optimized API payloads?

---

### Q203.
How do you secure public-facing APIs?

---

### Q204.
How do you review API designs during code reviews?

---

### Q205.
What REST API design mistake taught you the most?

---

# 19. "Why" Questions

### Q206.
Why should REST resources be nouns instead of verbs?

---

### Q207.
Why are GET requests safe?

---

### Q208.
Why should APIs be stateless?

---

### Q209.
Why should HTTP status codes be used correctly?

---

### Q210.
Why should POST requests support idempotency in critical systems?

---

### Q211.
Why is pagination essential for large datasets?

---

### Q212.
Why is cursor pagination preferred over offset pagination at scale?

---

### Q213.
Why should APIs return consistent error responses?

---

### Q214.
Why should API versioning be minimized?

---

### Q215.
Why is backward compatibility important?

---

# 20. Trade-off Questions

### Q216.
REST vs SOAP.

---

### Q217.
REST vs GraphQL.

---

### Q218.
REST vs gRPC.

---

### Q219.
PUT vs PATCH.

---

### Q220.
Offset Pagination vs Cursor Pagination.

---

### Q221.
URI Versioning vs Header Versioning.

---

### Q222.
API Key vs JWT.

---

### Q223.
JSON vs XML.

---

### Q224.
Standard Response Wrapper vs Direct Resource Response.

---

### Q225.
Synchronous REST vs Event-driven Communication.

---

# 21. Common Interview Follow-up Questions

## If you mention REST
- REST constraints?
- REST maturity?
- HATEOAS?
- Statelessness?
- Uniform interface?

---

## If you mention HTTP
- Safe methods?
- Idempotent methods?
- Status codes?
- Conditional requests?
- Content negotiation?

---

## If you mention Pagination
- Offset?
- Cursor?
- Keyset?
- Metadata?
- Performance?

---

## If you mention Security
- JWT?
- OAuth2?
- Rate limiting?
- API Keys?
- HTTPS?

---

## If you mention Versioning
- Breaking changes?
- Deprecation?
- Sunset headers?
- Backward compatibility?
- Media type versioning?

---

## If you mention Error Handling
- RFC 7807?
- Validation errors?
- Correlation IDs?
- Trace IDs?
- Business errors?

---

# Staff Engineer Discussion Questions

### Q226.
How would you standardize REST API design across hundreds of microservices?

---

### Q227.
How would you introduce API governance in a large engineering organization?

---

### Q228.
How would you design APIs that remain backward compatible for years?

---

### Q229.
How would you balance REST purity with business requirements?

---

### Q230.
How would you design highly scalable public APIs?

---

### Q231.
How would you evolve an API without breaking existing clients?

---

### Q232.
How would you monitor API quality and consumer experience?

---

### Q233.
How would you review an organization's REST APIs for consistency?

---

### Q234.
How would you migrate a legacy RPC system to REST?

---

### Q235.
If you were redesigning REST today, what improvements would you introduce?

---

# Completion Checklist

## REST Fundamentals
- [ ] REST Principles
- [ ] REST Constraints
- [ ] Resource Modeling
- [ ] HTTP Methods
- [ ] URI Design

## HTTP
- [ ] Status Codes
- [ ] Request Design
- [ ] Response Design
- [ ] Headers
- [ ] Content Negotiation

## API Design
- [ ] Resource Naming
- [ ] Pagination
- [ ] Filtering
- [ ] Sorting
- [ ] Versioning

## Reliability
- [ ] Idempotency
- [ ] Retry Handling
- [ ] Error Responses
- [ ] Caching
- [ ] Conditional Requests

## Security
- [ ] HTTPS
- [ ] JWT
- [ ] OAuth2
- [ ] Rate Limiting
- [ ] Input Validation

## Performance
- [ ] Compression
- [ ] Streaming
- [ ] Bulk APIs
- [ ] Payload Optimization
- [ ] Monitoring

## Documentation
- [ ] OpenAPI
- [ ] Swagger
- [ ] Contract-first Design
- [ ] SDK Generation
- [ ] API Changelog

## Interview Readiness
- [ ] Can design production-ready REST APIs from scratch.
- [ ] Can justify every HTTP method and status code.
- [ ] Can compare REST with GraphQL, gRPC, and SOAP.
- [ ] Can design scalable, versioned, backward-compatible APIs.
- [ ] Can discuss caching, idempotency, and API security with real-world examples.

---

**Total Questions:** 235
**Recommended Time:** 5–6 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** REST Principles, HTTP Methods, Resource Design, Status Codes, Versioning, Pagination, Idempotency, Error Handling, Caching, Security, API Documentation, REST vs GraphQL/gRPC