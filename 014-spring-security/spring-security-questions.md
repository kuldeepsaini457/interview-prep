# Spring Security Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Spring Version:** Spring Security 6.x + Spring Boot 3.x
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Spring Security is one of the most frequently asked backend interview topics because security is a fundamental requirement for enterprise applications. Interviewers expect candidates to understand authentication, authorization, filter chains, JWT, OAuth2, method security, CSRF, CORS, session management, password encoding, and Spring Security internals.

---

# Table of Contents

1. Spring Security Fundamentals
2. Authentication
3. Authorization
4. Security Filter Chain
5. UserDetailsService
6. Password Encoding
7. JWT Authentication
8. OAuth2 & OpenID Connect
9. Session Management
10. CSRF Protection
11. CORS
12. Method Security
13. Exception Handling
14. Security Configuration
15. Spring Security Internals
16. Advanced Security Topics
17. Scenario-Based Questions
18. Production Experience
19. Why Questions
20. Trade-offs
21. Common Follow-up Questions

---

# 1. Spring Security Fundamentals

## Basic

### Q1.
What is Spring Security?

**Follow-ups**
- Why was Spring Security introduced?
- What problems does it solve?

---

### Q2.
What features does Spring Security provide?

---

### Q3.
Authentication vs Authorization.

---

### Q4.
How does Spring Security integrate with Spring Boot?

---

### Q5.
Default security behavior in Spring Boot.

---

### Q6.
What is the Security Filter Chain?

---

### Q7.
How does Spring Security process an incoming request?

---

### Q8.
What is SecurityContext?

---

### Q9.
What is SecurityContextHolder?

---

### Q10.
ThreadLocal usage in Spring Security.

---

# 2. Authentication

## Intermediate

### Q11.
What is Authentication?

---

### Q12.
AuthenticationManager.

---

### Q13.
AuthenticationProvider.

---

### Q14.
ProviderManager.

---

### Q15.
Authentication object.

---

### Q16.
UsernamePasswordAuthenticationToken.

---

### Q17.
Anonymous Authentication.

---

### Q18.
Remember-Me Authentication.

---

### Q19.
Custom AuthenticationProvider.

---

### Q20.
Authentication flow.

---

### Q21.
AuthenticationManager vs AuthenticationProvider.

---

### Q22.
AuthenticationException.

---

### Q23.
Multiple AuthenticationProviders.

---

### Q24.
Authentication success handling.

---

### Q25.
Authentication failure handling.

---

# 3. Authorization

## Intermediate

### Q26.
What is Authorization?

---

### Q27.
Role-based Authorization.

---

### Q28.
Authority vs Role.

---

### Q29.
ROLE_ prefix.

---

### Q30.
GrantedAuthority.

---

### Q31.
hasRole() vs hasAuthority().

---

### Q32.
AuthorizationManager.

---

### Q33.
AccessDecisionManager (legacy).

---

### Q34.
Custom authorization logic.

---

### Q35.
Authorization best practices.

---

# 4. Security Filter Chain

## Advanced

### Q36.
What is the Security Filter Chain?

---

### Q37.
DelegatingFilterProxy.

---

### Q38.
FilterChainProxy.

---

### Q39.
Common Spring Security filters.

---

### Q40.
SecurityContextHolderFilter.

---

### Q41.
UsernamePasswordAuthenticationFilter.

---

### Q42.
BasicAuthenticationFilter.

---

### Q43.
BearerTokenAuthenticationFilter.

---

### Q44.
ExceptionTranslationFilter.

---

### Q45.
AuthorizationFilter.

---

### Q46.
How are filters ordered?

---

### Q47.
Adding custom filters.

---

### Q48.
OncePerRequestFilter.

---

### Q49.
Filter ordering issues.

---

### Q50.
Debugging the filter chain.

---

# 5. UserDetailsService

### Q51.
What is UserDetailsService?

---

### Q52.
UserDetails.

---

### Q53.
InMemoryUserDetailsManager.

---

### Q54.
JdbcUserDetailsManager.

---

### Q55.
Custom UserDetailsService.

---

### Q56.
Loading users from a database.

---

### Q57.
Custom UserDetails.

