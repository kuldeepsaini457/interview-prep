# CI/CD Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with 2–5 Years of Experience
>
> **Focus:** Amazon, Google, Microsoft, Uber, Netflix, LinkedIn, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Meesho, etc.
>
> **Technology Focus:** Git, GitHub Actions, GitLab CI/CD, Jenkins, Docker, Kubernetes, Helm, SonarQube, Nexus, ArgoCD
>
> **Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)
>
> Continuous Integration and Continuous Delivery (CI/CD) are fundamental to modern software engineering. SDE-2 engineers are expected to understand automated pipelines, deployment strategies, quality gates, artifact management, infrastructure automation, and production deployment practices. This guide covers everything from source code commit to production deployment.

---

# Table of Contents

## Part I — CI/CD Fundamentals
1. Continuous Integration
2. Continuous Delivery
3. Continuous Deployment
4. CI/CD Pipeline
5. Pipeline Stages

---

## Part II — Build Automation
6. Build Tools
7. Dependency Management
8. Artifact Generation
9. Versioning
10. Build Optimization

---

## Part III — CI Tools
11. Jenkins
12. GitHub Actions
13. GitLab CI/CD
14. Azure DevOps
15. Bamboo

---

## Part IV — CD & Deployment
16. Deployment Strategies
17. Docker
18. Kubernetes
19. Helm
20. Rollbacks

---

## Part V — Quality Gates
21. Unit Testing
22. Integration Testing
23. Static Code Analysis
24. Security Scanning
25. Code Coverage

---

## Part VI — Artifact Management
26. Nexus
27. JFrog Artifactory
28. Docker Registry
29. Versioning
30. Release Management

---

## Part VII — Infrastructure Automation
31. Infrastructure as Code
32. Terraform
33. Configuration Management
34. Secrets Management
35. Environment Management

---

## Part VIII — GitOps
36. GitOps Principles
37. ArgoCD
38. FluxCD
39. Kubernetes Deployments
40. Declarative Infrastructure

---

## Part IX — Production Deployments
41. Blue-Green Deployment
42. Canary Deployment
43. Rolling Updates
44. Feature Flags
45. Zero Downtime Deployment

---

## Part X — Production Operations
46. Monitoring Deployments
47. Rollbacks
48. Incident Response
49. Pipeline Optimization
50. DevOps Best Practices

---

# 1. CI/CD Fundamentals

## Basic

### Q1.
What is Continuous Integration (CI)?

---

### Q2.
What is Continuous Delivery (CD)?

---

### Q3.
What is Continuous Deployment?

---

### Q4.
Continuous Delivery vs Continuous Deployment.

---

### Q5.
Why is CI/CD important?

---

### Q6.
Explain a typical CI/CD pipeline.

---

### Q7.
What are the stages of a CI/CD pipeline?

---

### Q8.
What happens after a developer pushes code?

---

### Q9.
Why should builds be automated?

---

### Q10.
What makes a CI/CD pipeline successful?

---

### Q11.
What are pipeline quality gates?

---

### Q12.
Pipeline failure handling.

---

### Q13.
How do CI/CD pipelines improve developer productivity?

---

### Q14.
Common CI/CD bottlenecks.

---

### Q15.
CI/CD best practices.

---

# 2. Build Automation

### Q16.
What is build automation?

---

### Q17.
Gradle vs Maven.

---

### Q18.
How are artifacts generated?

---

### Q19.
Snapshot vs Release builds.

---

### Q20.
Semantic Versioning.

---

### Q21.
Dependency management.

---

### Q22.
Incremental builds.

---

### Q23.
Build caching.

---

### Q24.
Parallel builds.

---

### Q25.
Build reproducibility.

---

### Q26.
How do you reduce build time?

---

### Q27.
Why should builds be deterministic?

---

### Q28.
Multi-module builds.

---

### Q29.
Build optimization techniques.

---

### Q30.
Common build failures.

---

# 3. CI Tools

## Highest Priority

### Q31.
What is Jenkins?

---

### Q32.
Jenkins Master-Agent architecture.

---

### Q33.
Pipeline as Code.

---

### Q34.
Declarative vs Scripted Pipeline.

---

### Q35.
Jenkinsfile.

---

### Q36.
GitHub Actions workflow.

---

### Q37.
GitHub Actions runners.

---

### Q38.
Self-hosted vs GitHub-hosted runners.

---

### Q39.
GitLab CI/CD pipeline.

---

### Q40.
.gitlab-ci.yml.

---

### Q41.
Pipeline stages.

---

### Q42.
Pipeline jobs.

---

### Q43.
Pipeline caching.

---

### Q44.
Pipeline artifacts.

---

### Q45.
Environment variables.

---

### Q46.
Secrets management.

---

### Q47.
Pipeline matrices.

---

### Q48.
Scheduled pipelines.

---

