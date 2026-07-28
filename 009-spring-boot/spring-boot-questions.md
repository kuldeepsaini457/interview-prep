# Spring Boot Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Spring Boot Version:** Spring Boot 3.x (with Spring Framework 6.x)
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Spring Boot is one of the most heavily tested topics in Java backend interviews. Interviewers expect engineers to understand not only annotations but also auto-configuration, starters, embedded servers, Actuator, configuration management, startup lifecycle, and how Spring Boot works internally.

---

# Table of Contents

1. Spring Boot Fundamentals
2. Auto Configuration
3. Spring Boot Starters
4. Configuration Management
5. Profiles
6. Embedded Servers
7. Application Lifecycle
8. Externalized Configuration
9. Actuator
10. Logging
11. Spring Boot DevTools
12. Configuration Properties
13. Boot Internals
14. Advanced Spring Boot
15. Scenario-Based Questions
16. Production Experience
17. Why Questions
18. Trade-offs
19. Common Follow-up Questions

---

# 1. Spring Boot Fundamentals

## Basic

### Q1.
What is Spring Boot?

**Follow-ups**
- Why was Spring Boot introduced?
- What problems does it solve?

---

### Q2.
Difference between Spring Framework and Spring Boot.

---

### Q3.
Advantages of Spring Boot.

---

### Q4.
What is opinionated configuration?

---

### Q5.
How does Spring Boot reduce boilerplate code?

---

### Q6.
What is the purpose of `@SpringBootApplication`?

---

### Q7.
What annotations are included inside `@SpringBootApplication`?

---

### Q8.
Explain `@EnableAutoConfiguration`.

---

### Q9.
Explain `@ComponentScan`.

---

### Q10.
Explain `@Configuration`.

---

### Q11.
How does a Spring Boot application start?

---

### Q12.
What happens inside `SpringApplication.run()`?

---

### Q13.
Can Spring Boot work without Spring Framework?

---

### Q14.
Can Spring Framework work without Spring Boot?

---

### Q15.
What are the major modules provided by Spring Boot?

---

# 2. Auto Configuration

## Intermediate

### Q16.
What is Auto Configuration?

---

### Q17.
How does Auto Configuration work internally?

---

### Q18.
What is `spring.factories`?

---

### Q19.
What is `AutoConfiguration.imports` in Spring Boot 3?

---

### Q20.
How does Spring Boot decide which configuration to load?

---

### Q21.
What are Conditional Annotations?

---

### Q22.
`@ConditionalOnClass`

---

### Q23.
`@ConditionalOnMissingBean`

---

### Q24.
`@ConditionalOnBean`

---

### Q25.
`@ConditionalOnProperty`

---

### Q26.
`@ConditionalOnResource`

---

### Q27.
`@ConditionalOnExpression`

---

### Q28.
How does Boot avoid configuring unused libraries?

---

### Q29.
How do you disable Auto Configuration?

---

### Q30.
How do you create custom Auto Configuration?

---

# 3. Spring Boot Starters

## Basic

### Q31.
What are Spring Boot Starters?

---

### Q32.
Why were Starters introduced?

---

### Q33.
Common Spring Boot Starters.

---

### Q34.
Difference between Starter and Dependency.

---

### Q35.
How do Starters simplify dependency management?

---

### Q36.
What is the Spring Boot BOM?

---

### Q37.
How does dependency version management work?

---

### Q38.
Can multiple Starters introduce conflicting dependencies?

---

### Q39.
How do you exclude transitive dependencies?

---

### Q40.
How do you create a custom Starter?

---

# 4. Configuration Management

## Intermediate

### Q41.
How does Spring Boot load configuration?

---

### Q42.
`application.properties` vs `application.yml`.

---

### Q43.
Property precedence order.

---

### Q44.
How are environment variables mapped?

---

### Q45.
Command-line arguments.

---

### Q46.
System properties.

---

### Q47.
Default properties.

---

### Q48.
Profile-specific configuration.

---

### Q49.
Importing configuration files.

---

### Q50.
Configuration best practices.

---

# 5. Profiles

### Q51.
What are Profiles?

---

### Q52.
How do you activate a profile?

---

### Q53.
Multiple profiles.