---

### Q58.
UsernameNotFoundException.

---

### Q59.
Caching UserDetails.

---

### Q60.
Production recommendations.

---

# 6. Password Encoding

### Q61.
Why should passwords never be stored in plain text?

---

### Q62.
PasswordEncoder.

---

### Q63.
BCryptPasswordEncoder.

---

### Q64.
Argon2PasswordEncoder.

---

### Q65.
Pbkdf2PasswordEncoder.

---

### Q66.
SCryptPasswordEncoder.

---

### Q67.
DelegatingPasswordEncoder.

---

### Q68.
Password migration.

---

### Q69.
Salting passwords.

---

### Q70.
Password hashing vs encryption.

---

# 7. JWT Authentication

## Advanced

### Q71.
What is JWT?

---

### Q72.
JWT structure.

---

### Q73.
Header.

---

### Q74.
Payload.

---

### Q75.
Signature.

---

### Q76.
JWT authentication flow.

---

### Q77.
Access Token vs Refresh Token.

---

### Q78.
Token expiration.

---

### Q79.
JWT validation.

---

### Q80.
JWT signing algorithms.

---

### Q81.
HS256 vs RS256.

---

### Q82.
Token revocation.

---

### Q83.
JWT blacklisting.

---

### Q84.
Stateless authentication.

---

### Q85.
JWT security best practices.

---

# 8. OAuth2 & OpenID Connect

### Q86.
What is OAuth2?

---

### Q87.
OAuth2 roles.

---

### Q88.
Authorization Server.

---

### Q89.
Resource Server.

---

### Q90.
Client.

---

### Q91.
Resource Owner.

---

### Q92.
Authorization Code Flow.

---

### Q93.
Client Credentials Flow.

---

### Q94.
PKCE.

---

### Q95.
Refresh Tokens.

---

### Q96.
OpenID Connect.

---

### Q97.
ID Token.

---

### Q98.
OAuth2 Login.

---

### Q99.
Spring Security OAuth2 Resource Server.

---

### Q100.
Production use cases.

---

# 9. Session Management

### Q101.
Stateful authentication.

---

### Q102.
Stateless authentication.

---

### Q103.
Session fixation.

---

### Q104.
Concurrent sessions.

---

### Q105.
Session timeout.

---

### Q106.
Session invalidation.

---

### Q107.
Remember-Me.

---

### Q108.
SessionCreationPolicy.

---

### Q109.
STATELESS policy.

---

### Q110.
Production recommendations.

---

# 10. CSRF Protection

### Q111.
What is CSRF?

---

### Q112.
How does CSRF work?

---

### Q113.
CSRF Token.

---

### Q114.
Synchronizer Token Pattern.

---

### Q115.
CSRF in Spring Security.

---

### Q116.
When should CSRF be disabled?

---

### Q117.
CSRF with REST APIs.

---

### Q118.
CSRF vs XSS.

---

### Q119.
Testing CSRF.

---

### Q120.
Production best practices.

---

# 11. CORS

### Q121.
What is CORS?

---

### Q122.
Same-Origin Policy.

---

### Q123.
Preflight request.

---

### Q124.
Allowed Origins.

---

### Q125.
Allowed Methods.

---

### Q126.
Allowed Headers.

---

### Q127.
Credentials.

---

### Q128.
CORS configuration in Spring Security.

---

### Q129.
CORS debugging.

---

### Q130.
Production recommendations.

---

# 12. Method Security

### Q131.
@EnableMethodSecurity.

---

### Q132.
@PreAuthorize.

---

### Q133.
@PostAuthorize.

---

### Q134.
@Secured.

---

### Q135.
@RolesAllowed.

---

### Q136.
SpEL in security.

---

### Q137.
Method-level authorization.

---

### Q138.
Custom permission evaluation.

---

### Q139.
Method security internals.

---

### Q140.
Best practices.

---

# 13. Exception Handling

### Q141.
AuthenticationEntryPoint.

---

### Q142.
AccessDeniedHandler.

---

### Q143.
AuthenticationException.

---

### Q144.
AccessDeniedException.

---

### Q145.
Custom authentication responses.

