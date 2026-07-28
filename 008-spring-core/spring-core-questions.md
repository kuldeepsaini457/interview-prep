# Spring Core Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Uber, Adobe, Salesforce, LinkedIn, Google, PhonePe, Razorpay, Flipkart, etc.
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
>
> Spring Core is one of the most important topics in Java backend interviews. Interviewers expect candidates to understand not only annotations but also the underlying IoC container, bean lifecycle, dependency injection, proxying, scopes, and how Spring works internally.

---

# Table of Contents

1. Spring Fundamentals
2. IoC & Dependency Injection
3. Spring Container
4. Bean Lifecycle
5. Bean Scopes
6. Bean Configuration
7. Dependency Injection
8. Autowiring
9. Bean Resolution
10. Lazy Initialization
11. Circular Dependencies
12. Component Scanning
13. Profiles
14. Environment & Properties
15. Spring Expression Language (SpEL)
16. Resource Loading
17. Events
18. AOP Fundamentals
19. Proxies
20. Advanced Spring Core
21. Scenario-Based Questions
22. Production Experience
23. Why Questions
24. Trade-offs
25. Common Follow-up Questions

---

# 1. Spring Fundamentals

## Basic

### Q1.
What is Spring Framework?

**Follow-ups**
- Why was Spring created?
- What problems did it solve?

---

### Q2.
What are the core modules of Spring Framework?

---

### Q3.
Difference between Spring Framework and Spring Boot.

---

### Q4.
What is Inversion of Control (IoC)?

---

### Q5.
What is Dependency Injection (DI)?

---

### Q6.
Why is Spring called an IoC container?

---

### Q7.
What advantages does Spring provide over plain Java?

---

### Q8.
What is a Spring Bean?

---

### Q9.
Who manages Spring Beans?

---

### Q10.
What is the BeanFactory?

---

### Q11.
What is ApplicationContext?

---

### Q12.
Difference between BeanFactory and ApplicationContext.

---

### Q13.
When would BeanFactory be preferred?

---

### Q14.
What additional features does ApplicationContext provide?

---

### Q15.
How does Spring start an application?

---

# 2. IoC & Dependency Injection

## Basic

### Q16.
Explain Dependency Injection.

---

### Q17.
Types of Dependency Injection.

---

### Q18.
Constructor Injection vs Setter Injection.

---

### Q19.
Field Injection vs Constructor Injection.

---

### Q20.
Why is Constructor Injection recommended?

---

### Q21.
Can Spring inject private fields?

---

### Q22.
How does Spring perform injection?

---

### Q23.
Can dependencies be optional?

---

### Q24.
What is @Autowired?

---

### Q25.
How does @Autowired work internally?

---

### Q26.
How are dependencies resolved?

---

### Q27.
What happens if multiple beans match?

---

### Q28.
What happens if no bean matches?

---

### Q29.
Required vs Optional dependencies.

---

### Q30.
How does Spring create dependency graphs?

---

# 3. Spring Container

## Intermediate

### Q31.
Explain the Spring IoC Container.

---

### Q32.
How are Bean Definitions created?

---

### Q33.
What is BeanDefinition?

---

### Q34.
Lifecycle of the ApplicationContext.

---

### Q35.
How does Spring instantiate beans?

---

### Q36.
When are singleton beans created?

---

### Q37.
What is bean post-processing?

---

### Q38.
What is BeanFactoryPostProcessor?

---

### Q39.
What is BeanPostProcessor?

---

### Q40.
Difference between BeanFactoryPostProcessor and BeanPostProcessor.

---

### Q41.
How does Spring resolve dependencies internally?

---

### Q42.
When are bean definitions finalized?

---

### Q43.
Can Bean Definitions be modified at runtime?

---

### Q44.
How does Spring detect configuration errors?

---

### Q45.
What happens during ApplicationContext refresh()?

---

# 4. Bean Lifecycle

## Intermediate

### Q46.
Explain the complete Spring Bean lifecycle.

---

### Q47.
Bean instantiation.

---

### Q48.
Dependency injection phase.

---

### Q49.
Aware interfaces.

---

### Q50.
@PostConstruct.

---

### Q51.
InitializingBean.

---

### Q52.
Custom init-method.

---

### Q53.
BeanPostProcessor lifecycle.

---

### Q54.
@PreDestroy.

---

### Q55.
DisposableBean.

---

### Q56.
destroy-method.

---

### Q57.
Order of lifecycle callbacks.

---

### Q58.
When are destroy methods executed?

---

### Q59.
How are prototype beans destroyed?

---

### Q60.
Can lifecycle callbacks be customized?

---

# 5. Bean Scopes

## Basic

### Q61.
What are bean scopes?

---

### Q62.
Singleton scope.

---

### Q63.
Prototype scope.

---