---

### Q54.
Default profile.

---

### Q55.
Profile precedence.

---

### Q56.
Profile-specific properties.

---

### Q57.
Profile-specific beans.

---

### Q58.
How do profiles work in production?

---

### Q59.
Testing with profiles.

---

### Q60.
Common profile mistakes.

---

# 6. Embedded Servers

## Intermediate

### Q61.
What embedded servers does Spring Boot support?

---

### Q62.
Embedded Tomcat.

---

### Q63.
Embedded Jetty.

---

### Q64.
Embedded Undertow.

---

### Q65.
How does Spring Boot start Tomcat?

---

### Q66.
Can embedded servers be replaced?

---

### Q67.
How do you change the server port?

---

### Q68.
How do you configure SSL?

---

### Q69.
How do you configure HTTP/2?

---

### Q70.
WAR vs Executable JAR.

---

### Q71.
Can Boot deploy to an external server?

---

### Q72.
Embedded server lifecycle.

---

### Q73.
Server customization.

---

### Q74.
Graceful shutdown.

---

### Q75.
Production recommendations.

---

# 7. Application Lifecycle

### Q76.
Spring Boot startup lifecycle.

---

### Q77.
ApplicationContext initialization.

---

### Q78.
ApplicationRunner.

---

### Q79.
CommandLineRunner.

---

### Q80.
Difference between ApplicationRunner and CommandLineRunner.

---

### Q81.
Application Events during startup.

---

### Q82.
ApplicationReadyEvent.

---

### Q83.
ApplicationStartedEvent.

---

### Q84.
ApplicationFailedEvent.

---

### Q85.
Shutdown hooks.

---

### Q86.
SmartLifecycle.

---

### Q87.
Startup ordering.

---

### Q88.
Graceful startup.

---

### Q89.
Graceful shutdown.

---

### Q90.
Startup optimization.

---

# 8. Externalized Configuration

### Q91.
What is externalized configuration?

---

### Q92.
Configuration hierarchy.

---

### Q93.
Secrets management.

---

### Q94.
Environment variables.

---

### Q95.
Docker configuration.

---

### Q96.
Kubernetes ConfigMaps.

---

### Q97.
Kubernetes Secrets.

---

### Q98.
Spring Cloud Config overview.

---

### Q99.
Configuration refresh.

---

### Q100.
Production configuration management.

---

# 9. Actuator

## Advanced

### Q101.
What is Spring Boot Actuator?

---

### Q102.
Why is Actuator important?

---

### Q103.
Common Actuator endpoints.

---

### Q104.
`/health`

---

### Q105.
`/metrics`

---

### Q106.
`/info`

---

### Q107.
`/env`

---

### Q108.
`/beans`

---

### Q109.
`/mappings`

---

### Q110.
`/configprops`

---

### Q111.
Custom health indicators.

---

### Q112.
Liveness vs Readiness probes.

---

### Q113.
Actuator security.

---

### Q114.
Micrometer integration.

---

### Q115.
Prometheus integration.

---

### Q116.
Grafana integration.

---

### Q117.
Custom metrics.

---

### Q118.
Production monitoring.

---

### Q119.
Sensitive endpoints.

---

### Q120.
Actuator best practices.

---

# 10. Logging

### Q121.
Default logging framework.

---

### Q122.
SLF4J.

---

### Q123.
Logback.

---

### Q124.
Changing logging levels.

---

### Q125.
Package-specific logging.

---

### Q126.
Log patterns.

---

### Q127.
Rolling log files.

---

### Q128.
JSON logging.

---

### Q129.
Correlation IDs.

---

### Q130.
Production logging practices.

---

# 11. Spring Boot DevTools

### Q131.
What is DevTools?

---

### Q132.
Automatic restart.

---

### Q133.
LiveReload.

---

### Q134.
Restart ClassLoader.

---

### Q135.
Should DevTools be used in production?

---

### Q136.
Performance impact.

---

### Q137.
Common issues.

---

### Q138.
Remote DevTools.

---

### Q139.
DevTools exclusions.

---

### Q140.
Alternatives.

---

# 12. Configuration Properties

### Q141.
`@ConfigurationProperties`