---

### Q146.
Custom authorization responses.

---

### Q147.
ExceptionTranslationFilter.

---

### Q148.
Security exception flow.

---

### Q149.
REST error handling.

---

### Q150.
Production recommendations.

---

# 14. Security Configuration

### Q151.
SecurityFilterChain Bean.

---

### Q152.
HttpSecurity.

---

### Q153.
authorizeHttpRequests().

---

### Q154.
requestMatchers().

---

### Q155.
permitAll().

---

### Q156.
authenticated().

---

### Q157.
denyAll().

---

### Q158.
Custom login page.

---

### Q159.
Logout configuration.

---

### Q160.
Multiple SecurityFilterChains.

---

# 15. Spring Security Internals

## Advanced

### Q161.
How does DelegatingFilterProxy work?

---

### Q162.
FilterChainProxy internals.

---

### Q163.
SecurityContext persistence.

---

### Q164.
Authentication flow internals.

---

### Q165.
Authorization flow internals.

---

### Q166.
How does Spring Security use ThreadLocal?

---

### Q167.
How are filters registered?

---

### Q168.
How does SecurityContext propagate?

---

### Q169.
How does Spring Security integrate with Spring MVC?

---

### Q170.
How does Spring Security integrate with Spring Boot?

---

# 16. Advanced Security Topics

### Q171.
Custom Authentication Filter.

---

### Q172.
Custom Authorization Manager.

---

### Q173.
SecurityContextRepository.

---

### Q174.
SecurityContextHolderStrategy.

---

### Q175.
BearerTokenResolver.

---

### Q176.
Resource Server configuration.

---

### Q177.
JWT decoder.

---

### Q178.
JWT encoder.

---

### Q179.
Key rotation.

---

### Q180.
Security observability.

---

# 17. Scenario-Based Questions

### Q181.
A JWT remains valid after a user logs out. How would you handle this?

---

### Q182.
Your application uses JWT authentication but needs immediate token revocation. What approaches would you consider?

---

### Q183.
A REST endpoint returns HTTP 403 instead of HTTP 401. How would you investigate?

---

### Q184.
A custom filter executes twice for the same request. What could be the cause?

---

### Q185.
Users can access endpoints despite lacking the required role. How would you debug authorization?

---

### Q186.
Your application needs both API authentication using JWT and browser login using sessions. How would you configure Spring Security?

---

### Q187.
Cross-origin requests fail after enabling Spring Security. What would you investigate?

---

### Q188.
An application needs row-level authorization where users can access only their own records. How would you design it?

---

### Q189.
You need SSO with Google, Azure AD, or Okta. Which Spring Security features would you use?

---

### Q190.
A microservice must validate JWTs issued by another service. How would you implement it securely?

---

# 18. Production Experience Questions

### Q191.
Have you implemented JWT authentication in production?

---

### Q192.
How do you manage refresh tokens securely?

---

### Q193.
How do you protect sensitive REST APIs?

---

### Q194.
Have you integrated OAuth2 login?

---

### Q195.
How do you secure microservice-to-microservice communication?

---

### Q196.
How do you rotate JWT signing keys?

---

### Q197.
How do you monitor authentication failures?

---

### Q198.
How do you review security configurations during code reviews?

---

### Q199.
Have you customized Spring Security filters?

---

### Q200.
What security incident taught you the most?

---

# 19. "Why" Questions

### Q201.
Why does Spring Security use filters instead of interceptors?

---

### Q202.
Why is BCrypt preferred over SHA-256 for password storage?

---

### Q203.
Why should JWTs have short expiration times?

---

### Q204.
Why are refresh tokens stored more securely than access tokens?

---

### Q205.
Why should REST APIs generally be stateless?

---

### Q206.
Why is CSRF protection unnecessary for stateless JWT APIs?

---

### Q207.
Why should authorization not rely solely on frontend validation?

---

### Q208.
Why does Spring Security use ThreadLocal for SecurityContext?

---

### Q209.
Why should passwords never be encrypted using reversible encryption?

---

### Q210.
Why is least-privilege authorization important?

---

# 20. Trade-off Questions

### Q211.
Authentication vs Authorization.

