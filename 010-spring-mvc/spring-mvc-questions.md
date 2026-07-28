# Spring MVC Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Spring Version:** Spring Framework 6.x / Spring Boot 3.x
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Spring MVC is one of the most frequently asked topics in Java backend interviews. Interviewers expect engineers to understand not only REST annotations but also the complete request lifecycle, DispatcherServlet, HandlerMappings, HandlerAdapters, argument resolution, content negotiation, validation, exception handling, and Spring MVC internals.

---

# Table of Contents

1. Spring MVC Fundamentals
2. Request Lifecycle
3. DispatcherServlet
4. Controllers
5. Request Mapping
6. Request Parameters & Path Variables
7. Request & Response Body
8. Validation
9. Data Binding
10. Message Converters
11. Exception Handling
12. Interceptors
13. Filters vs Interceptors
14. Content Negotiation
15. File Upload & Download
16. Async Request Processing
17. CORS
18. REST Best Practices
19. Spring MVC Internals
20. Advanced Questions
21. Scenario-Based Questions
22. Production Experience
23. Why Questions
24. Trade-offs
25. Common Follow-up Questions

---

# 1. Spring MVC Fundamentals

## Basic

### Q1.
What is Spring MVC?

**Follow-ups**
- Why was Spring MVC introduced?
- What problems does it solve?

---

### Q2.
Explain the MVC architecture.

---

### Q3.
What are the responsibilities of Model, View, and Controller?

---

### Q4.
Difference between Spring MVC and Spring WebFlux.

---

### Q5.
Can Spring MVC be used without Spring Boot?

---

### Q6.
What is the Front Controller pattern?

---

### Q7.
How does Spring MVC implement the Front Controller pattern?

---

### Q8.
What is the role of DispatcherServlet?

---

### Q9.
Is Spring MVC synchronous or asynchronous by default?

---

### Q10.
When should Spring MVC be preferred over WebFlux?

---

# 2. Request Lifecycle

## Basic

### Q11.
Explain the complete request lifecycle in Spring MVC.

---

### Q12.
What happens after an HTTP request reaches the server?

---

### Q13.
How does DispatcherServlet process a request?

---

### Q14.
What is the sequence of HandlerMapping, HandlerAdapter, Controller, ViewResolver, and Response?

---

### Q15.
Where are interceptors executed?

---

### Q16.
Where is validation performed?

---

### Q17.
Where does exception handling fit into the request lifecycle?

---

### Q18.
How are HTTP responses generated?

---

### Q19.
How is JSON returned from a controller?

---

### Q20.
How is an HTTP response sent back to the client?

---

# 3. DispatcherServlet

## Intermediate

### Q21.
What is DispatcherServlet?

---

### Q22.
Why is it called the Front Controller?

---

### Q23.
How is DispatcherServlet initialized?

---

### Q24.
Can there be multiple DispatcherServlets?

---

### Q25.
How does DispatcherServlet locate controllers?

---

### Q26.
How does DispatcherServlet choose a HandlerMapping?

---

### Q27.
How does DispatcherServlet choose a HandlerAdapter?

---

### Q28.
How are exceptions handled inside DispatcherServlet?

---

### Q29.
How are ViewResolvers invoked?

---

### Q30.
What happens if no handler is found?

---

# 4. Controllers

## Basic

### Q31.
What is a Controller?

---

### Q32.
Difference between `@Controller` and `@RestController`.

---

### Q33.
How does `@RestController` work internally?

---

### Q34.
Can a controller be a singleton?

---

### Q35.
Are controllers thread-safe?

---

### Q36.
Can controllers maintain mutable state?

---

### Q37.
How are controller beans created?

---

### Q38.
Can multiple request mappings exist in one controller?

---

### Q39.
How are controllers discovered?

---

### Q40.
Best practices for controller design.

---

# 5. Request Mapping

## Intermediate

### Q41.
What is `@RequestMapping`?

---

### Q42.
Difference between `@RequestMapping` and `@GetMapping`.

---

### Q43.
`@PostMapping`

---

### Q44.
`@PutMapping`

---

### Q45.
`@DeleteMapping`

---

### Q46.
`@PatchMapping`

---

### Q47.
How does Spring choose the correct endpoint?

---

### Q48.
How are ambiguous mappings detected?

---

### Q49.
Path matching strategies.

---

### Q50.
Regex path variables.

---

### Q51.
Consumes attribute.

---

### Q52.
Produces attribute.

---

### Q53.
HTTP method constraints.

---

### Q54.
Header-based request mapping.

---

### Q55.
Parameter-based request mapping.

---

# 6. Request Parameters & Path Variables

### Q56.
`@RequestParam`