### Q49.
Manual approval stages.

---

### Q50.
CI tool comparison.

---

# 4. Continuous Delivery & Deployment

## Highest Priority

### Q51.
Continuous Delivery workflow.

---

### Q52.
Rolling Deployment.

---

### Q53.
Blue-Green Deployment.

---

### Q54.
Canary Deployment.

---

### Q55.
Recreate Deployment.

---

### Q56.
A/B Deployment.

---

### Q57.
Feature Flags.

---

### Q58.
Dark Launches.

---

### Q59.
Zero Downtime Deployment.

---

### Q60.
Rollback strategy.

---

### Q61.
Helm deployment.

---

### Q62.
Kubernetes rollout.

---

### Q63.
Deployment health checks.

---

### Q64.
Readiness vs Liveness probes during deployment.

---

### Q65.
Deployment best practices.

---

# 5. Quality Gates

### Q66.
Why run unit tests in CI?

---

### Q67.
Why run integration tests?

---

### Q68.
Static code analysis.

---

### Q69.
SonarQube.

---

### Q70.
Code coverage.

---

### Q71.
Mutation testing.

---

### Q72.
Dependency vulnerability scanning.

---

### Q73.
OWASP Dependency Check.

---

### Q74.
Container image scanning.

---

### Q75.
Quality gate failures.

---

### Q76.
Fail-fast principle.

---

### Q77.
Build breakers.

---

### Q78.
Artifact signing.

---

### Q79.
License compliance.

---

### Q80.
Quality gate best practices.

---

# 6. Artifact Management

### Q81.
What is Nexus Repository?

---

### Q82.
Artifactory vs Nexus.

---

### Q83.
Artifact Repository.

---

### Q84.
Docker Registry.

---

### Q85.
Image tagging strategy.

---

### Q86.
Immutable artifacts.

---

### Q87.
Release management.

---

### Q88.
Version promotion.

---

### Q89.
Artifact retention.

---

### Q90.
Artifact lifecycle.

---

# 7. Infrastructure Automation

### Q91.
Infrastructure as Code.

---

### Q92.
Terraform basics.

---

### Q93.
Secrets management.

---

### Q94.
Vault.

---

### Q95.
Environment variables.

---

### Q96.
Configuration management.

---

### Q97.
Environment-specific configurations.

---

### Q98.
Infrastructure provisioning.

---

### Q99.
Infrastructure drift.

---

### Q100.
Infrastructure automation best practices.

---

# 8. GitOps

### Q101.
What is GitOps?

---

### Q102.
GitOps workflow.

---

### Q103.
ArgoCD.

---

### Q104.
FluxCD.

---

### Q105.
Declarative deployments.

---

### Q106.
Desired state reconciliation.

---

### Q107.
Automatic synchronization.

---

### Q108.
Git as the source of truth.

---

### Q109.
GitOps benefits.

---

### Q110.
GitOps challenges.

---

# 9. Production Deployments

### Q111.
How would you deploy a Spring Boot microservice to Kubernetes?

---

### Q112.
How do you perform a zero-downtime deployment?

---

### Q113.
How do you safely deploy to production?

---

### Q114.
How do you monitor deployments?

---

### Q115.
How do you validate a deployment?

---

### Q116.
How do you rollback a deployment?

---

### Q117.
How do you deploy database schema changes?

---

### Q118.
How do feature flags reduce deployment risk?

---

### Q119.
How would you deploy to multiple regions?

---

### Q120.
Deployment best practices.

---

# 10. Production Experience Questions

### Q121.
Describe your CI/CD pipeline.

---

### Q122.
Which CI/CD tools does your team use?

---

### Q123.
How are artifacts stored?

---

### Q124.
Describe your deployment strategy.

---

### Q125.
How do you perform rollbacks?

---

### Q126.
Have you worked with GitHub Actions?

---

### Q127.
Have you worked with GitLab CI/CD?

---

### Q128.
Have you configured Jenkins pipelines?

---

### Q129.
Describe a pipeline failure you resolved.

---

### Q130.
How do you optimize pipeline execution time?

---

# 11. Scenario-Based Questions

### Q131.
A deployment fails halfway through. What would you do?

---

### Q132.
Production deployment succeeds, but health checks fail. How would you investigate?

---

### Q133.
A pipeline suddenly takes twice as long to complete. How do you debug it?

---

### Q134.
Your Docker image size has grown from 300 MB to 1.5 GB. How would you optimize it?

---

### Q135.
A Kubernetes rollout gets stuck. What could be the reasons?

---

### Q136.
A security scan fails because of a vulnerable dependency. How would you handle it?

---

### Q137.
Your artifact repository becomes unavailable during deployment. What happens next?

---

### Q138.
A rollback also fails. What is your recovery plan?

---

### Q139.
How would you implement CI/CD for a microservices architecture with 100+ services?