---

### Q212.
Session-based Authentication vs JWT Authentication.

---

### Q213.
JWT vs OAuth2.

---

### Q214.
Access Token vs Refresh Token.

---

### Q215.
BCrypt vs Argon2.

---

### Q216.
Role-based Authorization vs Permission-based Authorization.

---

### Q217.
Stateful vs Stateless Security.

---

### Q218.
Method Security vs URL Security.

---

### Q219.
OAuth2 Authorization Code Flow vs Client Credentials Flow.

---

### Q220.
HS256 vs RS256.

---

# 21. Common Interview Follow-up Questions

## If you mention Authentication
- AuthenticationManager?
- AuthenticationProvider?
- UserDetailsService?
- PasswordEncoder?
- SecurityContext?

---

## If you mention JWT
- Structure?
- Validation?
- Refresh Tokens?
- Revocation?
- Signing algorithms?

---

## If you mention OAuth2
- Authorization Code Flow?
- PKCE?
- OpenID Connect?
- Resource Server?
- Client Credentials?

---

## If you mention Security Filters
- Filter Chain?
- DelegatingFilterProxy?
- OncePerRequestFilter?
- Filter ordering?
- Custom filters?

---

## If you mention Authorization
- Roles vs Authorities?
- Method Security?
- SpEL?
- Custom permissions?
- AccessDeniedHandler?

---

## If you mention Sessions
- Session fixation?
- Concurrent sessions?
- Stateless APIs?
- Session timeout?
- Remember-Me?

---

# Staff Engineer Discussion Questions

### Q221.
How would you standardize authentication across hundreds of microservices?

---

### Q222.
How would you design an enterprise authorization model supporting both RBAC and ABAC?

---

### Q223.
How would you implement secure SSO across multiple applications?

---

### Q224.
How would you manage secret keys and JWT signing key rotation?

---

### Q225.
How would you review a large codebase for security vulnerabilities?

---

### Q226.
How would you secure service-to-service communication in a Kubernetes environment?

---

### Q227.
What metrics would you monitor to detect authentication attacks?

---

### Q228.
How would you balance security with developer productivity?

---

### Q229.
How would you migrate a legacy session-based application to JWT authentication?

---

### Q230.
If you were redesigning Spring Security today, what architectural improvements would you introduce?

---

# Completion Checklist

## Fundamentals
- [ ] Authentication
- [ ] Authorization
- [ ] SecurityContext
- [ ] Security Filter Chain
- [ ] Spring Security Architecture

## Authentication
- [ ] AuthenticationManager
- [ ] AuthenticationProvider
- [ ] UserDetailsService
- [ ] PasswordEncoder
- [ ] Custom Authentication

## Authorization
- [ ] Roles
- [ ] Authorities
- [ ] Method Security
- [ ] URL Security
- [ ] Custom Authorization

## JWT & OAuth2
- [ ] JWT Structure
- [ ] Access Tokens
- [ ] Refresh Tokens
- [ ] OAuth2 Flows
- [ ] OpenID Connect

## Web Security
- [ ] CSRF
- [ ] CORS
- [ ] Session Management
- [ ] Exception Handling
- [ ] Security Headers

## Internals
- [ ] FilterChainProxy
- [ ] DelegatingFilterProxy
- [ ] ThreadLocal SecurityContext
- [ ] Filter Ordering
- [ ] Custom Filters

## Production
- [ ] Key Rotation
- [ ] Monitoring
- [ ] Logging
- [ ] Secure Configuration
- [ ] Security Testing

## Interview Readiness
- [ ] Can explain the Spring Security filter chain from memory.
- [ ] Can implement JWT authentication with refresh tokens.
- [ ] Can compare session-based, JWT, and OAuth2 authentication.
- [ ] Can debug common Spring Security authentication and authorization issues.
- [ ] Can discuss enterprise security architecture and production best practices.

---

**Total Questions:** 230
**Recommended Time:** 5–6 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** Authentication, Authorization, Security Filter Chain, JWT, OAuth2, UserDetailsService, Password Encoding, Method Security, CSRF, CORS, Spring Security Internals, Stateless Authentication