---

### Q57.
Required vs Optional parameters.

---

### Q58.
Default values.

---

### Q59.
`@PathVariable`

---

### Q60.
Difference between Path Variables and Query Parameters.

---

### Q61.
`@RequestHeader`

---

### Q62.
`@CookieValue`

---

### Q63.
`@MatrixVariable`

---

### Q64.
Binding collections.

---

### Q65.
Binding enums.

---

### Q66.
Binding dates.

---

### Q67.
Binding custom objects.

---

### Q68.
Type conversion.

---

### Q69.
Custom converters.

---

### Q70.
Formatter interface.

---

# 7. Request & Response Body

### Q71.
`@RequestBody`

---

### Q72.
`@ResponseBody`

---

### Q73.
How is JSON converted into Java objects?

---

### Q74.
How is Java converted into JSON?

---

### Q75.
Jackson integration.

---

### Q76.
Can XML also be supported?

---

### Q77.
Custom serialization.

---

### Q78.
Ignoring fields during serialization.

---

### Q79.
Handling unknown JSON properties.

---

### Q80.
ResponseEntity.

---

### Q81.
Difference between ResponseEntity and `@ResponseBody`.

---

### Q82.
Returning custom HTTP headers.

---

### Q83.
Returning custom status codes.

---

### Q84.
Streaming responses.

---

### Q85.
Large response handling.

---

# 8. Validation

## Intermediate

### Q86.
Bean Validation.

---

### Q87.
`@Valid`

---

### Q88.
`@Validated`

---

### Q89.
Difference between `@Valid` and `@Validated`.

---

### Q90.
Validation annotations.

---

### Q91.
Nested validation.

---

### Q92.
Validation groups.

---

### Q93.
BindingResult.

---

### Q94.
Method parameter validation.

---

### Q95.
Custom validators.

---

### Q96.
ConstraintValidator.

---

### Q97.
Validation messages.

---

### Q98.
Global validation handling.

---

### Q99.
Validation best practices.

---

### Q100.
Production validation strategies.

---

# 9. Data Binding

### Q101.
What is Data Binding?

---

### Q102.
WebDataBinder.

---

### Q103.
`@InitBinder`

---

### Q104.
Property Editors.

---

### Q105.
Converters.

---

### Q106.
Formatters.

---

### Q107.
Custom binding.

---

### Q108.
Binding nested objects.

---

### Q109.
Binding collections.

---

### Q110.
Binding security concerns.

---

# 10. Message Converters

## Advanced

### Q111.
What is HttpMessageConverter?

---

### Q112.
Common MessageConverters.

---

### Q113.
JacksonMessageConverter.

---

### Q114.
StringHttpMessageConverter.

---

### Q115.
ByteArrayHttpMessageConverter.

---

### Q116.
ResourceHttpMessageConverter.

---

### Q117.
Converter selection.

---

### Q118.
Custom MessageConverter.

---

### Q119.
MessageConverter ordering.

---

### Q120.
Performance considerations.

---

# 11. Exception Handling

### Q121.
How does Spring MVC handle exceptions?

---

### Q122.
`@ExceptionHandler`

---

### Q123.
`@ControllerAdvice`

---

### Q124.
`@RestControllerAdvice`

---

### Q125.
ResponseStatusException.

---

### Q126.
`@ResponseStatus`

---

### Q127.
ProblemDetail (Spring Boot 3).

---

### Q128.
ExceptionResolver.

---

### Q129.
Default exception handling.

---

### Q130.
REST error response design.

---

# 12. Interceptors

### Q131.
What is HandlerInterceptor?

---

### Q132.
preHandle().

---

### Q133.
postHandle().

---

### Q134.
afterCompletion().

---

### Q135.
Interceptor execution order.

---

### Q136.
Registering interceptors.

---

### Q137.
Interceptor use cases.

---

### Q138.
Authentication via interceptors.

---

### Q139.
Logging via interceptors.

---

### Q140.
Performance implications.

---

# 13. Filters vs Interceptors

### Q141.
Servlet Filter.

---

### Q142.
Spring Interceptor.

---

### Q143.
Filter vs Interceptor.

---

### Q144.
Filter vs AOP.

---

### Q145.
Execution order.

---

### Q146.
Authentication use cases.

---

### Q147.
Logging use cases.

---

### Q148.
Compression filters.

---

### Q149.
CORS filters.

---

### Q150.
Production recommendations.

---

# 14. Content Negotiation

### Q151.
What is Content Negotiation?

---

### Q152.
Accept header.

---

### Q153.
Content-Type header.

---

### Q154.
Produces.

---

### Q155.
Consumes.

---

### Q156.
Default content type.

