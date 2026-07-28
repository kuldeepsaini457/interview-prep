# Git Interview Question Bank (SDE-2 Backend)

> **Target Audience:** Backend Engineers with 2–5 Years of Experience
>
> **Focus:** Amazon, Google, Microsoft, Uber, Netflix, LinkedIn, Atlassian, Adobe, Walmart Global Tech, PhonePe, Razorpay, Flipkart, Swiggy, Meesho, etc.
>
> **Technology Focus:** Git, GitHub, GitLab, Bitbucket, Branching Strategies, Code Review, Release Management
>
> **Interview Weight:** ⭐⭐⭐⭐☆ (High)
>
> Git is the foundation of collaborative software development. SDE-2 engineers are expected to understand Git internals, branching strategies, merge conflict resolution, history rewriting, release management, and production workflows. This guide covers everything from Git fundamentals to advanced production scenarios.

---

# Table of Contents

## Part I — Git Fundamentals
1. Version Control
2. Git Architecture
3. Repository Basics
4. Git Objects
5. Commit Lifecycle

---

## Part II — Daily Git Commands
6. Repository Management
7. Branch Management
8. Staging Area
9. Commit Management
10. History Inspection

---

## Part III — Branching Strategies
11. Feature Branch Workflow
12. Git Flow
13. GitHub Flow
14. Trunk-Based Development
15. Release Branching

---

## Part IV — Advanced Git
16. Rebase
17. Cherry-pick
18. Stash
19. Reset
20. Revert

---

## Part V — Collaboration
21. Pull Requests
22. Code Reviews
23. Merge Conflicts
24. Fork Workflow
25. Protected Branches

---

## Part VI — Git Internals
26. HEAD
27. Index
28. Reflog
29. Garbage Collection
30. Pack Files

---

## Part VII — Production Workflows
31. Releases
32. Hotfixes
33. Rollbacks
34. Large Repositories
35. Git Best Practices

---

## Part VIII — Staff Engineer Discussions
36. Repository Standards
37. Branch Protection
38. Code Review Culture
39. Release Governance
40. Organization-wide Git Strategy

---

# 1. Git Fundamentals

## Basic

### Q1.
What is Version Control?

---

### Q2.
What is Git?

---

### Q3.
Git vs GitHub.

---

### Q4.
Git vs SVN.

---

### Q5.
Centralized vs Distributed Version Control.

---

### Q6.
Explain Git architecture.

---

### Q7.
What is a Git repository?

---

### Q8.
Working Directory vs Staging Area vs Repository.

---

### Q9.
What is the Git Index?

---

### Q10.
Explain the Git commit lifecycle.

---

### Q11.
What is a commit?

---

### Q12.
What makes a good commit?

---

### Q13.
How should commits be organized?

---

### Q14.
Why are small commits preferred?

---

### Q15.
Git best practices.

---

# 2. Git Daily Commands

## Highest Priority

### Q16.
git init

---

### Q17.
git clone

---

### Q18.
git status

---

### Q19.
git add

---

### Q20.
git commit

---

### Q21.
git push

---

### Q22.
git pull

---

### Q23.
git fetch

---

### Q24.
git merge

---

### Q25.
git checkout

---

### Q26.
git switch

---

### Q27.
git branch

---

### Q28.
git log

---

### Q29.
git diff

---

### Q30.
git show

---

### Q31.
git tag

---

### Q32.
Annotated vs Lightweight Tags.

---

### Q33.
git remote

---

### Q34.
git mv

---

### Q35.
git rm

---

# 3. Branching Strategies

## Highest Priority

### Q36.
What is branching?

---

### Q37.
Feature Branch Workflow.

---

### Q38.
Git Flow.

---

### Q39.
GitHub Flow.

---

### Q40.
Trunk-Based Development.

---

### Q41.
Release Branches.

---

### Q42.
Hotfix Branches.

---

### Q43.
Long-lived vs Short-lived branches.

---

### Q44.
When should branches be deleted?

---

### Q45.
Branch naming conventions.

---

### Q46.
Protected branches.

---

### Q47.
Why avoid long-running branches?

---

### Q48.
Merge frequently vs Large merges.

---

### Q49.
Feature flags vs Feature branches.

---

### Q50.
Branching best practices.

---

# 4. Advanced Git Commands

## Highest Priority

### Q51.
git rebase