---

### Q142.
`@EnableConfigurationProperties`

---

### Q143.
`@ConfigurationPropertiesScan`

---

### Q144.
Immutable Configuration Properties.

---

### Q145.
Constructor Binding.

---

### Q146.
Nested properties.

---

### Q147.
Collection binding.

---

### Q148.
Validation.

---

### Q149.
Metadata generation.

---

### Q150.
`@ConfigurationProperties` vs `@Value`.

---

# 13. Boot Internals

## Advanced

### Q151.
How does Boot discover Auto Configurations?

---

### Q152.
What is AutoConfigurationImportSelector?

---

### Q153.
Condition Evaluation Report.

---

### Q154.
Failure Analysis.

---

### Q155.
SpringFactoriesLoader.

---

### Q156.
AutoConfigurationPackages.

---

### Q157.
How does Boot create the executable JAR?

---

### Q158.
Spring Boot Loader.

---

### Q159.
Nested JARs.

---

### Q160.
How does Boot start from a fat JAR?

---

### Q161.
Classpath scanning.

---

### Q162.
Boot startup phases.

---

### Q163.
Bean initialization order.

---

### Q164.
Lazy Initialization.

---

### Q165.
Startup metrics.

---

# 14. Advanced Spring Boot

### Q166.
Custom Starter creation.

---

### Q167.
Custom Auto Configuration.

---

### Q168.
ApplicationContextInitializer.

---

### Q169.
EnvironmentPostProcessor.

---

### Q170.
Banner customization.

---

### Q171.
FailureAnalyzer.

---

### Q172.
ApplicationListener.

---

### Q173.
Custom Actuator Endpoint.

---

### Q174.
Custom Health Indicator.

---

### Q175.
Custom Metrics.

---

### Q176.
Native Image support.

---

### Q177.
AOT Processing.

---

### Q178.
Spring Boot 3 improvements.

---

### Q179.
Observability support.

---

### Q180.
Startup optimization techniques.

---

# 15. Scenario-Based Questions

### Q181.
Your application takes 45 seconds to start. How would you investigate and optimize startup?

---

### Q182.
A Spring Boot service fails because Auto Configuration creates an unexpected bean. How would you debug it?

---

### Q183.
Your production service exposes all Actuator endpoints publicly. What are the risks?

---

### Q184.
You need different database configurations for local, QA, staging, and production. How would you design the configuration?

---

### Q185.
A containerized Spring Boot application ignores environment variables. What would you investigate?

---

### Q186.
Your service needs to expose custom health information for an external dependency. How would you implement it?

---

### Q187.
A configuration value changes frequently without restarting the application. What approaches would you consider?

---

### Q188.
Your application throws `PortAlreadyInUseException`. How would you diagnose the issue?

---

### Q189.
A startup failure occurs due to missing configuration properties. How would you make the failure easier to diagnose?

---

### Q190.
Your application needs detailed production metrics for latency and memory. How would you configure Spring Boot?

---

# 16. Production Experience Questions

### Q191.
Which Spring Boot features do you use most frequently?

---

### Q192.
Have you customized Auto Configuration?

---

### Q193.
How do you manage configuration across multiple environments?

---

### Q194.
How do you secure Actuator endpoints?

---

### Q195.
Have you integrated Micrometer with Prometheus and Grafana?

---

### Q196.
How do you optimize Spring Boot startup time?

---

### Q197.
Have you customized embedded Tomcat or Undertow?

---

### Q198.
How do you package and deploy Spring Boot applications?

---

### Q199.
How do you monitor Spring Boot applications in production?

---

### Q200.
What Spring Boot production issue taught you the most?

---

# 17. "Why" Questions

### Q201.
Why was Spring Boot introduced?

---

### Q202.
Why is Auto Configuration useful?

---

### Q203.
Why are Starters preferred over manually adding dependencies?

---

### Q204.
Why does Spring Boot use embedded servers?

---

### Q205.
Why is externalized configuration important?

---

### Q206.
Why should `@ConfigurationProperties` be preferred over `@Value` for large configurations?

---

### Q207.
Why is Actuator considered essential in production?

---

### Q208.
Why should configuration not be hardcoded?

---