---

### Q157.
JSON vs XML.

---

### Q158.
Versioned APIs.

---

### Q159.
Media types.

---

### Q160.
Custom content negotiation.

---

# 15. File Upload & Download

### Q161.
Multipart requests.

---

### Q162.
MultipartFile.

---

### Q163.
File upload validation.

---

### Q164.
Large file uploads.

---

### Q165.
Streaming downloads.

---

### Q166.
Returning files.

---

### Q167.
Content-Disposition header.

---

### Q168.
Range requests.

---

### Q169.
Security considerations.

---

### Q170.
Production best practices.

---

# 16. Async Request Processing

### Q171.
Callable.

---

### Q172.
DeferredResult.

---

### Q173.
WebAsyncTask.

---

### Q174.
SseEmitter.

---

### Q175.
ResponseBodyEmitter.

---

### Q176.
StreamingResponseBody.

---

### Q177.
Async lifecycle.

---

### Q178.
Thread management.

---

### Q179.
Timeout handling.

---

### Q180.
When should async MVC be used?

---

# 17. CORS

### Q181.
What is CORS?

---

### Q182.
Same-Origin Policy.

---

### Q183.
Preflight requests.

---

### Q184.
`@CrossOrigin`.

---

### Q185.
Global CORS configuration.

---

### Q186.
Allowed origins.

---

### Q187.
Credentials.

---

### Q188.
Security implications.

---

### Q189.
CORS debugging.

---

### Q190.
Production recommendations.

---

# 18. REST Best Practices

### Q191.
REST principles.

---

### Q192.
Resource naming.

---

### Q193.
HTTP status codes.

---

### Q194.
Idempotency.

---

### Q195.
Pagination.

---

### Q196.
Sorting & filtering.

---

### Q197.
Versioning.

---

### Q198.
HATEOAS overview.

---

### Q199.
Error response standards.

---

### Q200.
REST API documentation.

---

# 19. Spring MVC Internals

### Q201.
HandlerMapping internals.

---

### Q202.
HandlerAdapter internals.

---

### Q203.
RequestMappingHandlerMapping.

---

### Q204.
RequestMappingHandlerAdapter.

---

### Q205.
ArgumentResolver.

---

### Q206.
ReturnValueHandler.

---

### Q207.
ViewResolver.

---

### Q208.
LocaleResolver.

---

### Q209.
FlashMap.

---

### Q210.
MultipartResolver.

---

# 20. Advanced Questions

### Q211.
How does Spring MVC resolve method arguments?

---

### Q212.
How are custom argument resolvers implemented?

---

### Q213.
How are return values processed?

---

### Q214.
How does Spring MVC integrate with Servlet API?

---

### Q215.
How are converters selected?

---

### Q216.
PathPatternParser vs AntPathMatcher.

---

### Q217.
How does MVC integrate with Spring Security?

---

### Q218.
How does MVC differ from WebFlux internally?

---

### Q219.
Thread-per-request architecture.

---

### Q220.
Performance tuning for Spring MVC.

---

# 21. Scenario-Based Questions

### Q221.
A controller returns HTTP 415 Unsupported Media Type. What could be the cause?

---

### Q222.
Your REST API returns HTTP 400 before reaching the controller. How would you investigate?

---

### Q223.
Two endpoints conflict due to ambiguous mappings. How would you resolve them?

---

### Q224.
A file upload endpoint consumes excessive memory. How would you optimize it?

---

### Q225.
You need request logging without modifying controllers. Which Spring MVC feature would you use?

---

### Q226.
Validation errors return inconsistent responses across services. How would you standardize them?

---

### Q227.
A controller becomes slow because of long-running operations. Would async request processing help? Why?

---

### Q228.
Your application needs to support both JSON and XML clients. How would you configure Spring MVC?

---

### Q229.
Cross-origin requests fail only in production. What would you investigate?

---

### Q230.
A controller stores request-specific data in instance variables. What problems could this cause?

---

# 22. Production Experience Questions

### Q231.
How have you structured controllers in large microservices?

---

### Q232.
Have you implemented global exception handling?

---

### Q233.
How do you validate incoming requests?

---

### Q234.
Have you customized Jackson serialization?

---

### Q235.
How do you handle file uploads in production?

---

### Q236.
How do you secure REST endpoints?

---

### Q237.
Have you implemented custom argument resolvers?

---

### Q238.
How do you optimize Spring MVC performance?

---

### Q239.
How do you monitor request latency and failures?

---

### Q240.
What Spring MVC production issue taught you the most?

---

# 23. "Why" Questions

### Q241.
Why does Spring MVC use DispatcherServlet?

---

### Q242.
Why are controllers singleton beans?

