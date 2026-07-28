# Gradle Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with 2–5 Years of Experience
>
> **Focus:** Amazon, Google, Microsoft, Uber, Netflix, LinkedIn, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Meesho, etc.
>
> **Technology Focus:** Gradle, Groovy DSL, Kotlin DSL, Spring Boot, Multi-module Projects, Dependency Management, Build Optimization, CI/CD
>
> **Interview Weight:** ⭐⭐⭐⭐☆ (High)
>
> Gradle is the de facto build automation tool for modern Java and Spring Boot applications. SDE-2 engineers are expected to understand Gradle's build lifecycle, dependency resolution, plugin system, multi-module architecture, performance optimization, and integration with CI/CD pipelines.

---

# Table of Contents

## Part I — Gradle Fundamentals
1. Build Automation
2. Gradle Architecture
3. Build Lifecycle
4. Project Structure
5. Gradle Wrapper

---

## Part II — Build Scripts
6. Groovy DSL
7. Kotlin DSL
8. Plugins
9. Tasks
10. Properties

---

## Part III — Dependency Management
11. Dependency Configurations
12. Version Management
13. Dependency Resolution
14. Conflict Resolution
15. Dependency Locking

---

## Part IV — Multi-module Projects
16. Project Structure
17. Module Dependencies
18. Shared Libraries
19. Composite Builds
20. Convention Plugins

---

## Part V — Build Optimization
21. Incremental Builds
22. Build Cache
23. Parallel Builds
24. Configuration Cache
25. Build Scans

---

## Part VI — Spring Boot & Gradle
26. Spring Boot Plugin
27. Packaging
28. Executable JARs
29. Docker Integration
30. Native Images

---

## Part VII — Testing & Quality
31. Test Execution
32. JaCoCo
33. Checkstyle
34. SpotBugs
35. SonarQube

---

## Part VIII — CI/CD Integration
36. Pipeline Integration
37. Artifact Publishing
38. Repository Management
39. Release Builds
40. Versioning

---

## Part IX — Production Builds
41. Build Performance
42. Reproducible Builds
43. Dependency Security
44. Build Troubleshooting
45. Enterprise Build Practices

---

## Part X — Staff Engineer Discussion
46. Build Platform
47. Organization-wide Standards
48. Build Infrastructure
49. Engineering Productivity
50. Enterprise Build Strategy

---

# 1. Gradle Fundamentals

## Basic

### Q1.
What is Gradle?

---

### Q2.
Why is Gradle used?

---

### Q3.
Gradle vs Maven.

---

### Q4.
Gradle vs Ant.

---

### Q5.
What is build automation?

---

### Q6.
Explain the Gradle architecture.

---

### Q7.
What is the Gradle Wrapper?

---

### Q8.
Why should every project use the Gradle Wrapper?

---

### Q9.
Explain the Gradle project structure.

---

### Q10.
What files are present in a Gradle project?

---

### Q11.
settings.gradle vs build.gradle.

---

### Q12.
What is gradle.properties?

---

### Q13.
How do you execute a Gradle build?

---

### Q14.
What are Gradle Daemons?

---

### Q15.
Gradle best practices.

---

# 2. Gradle Build Lifecycle

## Highest Priority

### Q16.
Explain the Gradle build lifecycle.

---

### Q17.
Initialization Phase.

---

### Q18.
Configuration Phase.

---

### Q19.
Execution Phase.

---

### Q20.
What happens during each phase?

---

### Q21.
How are tasks discovered?

---

### Q22.
How are task dependencies resolved?

---

### Q23.
Task graph.

---

### Q24.
Lazy task configuration.

---

### Q25.
Task ordering.

---

### Q26.
dependsOn vs finalizedBy.

---

### Q27.
mustRunAfter vs shouldRunAfter.

---

### Q28.
Task inputs and outputs.

---

### Q29.
Up-to-date checks.

---

### Q30.
Gradle lifecycle best practices.

---

# 3. Build Scripts & Plugins

### Q31.
Groovy DSL vs Kotlin DSL.

---

### Q32.
How are plugins applied?

---

### Q33.
Core plugins.

---

### Q34.
Java Plugin.

---

### Q35.
Application Plugin.

---

### Q36.
Spring Boot Plugin.

---

### Q37.
Dependency Management Plugin.

---

### Q38.
How do custom plugins work?

---

### Q39.
Convention Plugins.

---

### Q40.
BuildSrc.

---

### Q41.
Version Catalogs.

---

### Q42.
Extra Properties.

---

### Q43.
Custom Gradle Tasks.

---

### Q44.
Task Types.

---

### Q45.
Plugin best practices.

---

# 4. Dependency Management

## Highest Priority