### Q64.
Request scope.

---

### Q65.
Session scope.

---

### Q66.
Application scope.

---

### Q67.
WebSocket scope.

---

### Q68.
Default bean scope.

---

### Q69.
Singleton bean vs Singleton design pattern.

---

### Q70.
Thread safety of singleton beans.

---

### Q71.
Can singleton beans maintain mutable state?

---

### Q72.
Injecting prototype into singleton.

---

### Q73.
Scoped Proxy.

---

### Q74.
ObjectProvider.

---

### Q75.
Lookup method injection.

---

# 6. Bean Configuration

### Q76.
Ways to define beans.

---

### Q77.
@Component.

---

### Q78.
@Configuration.

---

### Q79.
@Bean.

---

### Q80.
Difference between @Component and @Bean.

---

### Q81.
How does @Configuration differ from a normal class?

---

### Q82.
Full vs Lite Configuration.

---

### Q83.
Can @Bean methods call each other?

---

### Q84.
@Configuration proxy behavior.

---

### Q85.
How does Spring ensure singleton behavior for @Bean methods?

---

# 7. Dependency Injection

### Q86.
Constructor injection.

---

### Q87.
Setter injection.

---

### Q88.
Field injection.

---

### Q89.
Method injection.

---

### Q90.
Collection injection.

---

### Q91.
Map injection.

---

### Q92.
Injecting Optional beans.

---

### Q93.
Injecting lazy beans.

---

### Q94.
Circular dependencies during injection.

---

### Q95.
Dependency resolution order.

---

# 8. Autowiring

### Q96.
@Autowired.

---

### Q97.
@Qualifier.

---

### Q98.
@Primary.

---

### Q99.
@Resource.

---

### Q100.
@Inject.

---

### Q101.
@Autowired(required = false).

---

### Q102.
Collection autowiring.

---

### Q103.
Map autowiring.

---

### Q104.
Resolving multiple bean candidates.

---

### Q105.
Autowiring by type vs by name.

---

# 9. Bean Resolution

### Q106.
How does Spring choose which bean to inject?

---

### Q107.
What happens if two beans have the same type?

---

### Q108.
Bean naming strategy.

---

### Q109.
Bean aliases.

---

### Q110.
Resolving generic types.

---

### Q111.
Resolving inherited beans.

---

### Q112.
Conditional beans.

---

### Q113.
@Conditional.

---

### Q114.
@ConditionalOnBean.

---

### Q115.
@ConditionalOnMissingBean.

---

# 10. Lazy Initialization

### Q116.
What is lazy initialization?

---

### Q117.
@Lazy annotation.

---

### Q118.
When should lazy initialization be used?

---

### Q119.
Advantages of lazy loading.

---

### Q120.
Disadvantages of lazy loading.

---

# 11. Circular Dependencies

### Q121.
What is a circular dependency?

---

### Q122.
How does Spring detect circular dependencies?

---

### Q123.
Constructor injection circular dependency.

---

### Q124.
Setter injection circular dependency.

---

### Q125.
Why can't constructor cycles be resolved?

---

### Q126.
How does Spring resolve setter cycles?

---

### Q127.
How should circular dependencies be eliminated?

---

### Q128.
What changed in recent Spring versions regarding circular references?

---

### Q129.
Real-world examples of circular dependencies.

---

### Q130.
Production implications of circular dependencies.

---

# 12. Component Scanning

### Q131.
What is component scanning?

---

### Q132.
@ComponentScan.

---

### Q133.
How does Spring discover beans?

---

### Q134.
Default scanning behavior.

---

### Q135.
includeFilters and excludeFilters.

---

### Q136.
How does package structure affect scanning?

---

### Q137.
Performance impact of component scanning.

---

### Q138.
How does Spring Boot determine scan packages?

---

### Q139.
Common scanning mistakes.

---

### Q140.
How do large applications organize scanning?

---

# 13. Profiles

### Q141.
What are Spring Profiles?

---

### Q142.
@Profile.

---

### Q143.
How do profiles work?

---

### Q144.
Activating profiles.

---

### Q145.
Default profile.

---

### Q146.
Multiple active profiles.

---

### Q147.
Production use cases.

---

### Q148.
Profile-specific beans.

---

### Q149.
Testing with profiles.

---

### Q150.
Profile best practices.

---

# 14. Environment & Properties

### Q151.
@Value.

---

### Q152.
Environment interface.

---

### Q153.
@ConfigurationProperties.

---

### Q154.
@ConfigurationProperties vs @Value.

---

### Q155.
Property Sources.

---

### Q156.
Property precedence.

---

### Q157.
External configuration.

---

### Q158.
YAML vs Properties.

---

### Q159.
Relaxed binding.

---

### Q160.
Validation of configuration properties.

---