---

### Q243.
Why shouldn't controllers maintain mutable state?

---

### Q244.
Why does Spring use HttpMessageConverters?

---

### Q245.
Why is validation separated from business logic?

---

### Q246.
Why is `ResponseEntity` preferred for REST APIs?

---

### Q247.
Why are Interceptors preferred over controller logging?

---

### Q248.
Why should REST APIs return standardized error responses?

---

### Q249.
Why is content negotiation useful?

---

### Q250.
Why does Spring MVC rely on the Servlet API?

---

# 24. Trade-off Questions

### Q251.
`@Controller` vs `@RestController`.

---

### Q252.
Filter vs Interceptor.

---

### Q253.
Interceptor vs AOP.

---

### Q254.
`@RequestParam` vs `@PathVariable`.

---

### Q255.
`@Valid` vs `@Validated`.

---

### Q256.
ResponseEntity vs `@ResponseBody`.

---

### Q257.
JSON vs XML.

---

### Q258.
Spring MVC vs WebFlux.

---

### Q259.
Sync Requests vs Async Requests.

---

### Q260.
Servlet Stack vs Reactive Stack.

---

# 25. Common Interview Follow-up Questions

## If you mention DispatcherServlet
- Request lifecycle?
- HandlerMapping?
- HandlerAdapter?
- ViewResolver?
- ExceptionResolver?

---

## If you mention Controllers
- Thread safety?
- Singleton scope?
- Mutable state?
- Validation?
- REST annotations?

---

## If you mention Validation
- BindingResult?
- Validation groups?
- Custom validators?
- ConstraintValidator?
- Global handling?

---

## If you mention MessageConverters
- Jackson?
- XML?
- Converter selection?
- Custom converters?
- Performance?

---

## If you mention Async MVC
- Callable?
- DeferredResult?
- StreamingResponseBody?
- Timeouts?
- Thread model?

---

## If you mention REST APIs
- HTTP status codes?
- Versioning?
- Pagination?
- Idempotency?
- Error responses?

---

# Staff Engineer Discussion Questions

### Q261.
How would you design REST controllers for hundreds of microservices while maintaining consistency?

---

### Q262.
How would you standardize API error responses across an organization?

---

### Q263.
How do you decide between Spring MVC and Spring WebFlux for a new service?

---

### Q264.
How would you improve request observability without affecting controller code?

---

### Q265.
How do you minimize controller complexity while keeping services maintainable?

---

### Q266.
How would you optimize Spring MVC for high-throughput APIs?

---

### Q267.
How do you design backward-compatible REST APIs?

---

### Q268.
What metrics would you monitor for Spring MVC applications in production?

---

### Q269.
How would you review a codebase for poor Spring MVC practices?

---

### Q270.
If you were redesigning Spring MVC today, what architectural improvements would you introduce?

---

# Completion Checklist

## Fundamentals
- [ ] MVC Architecture
- [ ] DispatcherServlet
- [ ] Request Lifecycle
- [ ] Controllers
- [ ] Request Mapping

## Request Processing
- [ ] Request Parameters
- [ ] Path Variables
- [ ] RequestBody
- [ ] ResponseEntity
- [ ] Data Binding

## Validation
- [ ] Bean Validation
- [ ] @Valid
- [ ] BindingResult
- [ ] Custom Validators
- [ ] Global Exception Handling

## MVC Components
- [ ] HandlerMapping
- [ ] HandlerAdapter
- [ ] MessageConverters
- [ ] Interceptors
- [ ] ViewResolvers

## REST
- [ ] Content Negotiation
- [ ] HTTP Status Codes
- [ ] Versioning
- [ ] Pagination
- [ ] Error Responses

## Advanced
- [ ] Async MVC
- [ ] File Upload/Download
- [ ] CORS
- [ ] Custom Argument Resolvers
- [ ] Spring MVC Internals

## Production
- [ ] Performance Tuning
- [ ] Logging
- [ ] Monitoring
- [ ] Security
- [ ] API Standardization

## Interview Readiness
- [ ] Can explain the complete Spring MVC request lifecycle from memory.
- [ ] Can describe DispatcherServlet internals and request processing.
- [ ] Can compare Filters, Interceptors, and AOP with real use cases.
- [ ] Can design production-ready REST APIs using Spring MVC.
- [ ] Can diagnose common Spring MVC production issues confidently.

---

**Total Questions:** 270
**Recommended Time:** 5–6 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** DispatcherServlet, Request Lifecycle, Controllers, Request Mapping, Validation, HttpMessageConverters, Global Exception Handling, Interceptors, REST API Design, Async MVC, Content Negotiation, Spring MVC Internals