### Q46.
implementation vs api.

---

### Q47.
compileOnly.

---

### Q48.
runtimeOnly.

---

### Q49.
testImplementation.

---

### Q50.
annotationProcessor.

---

### Q51.
How does Gradle resolve dependencies?

---

### Q52.
Dependency graph.

---

### Q53.
Transitive dependencies.

---

### Q54.
Dependency conflict resolution.

---

### Q55.
Dependency exclusions.

---

### Q56.
Forcing dependency versions.

---

### Q57.
Dependency locking.

---

### Q58.
BOM (Bill of Materials).

---

### Q59.
Spring Boot Dependency Management.

---

### Q60.
Dependency management best practices.

---

# 5. Multi-module Projects

### Q61.
Why use multi-module projects?

---

### Q62.
settings.gradle in multi-module builds.

---

### Q63.
Project dependencies.

---

### Q64.
Shared libraries.

---

### Q65.
Composite builds.

---

### Q66.
Convention plugins.

---

### Q67.
Module isolation.

---

### Q68.
Build order.

---

### Q69.
Sharing common configuration.

---

### Q70.
Large project best practices.

---

# 6. Build Optimization

## Highest Priority

### Q71.
Incremental Builds.

---

### Q72.
Build Cache.

---

### Q73.
Local vs Remote Build Cache.

---

### Q74.
Configuration Cache.

---

### Q75.
Parallel Builds.

---

### Q76.
Gradle Daemon optimization.

---

### Q77.
Task avoidance.

---

### Q78.
Build profiling.

---

### Q79.
Build Scan.

---

### Q80.
How do you reduce build time?

---

### Q81.
Common causes of slow builds.

---

### Q82.
Memory tuning for Gradle.

---

### Q83.
JVM arguments for Gradle.

---

### Q84.
Profiling Gradle builds.

---

### Q85.
Performance optimization best practices.

---

# 7. Spring Boot with Gradle

### Q86.
Spring Boot Gradle Plugin.

---

### Q87.
bootJar vs jar.

---

### Q88.
Executable JAR generation.

---

### Q89.
Layered JARs.

---

### Q90.
Docker image generation.

---

### Q91.
Buildpacks.

---

### Q92.
Native Image support.

---

### Q93.
AOT compilation.

---

### Q94.
Spring Boot dependency management.

---

### Q95.
Spring Boot Gradle best practices.

---

# 8. Testing & Code Quality

### Q96.
Running tests with Gradle.

---

### Q97.
Gradle test task.

---

### Q98.
JaCoCo integration.

---

### Q99.
Code coverage.

---

### Q100.
Checkstyle.

---

### Q101.
SpotBugs.

---

### Q102.
PMD.

---

### Q103.
SonarQube integration.

---

### Q104.
Static analysis.

---

### Q105.
Quality gate automation.

---

# 9. CI/CD Integration

### Q106.
Gradle in Jenkins.

---

### Q107.
Gradle in GitHub Actions.

---

### Q108.
Gradle in GitLab CI.

---

### Q109.
Artifact publishing.

---

### Q110.
Publishing to Nexus.

---

### Q111.
Publishing to Artifactory.

---

### Q112.
Versioning strategy.

---

### Q113.
Snapshot vs Release publishing.

---

### Q114.
Reproducible builds.

---

### Q115.
CI/CD best practices.

---

# 10. Production Experience Questions

### Q116.
Describe your Gradle project structure.

---

### Q117.
How do you manage dependencies in your current project?

---

### Q118.
Have you optimized Gradle build times?

---

### Q119.
Have you worked with multi-module Gradle projects?

---

### Q120.
How do you publish artifacts?

---

### Q121.
How do you configure Gradle in CI/CD?

---

### Q122.
Describe a Gradle build issue you resolved.

---

### Q123.
How do you debug dependency conflicts?

---

### Q124.
How do you upgrade Gradle versions?

---

### Q125.
Describe your build optimization strategy.

---

# 11. Scenario-Based Questions

### Q126.
Your Gradle build suddenly takes twice as long. How would you investigate?

---

### Q127.
Two libraries require incompatible versions of the same dependency. How would you resolve it?

---

### Q128.
A multi-module build fails only in CI but works locally. What could be the reasons?

---

### Q129.
Your build works on one machine but fails on another. How would you debug it?

---

### Q130.
A plugin upgrade breaks your build. How would you approach the issue?

---

### Q131.
A Gradle daemon consumes excessive memory. What would you investigate?

---

### Q132.
Your build cache is not being used. How do you debug it?

---

### Q133.
Your artifact fails to publish to Nexus. What would you check?

---

### Q134.
Your Spring Boot executable JAR does not start after deployment. How would you troubleshoot it?