# 15. Spring Expression Language (SpEL)

### Q161.
What is SpEL?

---

### Q162.
Common SpEL use cases.

---

### Q163.
Property access.

---

### Q164.
Method invocation.

---

### Q165.
Collection selection.

---

### Q166.
Conditional expressions.

---

### Q167.
Bean references.

---

### Q168.
Security considerations.

---

### Q169.
Performance implications.

---

### Q170.
When should SpEL be avoided?

---

# 16. Resource Loading

### Q171.
Resource interface.

---

### Q172.
ClassPathResource.

---

### Q173.
FileSystemResource.

---

### Q174.
UrlResource.

---

### Q175.
ResourceLoader.

---

### Q176.
Loading resources from JAR files.

---

### Q177.
ResourcePatternResolver.

---

### Q178.
Wildcard resource loading.

---

### Q179.
Production use cases.

---

### Q180.
Common pitfalls.

---

# 17. Events

### Q181.
What is the Spring Event mechanism?

---

### Q182.
ApplicationEvent.

---

### Q183.
ApplicationListener.

---

### Q184.
@EventListener.

---

### Q185.
Publishing events.

---

### Q186.
Synchronous vs asynchronous events.

---

### Q187.
Transactional events.

---

### Q188.
@Async with events.

---

### Q189.
Production use cases.

---

### Q190.
Events vs direct service calls.

---

# 18. AOP Fundamentals

### Q191.
What is Aspect-Oriented Programming?

---

### Q192.
Why was AOP introduced?

---

### Q193.
Cross-cutting concerns.

---

### Q194.
Aspect.

---

### Q195.
Advice.

---

### Q196.
Pointcut.

---

### Q197.
Join Point.

---

### Q198.
Types of Advice.

---

### Q199.
Around Advice vs Before Advice.

---

### Q200.
How does Spring AOP work?

---

# 19. Proxies

### Q201.
What are proxies in Spring?

---

### Q202.
JDK Dynamic Proxy vs CGLIB.

---

### Q203.
When does Spring use JDK proxies?

---

### Q204.
When does Spring use CGLIB?

---

### Q205.
How do proxies enable transactions?

---

### Q206.
How do proxies enable security?

---

### Q207.
How do proxies enable caching?

---

### Q208.
Self-invocation problem.

---

### Q209.
How do proxies affect debugging?

---

### Q210.
Performance implications of proxies.

---

# 20. Advanced Spring Core

### Q211.
BeanFactoryPostProcessor internals.

---

### Q212.
BeanPostProcessor internals.

---

### Q213.
FactoryBean.

---

### Q214.
SmartInitializingSingleton.

---

### Q215.
ImportSelector.

---

### Q216.
DeferredImportSelector.

---

### Q217.
ImportBeanDefinitionRegistrar.

---

### Q218.
Aware interfaces.

---

### Q219.
ApplicationContextAware.

---

### Q220.
How does Spring Boot auto-configuration leverage Spring Core?

---

# 21. Scenario-Based Questions

### Q221.
Your application fails to start because of multiple bean candidates. How would you investigate?

---

### Q222.
A singleton bean contains mutable state and causes data inconsistencies. What is wrong?

---

### Q223.
Your service has a circular dependency. How would you redesign it?

---

### Q224.
Application startup takes 40 seconds. Which Spring Core mechanisms would you investigate?

---

### Q225.
You need different implementations for development and production environments. How would you configure Spring?

---

### Q226.
A prototype bean injected into a singleton always behaves like a singleton. Why?

---

### Q227.
A bean is not being discovered during component scanning. What could be the cause?

---

### Q228.
Your @Transactional method isn't working. How could Spring proxies be involved?

---

### Q229.
You need to execute initialization logic after all singleton beans are created. How would you implement it?

---

### Q230.
A Spring Boot application consumes excessive memory during startup. Which Spring Core features would you investigate?

---

# 22. Production Experience Questions

### Q231.
How do you structure Spring configuration in large microservices?

---

### Q232.
Have you ever debugged bean creation failures?

---

### Q233.
Have you used @ConfigurationProperties in production?

---

### Q234.
How do you manage environment-specific configurations?

---

### Q235.
Have you customized BeanPostProcessors?

---

### Q236.
How do you avoid circular dependencies during code reviews?

---

### Q237.
How do you organize packages for component scanning?

---

### Q238.
Have you used Spring Events in production?

---

### Q239.
How do you debug proxy-related issues?

---

### Q240.
What Spring Core concept has saved you the most development time?

---

# 23. "Why" Questions

### Q241.
Why does Spring prefer Constructor Injection?

---

### Q242.
Why is Field Injection discouraged?

---

### Q243.
Why are singleton beans the default?

---

### Q244.
Why does Spring use proxies instead of bytecode modification?

---