---

### Q140.
How would you migrate a team from manual deployments to automated CI/CD?

---

# 12. "Why" Questions

### Q141.
Why should deployments be automated?

---

### Q142.
Why should pipelines fail fast?

---

### Q143.
Why should artifacts be immutable?

---

### Q144.
Why should secrets never be stored in Git?

---

### Q145.
Why should production deployments require quality gates?

---

### Q146.
Why is Blue-Green deployment safer than Recreate deployment?

---

### Q147.
Why are feature flags preferred over long-lived branches?

---

### Q148.
Why should infrastructure be managed as code?

---

### Q149.
Why is GitOps becoming popular?

---

### Q150.
Why should deployments be reproducible?

---

# 13. Trade-off Questions

### Q151.
Jenkins vs GitHub Actions.

---

### Q152.
GitHub Actions vs GitLab CI/CD.

---

### Q153.
Blue-Green vs Canary Deployment.

---

### Q154.
Rolling Update vs Recreate.

---

### Q155.
Continuous Delivery vs Continuous Deployment.

---

### Q156.
Helm vs Kustomize.

---

### Q157.
Nexus vs Artifactory.

---

### Q158.
Pipeline Cache vs Build Cache.

---

### Q159.
GitOps vs Traditional CI/CD.

---

### Q160.
Feature Flags vs Separate Deployments.

---

# 14. Common Interview Follow-up Questions

## If you mention Jenkins
- Jenkinsfile?
- Declarative pipeline?
- Agents?
- Pipeline stages?
- Shared libraries?

---

## If you mention GitHub Actions
- Workflow YAML?
- Matrix builds?
- Runners?
- Secrets?
- Caching?

---

## If you mention Kubernetes
- Helm?
- Rolling updates?
- Rollbacks?
- Readiness probe?
- Canary?

---

## If you mention GitOps
- ArgoCD?
- Reconciliation?
- Desired state?
- Sync?
- Rollback?

---

## If you mention Production Deployments
- Zero downtime?
- Health checks?
- Feature flags?
- Monitoring?
- Rollback?

---

# Staff Engineer Discussion Questions

### Q161.
How would you design a CI/CD platform for hundreds of engineering teams?

---

### Q162.
How would you standardize deployment strategies across all microservices?

---

### Q163.
How would you reduce deployment risk in a large organization?

---

### Q164.
How would you improve developer productivity through CI/CD?

---

### Q165.
How would you establish organization-wide quality gates?

---

### Q166.
How would you design a secure software supply chain?

---

### Q167.
How would you optimize CI/CD costs in the cloud?

---

### Q168.
How would you manage deployments across multiple Kubernetes clusters?

---

### Q169.
How would you measure CI/CD effectiveness?

---

### Q170.
If you were responsible for platform engineering, what CI/CD standards would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] CI
- [ ] Continuous Delivery
- [ ] Continuous Deployment
- [ ] Pipeline Stages
- [ ] Quality Gates

## Build Automation
- [ ] Gradle/Maven
- [ ] Versioning
- [ ] Build Cache
- [ ] Incremental Builds
- [ ] Artifact Generation

## CI Tools
- [ ] Jenkins
- [ ] GitHub Actions
- [ ] GitLab CI/CD
- [ ] Pipeline as Code
- [ ] Secrets Management

## Deployment
- [ ] Rolling Updates
- [ ] Blue-Green
- [ ] Canary
- [ ] Helm
- [ ] Rollbacks

## Quality
- [ ] Unit Testing
- [ ] Integration Testing
- [ ] SonarQube
- [ ] Security Scanning
- [ ] Code Coverage

## GitOps
- [ ] ArgoCD
- [ ] FluxCD
- [ ] GitOps Workflow
- [ ] Desired State
- [ ] Reconciliation

## Production
- [ ] Zero Downtime Deployment
- [ ] Health Checks
- [ ] Feature Flags
- [ ] Monitoring
- [ ] Incident Recovery

## Interview Readiness
- [ ] Can explain an end-to-end CI/CD pipeline from commit to production.
- [ ] Can compare deployment strategies and choose the appropriate one.
- [ ] Can design secure, scalable CI/CD pipelines for microservices.
- [ ] Can discuss GitOps, Kubernetes deployments, and rollback strategies.
- [ ] Can explain real production deployment experiences and optimizations.

---

**Total Questions:** **170**

**Recommended Study Time:** **5–6 Days**

**Interview Weight:** ⭐⭐⭐⭐⭐ (Highest Priority)

**Most Frequently Asked Topics:** CI/CD Pipeline, Jenkins, GitHub Actions, GitLab CI/CD, Pipeline as Code, Blue-Green Deployment, Canary Deployment, Rolling Updates, Helm, GitOps, ArgoCD, SonarQube, Nexus, Feature Flags, Zero Downtime Deployment