---

### Q135.
How would you migrate a large Maven project to Gradle?

---

# 12. "Why" Questions

### Q136.
Why does Gradle perform better than Maven for many projects?

---

### Q137.
Why use the Gradle Wrapper instead of a locally installed Gradle?

---

### Q138.
Why are incremental builds important?

---

### Q139.
Why is the Configuration Cache significant?

---

### Q140.
Why should dependencies be locked?

---

### Q141.
Why should builds be reproducible?

---

### Q142.
Why are version catalogs recommended?

---

### Q143.
Why should plugins be versioned explicitly?

---

### Q144.
Why should custom build logic be extracted into plugins?

---

### Q145.
Why should build scripts remain declarative?

---

# 13. Trade-off Questions

### Q146.
Gradle vs Maven.

---

### Q147.
Groovy DSL vs Kotlin DSL.

---

### Q148.
implementation vs api.

---

### Q149.
bootJar vs jar.

---

### Q150.
Local Cache vs Remote Cache.

---

### Q151.
Incremental Build vs Full Build.

---

### Q152.
Configuration Cache vs Build Cache.

---

### Q153.
Convention Plugin vs buildSrc.

---

### Q154.
Multi-module vs Monolithic Project.

---

### Q155.
Version Catalogs vs Hardcoded Versions.

---

# 14. Common Interview Follow-up Questions

## If you mention Build Performance
- Build Cache?
- Configuration Cache?
- Daemon?
- Parallel Builds?
- Build Scan?

---

## If you mention Dependency Management
- Transitive dependencies?
- BOM?
- Version conflicts?
- Dependency locking?
- Exclusions?

---

## If you mention Spring Boot
- bootJar?
- Layered JAR?
- Buildpacks?
- Native Image?
- Dependency plugin?

---

## If you mention Multi-module Projects
- settings.gradle?
- Composite builds?
- Convention plugins?
- Shared configuration?
- Module dependencies?

---

## If you mention CI/CD
- Jenkins integration?
- GitHub Actions?
- Artifact publishing?
- Nexus?
- Reproducible builds?

---

# Staff Engineer Discussion Questions

### Q156.
How would you standardize Gradle builds across hundreds of repositories?

---

### Q157.
How would you reduce build times organization-wide?

---

### Q158.
How would you design a shared Gradle plugin for engineering teams?

---

### Q159.
How would you manage dependency upgrades across hundreds of services?

---

### Q160.
How would you enforce reproducible and secure builds?

---

### Q161.
How would you organize a large multi-module platform project?

---

### Q162.
How would you monitor build performance across engineering teams?

---

### Q163.
How would you migrate an organization from Maven to Gradle?

---

### Q164.
Which Gradle metrics would you monitor continuously?

---

### Q165.
If you owned the build platform, what Gradle standards would you establish?

---

# Completion Checklist

## Fundamentals
- [ ] Gradle Architecture
- [ ] Wrapper
- [ ] Build Lifecycle
- [ ] Project Structure
- [ ] Daemon

## Build Lifecycle
- [ ] Initialization
- [ ] Configuration
- [ ] Execution
- [ ] Task Graph
- [ ] Lazy Configuration

## Dependency Management
- [ ] implementation
- [ ] api
- [ ] BOM
- [ ] Dependency Locking
- [ ] Conflict Resolution

## Build Optimization
- [ ] Incremental Builds
- [ ] Build Cache
- [ ] Configuration Cache
- [ ] Parallel Builds
- [ ] Build Scan

## Spring Boot
- [ ] Spring Boot Plugin
- [ ] bootJar
- [ ] Layered JAR
- [ ] Buildpacks
- [ ] Native Images

## CI/CD
- [ ] Jenkins
- [ ] GitHub Actions
- [ ] GitLab CI
- [ ] Artifact Publishing
- [ ] Nexus

## Interview Readiness
- [ ] Can explain the complete Gradle build lifecycle.
- [ ] Can optimize Gradle builds using caches, parallel execution, and profiling.
- [ ] Can manage dependencies and resolve version conflicts confidently.
- [ ] Can discuss multi-module builds and Spring Boot integration.
- [ ] Can explain real production Gradle optimizations and CI/CD integration.

---

**Total Questions:** **165**

**Recommended Study Time:** **4–5 Days**

**Interview Weight:** ⭐⭐⭐⭐☆ (High)

**Most Frequently Asked Topics:** Build Lifecycle, Gradle Wrapper, Groovy vs Kotlin DSL, Dependency Resolution, `implementation` vs `api`, Multi-module Projects, Build Cache, Configuration Cache, Spring Boot Plugin, `bootJar`, Build Scans, Nexus Publishing, CI/CD Integration