### Q245.
Why is ApplicationContext preferred over BeanFactory?

---

### Q246.
Why are BeanPostProcessors powerful?

---

### Q247.
Why should business logic avoid depending on Spring APIs?

---

### Q248.
Why are circular dependencies considered a design smell?

---

### Q249.
Why does Spring Boot rely heavily on auto-configuration?

---

### Q250.
Why is dependency injection superior to manually creating objects?

---

# 24. Trade-off Questions

### Q251.
Constructor Injection vs Field Injection.

---

### Q252.
Constructor Injection vs Setter Injection.

---

### Q253.
@Component vs @Bean.

---

### Q254.
BeanFactory vs ApplicationContext.

---

### Q255.
Singleton Scope vs Prototype Scope.

---

### Q256.
@Value vs @ConfigurationProperties.

---

### Q257.
Profiles vs Conditional Beans.

---

### Q258.
Events vs Direct Method Calls.

---

### Q259.
JDK Proxy vs CGLIB.

---

### Q260.
Lazy Initialization vs Eager Initialization.

---

# 25. Common Interview Follow-up Questions

## If you mention IoC
- How does Spring implement IoC?
- BeanFactory?
- ApplicationContext?
- Dependency graph?
- Bean lifecycle?

---

## If you mention Dependency Injection
- Constructor vs Setter?
- Field Injection?
- Optional dependencies?
- Circular dependencies?
- Testing benefits?

---

## If you mention Bean Lifecycle
- @PostConstruct?
- BeanPostProcessor?
- Destroy methods?
- Prototype destruction?
- Initialization order?

---

## If you mention Scopes
- Thread safety?
- Prototype into Singleton?
- Scoped Proxy?
- Request Scope?
- Session Scope?

---

## If you mention Proxies
- JDK vs CGLIB?
- @Transactional?
- @Async?
- Self Invocation?
- AOP?

---

## If you mention Component Scanning
- Package structure?
- Filters?
- Performance?
- Auto Configuration?
- Bean discovery?

---

# Staff Engineer Discussion Questions

### Q261.
How would you structure Spring configuration across 100+ microservices?

---

### Q262.
How do you minimize Spring startup time in large applications?

---

### Q263.
How do you review Spring code for dependency injection anti-patterns?

---

### Q264.
When should business code avoid framework-specific annotations?

---

### Q265.
How do Spring proxies influence application architecture?

---

### Q266.
How do you design beans for thread safety in high-concurrency applications?

---

### Q267.
What metrics would you monitor to identify Spring startup bottlenecks?

---

### Q268.
How do you balance auto-configuration convenience with explicit configuration?

---

### Q269.
How would you onboard junior engineers to Spring Core concepts effectively?

---

### Q270.
If you were redesigning Spring Core today, what would you improve and why?

---

# Completion Checklist

## Fundamentals
- [ ] IoC
- [ ] Dependency Injection
- [ ] BeanFactory
- [ ] ApplicationContext
- [ ] Spring Bean

## Bean Management
- [ ] Bean Lifecycle
- [ ] Bean Scopes
- [ ] Bean Configuration
- [ ] Dependency Resolution
- [ ] Lazy Initialization

## Dependency Injection
- [ ] Constructor Injection
- [ ] Setter Injection
- [ ] Field Injection
- [ ] @Autowired
- [ ] @Qualifier
- [ ] @Primary

## Configuration
- [ ] Component Scanning
- [ ] Profiles
- [ ] Properties
- [ ] ConfigurationProperties
- [ ] SpEL

## Advanced
- [ ] BeanPostProcessor
- [ ] BeanFactoryPostProcessor
- [ ] FactoryBean
- [ ] Spring Events
- [ ] Resource Loading

## AOP & Proxies
- [ ] Spring AOP
- [ ] JDK Proxy
- [ ] CGLIB
- [ ] Self Invocation
- [ ] Cross-Cutting Concerns

## Production
- [ ] Startup Optimization
- [ ] Bean Resolution
- [ ] Circular Dependencies
- [ ] Environment Configuration
- [ ] Thread Safety

## Interview Readiness
- [ ] Can explain the complete Spring Bean lifecycle from memory.
- [ ] Can describe IoC container internals and dependency resolution.
- [ ] Can compare all injection techniques with production trade-offs.
- [ ] Can explain how Spring proxies enable transactions, security, and AOP.
- [ ] Can diagnose common Spring Core production issues confidently.

---

**Total Questions:** 270
**Recommended Time:** 5–6 Days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Extremely High)
**Most Frequently Asked Topics:** IoC Container, Dependency Injection, Bean Lifecycle, Bean Scopes, Constructor Injection, @Autowired, Component Scanning, BeanPostProcessor, AOP, Spring Proxies, Circular Dependencies, @Configuration vs @Component