---

### Q52.
Merge vs Rebase.

---

### Q53.
Interactive Rebase.

---

### Q54.
Squash commits.

---

### Q55.
git cherry-pick

---

### Q56.
git stash

---

### Q57.
git stash pop vs apply.

---

### Q58.
git reset --soft

---

### Q59.
git reset --mixed

---

### Q60.
git reset --hard

---

### Q61.
git revert

---

### Q62.
Reset vs Revert.

---

### Q63.
git reflog

---

### Q64.
Recovering deleted commits.

---

### Q65.
Undoing accidental commits.

---

### Q66.
Undoing pushed commits.

---

### Q67.
Amending commits.

---

### Q68.
Cleaning untracked files.

---

### Q69.
Force push.

---

### Q70.
When should force push never be used?

---

# 5. Merge Conflicts & Collaboration

### Q71.
What causes merge conflicts?

---

### Q72.
How do you resolve merge conflicts?

---

### Q73.
Conflict markers.

---

### Q74.
Binary file conflicts.

---

### Q75.
How do Pull Requests work?

---

### Q76.
Why are code reviews important?

---

### Q77.
Draft Pull Requests.

---

### Q78.
Review comments.

---

### Q79.
Approval workflow.

---

### Q80.
Merge queues.

---

### Q81.
Branch protection rules.

---

### Q82.
Required status checks.

---

### Q83.
Signed commits.

---

### Q84.
Commit message conventions.

---

### Q85.
Collaboration best practices.

---

# 6. Git Internals

### Q86.
How does Git store data?

---

### Q87.
Blob objects.

---

### Q88.
Tree objects.

---

### Q89.
Commit objects.

---

### Q90.
Tag objects.

---

### Q91.
SHA-1 hashes.

---

### Q92.
HEAD.

---

### Q93.
Detached HEAD.

---

### Q94.
What is reflog?

---

### Q95.
Git garbage collection.

---

### Q96.
Pack files.

---

### Q97.
Loose objects.

---

### Q98.
How does Git compress repositories?

---

### Q99.
How does Git detect file changes?

---

### Q100.
Git internals best practices.

---

# 7. Production Workflows

### Q101.
Describe your team's Git workflow.

---

### Q102.
How do you prepare a release?

---

### Q103.
How do you create release tags?

---

### Q104.
How do you apply hotfixes?

---

### Q105.
How do you rollback a release?

---

### Q106.
How do you handle multiple release branches?

---

### Q107.
How do you work with monorepos?

---

### Q108.
Large repository optimization.

---

### Q109.
Git LFS.

---

### Q110.
Production Git best practices.

---

# 8. Production Experience Questions

### Q111.
Describe your Git branching strategy.

---

### Q112.
How are Pull Requests reviewed in your team?

---

### Q113.
How do you resolve merge conflicts?

---

### Q114.
Have you ever lost commits? How did you recover them?

---

### Q115.
Have you used interactive rebase?

---

### Q116.
Describe a difficult merge conflict you solved.

---

### Q117.
How do you review large Pull Requests?

---

### Q118.
How do you ensure high-quality commit history?

---

### Q119.
Have you worked with monorepositories?

---

### Q120.
Describe your release workflow.

---

# 9. Scenario-Based Questions

### Q121.
You accidentally committed a secret API key. What would you do?

---

### Q122.
You accidentally force-pushed to the main branch. What is your recovery plan?

---

### Q123.
A production hotfix must be released immediately while a major feature is under development. How would you manage Git branches?

---

### Q124.
Your branch has diverged significantly from main. How would you synchronize it?

---

### Q125.
A teammate deleted an important branch. How would you recover it?

---

### Q126.
You accidentally deleted local commits. How would you recover them?

---

### Q127.
A Pull Request contains 2,000 changed files. How would you review it?

---

### Q128.
A merge conflict spans dozens of files. How would you resolve it safely?

---

### Q129.
Your repository has become extremely slow because of large binary files. How would you fix it?

---

### Q130.
How would you migrate a team from Git Flow to Trunk-Based Development?

---

# 10. "Why" Questions

### Q131.
Why is Git distributed?

---

### Q132.
Why are commits immutable?

---

### Q133.
Why should commits be atomic?

---

### Q134.
Why is rebasing discouraged on shared branches?

---

### Q135.
Why is `git revert` safer than `git reset` for shared repositories?