### Q209.
Why does Spring Boot package applications as executable JARs?

---

### Q210.
Why is observability a first-class feature in Spring Boot 3?

---

# 18. Trade-off Questions

### Q211.
Spring Framework vs Spring Boot.

---

### Q212.
`application.properties` vs `application.yml`.

---

### Q213.
`@Value` vs `@ConfigurationProperties`.

---

### Q214.
Executable JAR vs WAR Deployment.

---

### Q215.
Tomcat vs Undertow.

---

### Q216.
Embedded Server vs External Application Server.

---

### Q217.
Profiles vs Environment Variables.

---

### Q218.
Auto Configuration vs Explicit Configuration.

---

### Q219.
ApplicationRunner vs CommandLineRunner.

---

### Q220.
Micrometer vs Custom Monitoring.

---

# 19. Common Interview Follow-up Questions

## If you mention Auto Configuration
- How does it work?
- Conditional annotations?
- AutoConfigurationImportSelector?
- How do you disable it?
- Custom Auto Configuration?

---

## If you mention Spring Boot Startup
- `SpringApplication.run()`?
- Startup events?
- Runner interfaces?
- Lifecycle?
- Embedded Tomcat?

---

## If you mention Actuator
- Health endpoint?
- Metrics?
- Custom HealthIndicator?
- Prometheus?
- Security?

---

## If you mention Configuration
- Property precedence?
- Profiles?
- Environment variables?
- YAML?
- Validation?

---

## If you mention Boot Internals
- Fat JAR?
- Nested JARs?
- Boot Loader?
- Condition Evaluation Report?
- Failure Analyzer?

---

# Staff Engineer Discussion Questions

### Q221.
How would you standardize Spring Boot configuration across hundreds of microservices?

---

### Q222.
How do you reduce startup time for large Spring Boot applications?

---

### Q223.
How would you design organization-wide observability using Spring Boot Actuator and Micrometer?

---

### Q224.
When should Auto Configuration be overridden with explicit configuration?

---

### Q225.
How do you manage configuration securely across multiple environments and Kubernetes clusters?

---

### Q226.
How would you package and deploy Spring Boot applications for rapid scaling?

---

### Q227.
What metrics would you monitor to evaluate Spring Boot application health?

---

### Q228.
How would you review a codebase for poor Spring Boot practices?

---

### Q229.
How do Spring Boot 3 features improve enterprise backend development?

---

### Q230.
If you were redesigning Spring Boot today, what would you improve and why?

---

# Completion Checklist

## Fundamentals
- [ ] Spring Boot Architecture
- [ ] `@SpringBootApplication`
- [ ] Auto Configuration
- [ ] Starters
- [ ] Embedded Servers

## Configuration
- [ ] Profiles
- [ ] Externalized Configuration
- [ ] YAML
- [ ] `@ConfigurationProperties`
- [ ] Property Precedence

## Lifecycle
- [ ] Startup Process
- [ ] Application Events
- [ ] ApplicationRunner
- [ ] Graceful Shutdown

## Monitoring
- [ ] Actuator
- [ ] Health Endpoints
- [ ] Metrics
- [ ] Micrometer
- [ ] Prometheus

## Boot Internals
- [ ] AutoConfigurationImportSelector
- [ ] Boot Loader
- [ ] Fat JAR
- [ ] Condition Evaluation
- [ ] Failure Analyzer

## Production
- [ ] Logging
- [ ] Startup Optimization
- [ ] Configuration Management
- [ ] Security of Actuator
- [ ] Observability

## Interview Readiness
- [ ] Can explain the complete Spring Boot startup lifecycle.
- [ ] Can describe Auto Configuration internals from memory.
- [ ] Can configure production-ready Actuator and Micrometer.
- [ ] Can compare deployment models and configuration strategies.
- [ ] Can diagnose common Spring Boot startup and production issues.

---

**Total Questions:** 230
**Recommended Time:** 4–5 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** Auto Configuration, `@SpringBootApplication`, Starters, Embedded Tomcat, Configuration Properties, Profiles, Actuator, Micrometer, Boot Startup Lifecycle, Spring Boot Internals, Executable JARs, Spring Boot 3 Features