---

### Q136.
Why should feature branches be short-lived?

---

### Q137.
Why should protected branches be enabled?

---

### Q138.
Why should commits have meaningful messages?

---

### Q139.
Why should history rewriting be used carefully?

---

### Q140.
Why are code reviews important before merging?

---

# 11. Trade-off Questions

### Q141.
Merge vs Rebase.

---

### Q142.
Reset vs Revert.

---

### Q143.
Fetch vs Pull.

---

### Q144.
Cherry-pick vs Merge.

---

### Q145.
Git Flow vs GitHub Flow.

---

### Q146.
Git Flow vs Trunk-Based Development.

---

### Q147.
Squash Merge vs Merge Commit.

---

### Q148.
Fork Workflow vs Branch Workflow.

---

### Q149.
Monorepo vs Polyrepo.

---

### Q150.
Annotated Tag vs Lightweight Tag.

---

# 12. Common Interview Follow-up Questions

## If you mention Git Flow
- Why Git Flow?
- Release branches?
- Hotfixes?
- Feature branches?
- Draw the workflow.

---

## If you mention Rebase
- Interactive rebase?
- Squashing?
- Conflict resolution?
- Force push?
- Shared branches?

---

## If you mention Pull Requests
- Required approvals?
- Status checks?
- Merge strategy?
- CI integration?
- Branch protection?

---

## If you mention Git Internals
- Blob?
- Tree?
- Commit?
- HEAD?
- Reflog?

---

## If you mention Releases
- Tags?
- Rollback?
- Hotfix?
- Versioning?
- Release branches?

---

# Staff Engineer Discussion Questions

### Q151.
How would you establish Git standards across hundreds of repositories?

---

### Q152.
How would you standardize branching strategies across engineering teams?

---

### Q153.
How would you improve Pull Request quality across an organization?

---

### Q154.
How would you reduce merge conflicts in a large engineering team?

---

### Q155.
How would you manage releases for hundreds of microservices?

---

### Q156.
How would you migrate an organization from Git Flow to Trunk-Based Development?

---

### Q157.
How would you organize repositories for a platform team?

---

### Q158.
How would you manage monorepos at scale?

---

### Q159.
Which Git metrics would you monitor to improve engineering productivity?

---

### Q160.
If you were responsible for engineering productivity, what Git standards would you enforce?

---

# Completion Checklist

## Fundamentals
- [ ] Version Control
- [ ] Git Architecture
- [ ] Repository Structure
- [ ] Staging Area
- [ ] Commit Lifecycle

## Daily Commands
- [ ] clone
- [ ] add
- [ ] commit
- [ ] push
- [ ] pull

## Branching
- [ ] Feature Branches
- [ ] Git Flow
- [ ] GitHub Flow
- [ ] Trunk-Based Development
- [ ] Protected Branches

## Advanced Git
- [ ] Rebase
- [ ] Cherry-pick
- [ ] Reset
- [ ] Revert
- [ ] Reflog

## Collaboration
- [ ] Pull Requests
- [ ] Code Reviews
- [ ] Merge Conflicts
- [ ] Branch Protection
- [ ] Merge Strategies

## Git Internals
- [ ] HEAD
- [ ] Blob
- [ ] Tree
- [ ] Commit Objects
- [ ] Pack Files

## Production
- [ ] Releases
- [ ] Hotfixes
- [ ] Rollbacks
- [ ] Monorepos
- [ ] Git LFS

## Interview Readiness
- [ ] Can explain Git internals, including blobs, trees, commits, and the staging area.
- [ ] Can confidently use advanced commands like rebase, reflog, cherry-pick, reset, and revert.
- [ ] Can compare branching strategies and justify the right choice for different teams.
- [ ] Can handle production Git scenarios such as hotfixes, rollbacks, and secret removal.
- [ ] Can discuss real Git workflows, code review practices, and repository management.

---

**Total Questions:** **160**

**Recommended Study Time:** **4–5 Days**

**Interview Weight:** ⭐⭐⭐⭐☆ (High)

**Most Frequently Asked Topics:** Merge vs Rebase, Reset vs Revert, Fetch vs Pull, Cherry-pick, Interactive Rebase, Git Flow, Trunk-Based Development, Merge Conflicts, Reflog, Pull Requests, Branch Protection, Git Internals, Monorepos, Release Management