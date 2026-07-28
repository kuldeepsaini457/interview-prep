# Java Core Interview Question Bank (SDE-2 Backend)
> **Target Audience:** Backend Engineers with ~3 Years of Experience
>
> **Focus:** Amazon, Microsoft, Walmart Global Tech, Atlassian, Adobe, Salesforce, Uber, Razorpay, PhonePe, Flipkart, LinkedIn, Google, etc.
>
> **Instructions**
> - Do **NOT** look at answers immediately.
> - Try answering each question aloud.
> - Draw diagrams whenever appropriate.
> - Think from a production perspective instead of only textbook definitions.
> - Every question can have multiple follow-up questions in a real interview.

---

# Table of Contents

1. Basic
2. Intermediate
3. Advanced
4. Scenario-Based
5. Production Experience
6. Why Questions
7. Trade-offs
8. Common Follow-up Questions

---

# 1. Basic Questions

## Java Fundamentals

### Q1.
What is Java?

**Possible Follow-ups**
- Why is Java platform independent?
- What makes Java object-oriented?
- Is Java completely object-oriented?

---

### Q2.
Explain JVM, JDK and JRE.

**Follow-ups**

- Why do we need JDK?
- Can a machine have multiple JDKs?
- What happens if only JRE is installed?

---

### Q3.

Explain Java's "Write Once, Run Anywhere."

**Follow-ups**

- Is it really true?
- Why can Java run on Windows and Linux without recompilation?

---

### Q4.

How is Java compiled and executed?

**Follow-ups**

- What is bytecode?
- Who executes bytecode?
- What is JIT?

---

### Q5.

Primitive data types in Java?

**Follow-ups**

- Why is boolean size JVM dependent?
- Why is char 2 bytes?

---

### Q6.

Difference between primitive types and wrapper classes.

**Follow-ups**

- Why do wrapper classes exist?
- Where have you used wrappers in Spring Boot?

---

### Q7.

What is autoboxing and unboxing?

**Follow-ups**

- Performance implications?
- Can it cause NullPointerException?

---

### Q8.

Difference between == and equals().

**Follow-ups**

- Why does String override equals()?
- When is == correct?

---

### Q9.

Difference between String, StringBuilder and StringBuffer.

**Follow-ups**

- Why is String immutable?
- Which one is thread-safe?
- Which one is faster?

---

### Q10.

What is String Pool?

**Follow-ups**

- Where is String Pool stored?
- What happens with new String("abc")?

---

### Q11.

Why is String immutable?

**Follow-ups**

- Security implications?
- HashMap implications?
- Thread safety implications?

---

### Q12.

Explain Object class.

**Follow-ups**

- Which methods are inherited?
- Which methods are commonly overridden?

---

### Q13.

Explain hashCode() and equals() contract.

**Follow-ups**

- What happens if contract breaks?
- Impact on HashMap?

---

### Q14.

Difference between final, finally and finalize().

**Follow-ups**

- Is finalize deprecated?
- Why?

---

### Q15.

What are access modifiers?

**Follow-ups**

- package-private?
- protected across packages?

---

### Q16.

Difference between abstract class and interface.

**Follow-ups**

- Java 8 changes?
- Java 9 changes?
- Which one should you prefer?

---

### Q17.

Can an interface have constructors?

---

### Q18.

Can abstract class have constructors?

---

### Q19.

What is polymorphism?

---

### Q20.

Compile-time vs Runtime polymorphism.

---

### Q21.

Method overloading vs overriding.

---

### Q22.

Rules of overriding.

---

### Q23.

Can static methods be overridden?

---

### Q24.

Can private methods be overridden?

---

### Q25.

Can constructors be overridden?

---

### Q26.

What is inheritance?

---

### Q27.

Multiple inheritance in Java?

**Follow-ups**

- Diamond problem?
- How do interfaces solve it?

---

### Q28.

What is encapsulation?

---

### Q29.

What is abstraction?

---

### Q30.

Composition vs Inheritance.

---

# 2. Intermediate Questions

## Object-Oriented Design

### Q31.

When should you use composition over inheritance?

---

### Q32.

What problems does inheritance create?

---

### Q33.

How do SOLID principles influence Java class design?

---

### Q34.

Difference between IS-A and HAS-A relationship.

---

### Q35.

Can you break encapsulation accidentally?

---

### Q36.

Why should mutable fields be private?

---

### Q37.

How do immutable classes improve concurrency?

---

### Q38.

How would you create your own immutable class?

---

### Q39.

What should be final in an immutable class?

---

### Q40.

Why should defensive copying be used?

---

## Memory & Objects

### Q41.

Where are objects created?

---

### Q42.

Where are local variables stored?

---

### Q43.

What is stack memory?

---

### Q44.

What is heap memory?

---

### Q45.

Difference between stack and heap.

---

### Q46.

What causes StackOverflowError?

---

### Q47.

What causes OutOfMemoryError?

---

### Q48.

Difference between reference variable and object.

---

### Q49.

What happens during object creation?

**Expected discussion**

- Memory allocation
- Constructor
- Default values
- Initialization blocks
- Parent constructor

---

### Q50.

What happens if constructor throws exception?

---

### Q51.

Can object exist without reference?

---

### Q52.

Can multiple references point to same object?

---

### Q53.

Difference between shallow copy and deep copy.

---

### Q54.

How would you clone an object?

---

### Q55.

Problems with Cloneable interface?

---

## Static

### Q56.

What is static keyword?

---

### Q57.

Static variable vs instance variable.

---

### Q58.

Static block use cases.

---

### Q59.

When are static blocks executed?

---

### Q60.

Can static method access instance variables?

---

### Q61.

Can instance method access static members?

---

### Q62.

Can constructors be static?

---

### Q63.

When should utility classes use static methods?

---

# 3. Advanced Questions

## Advanced OOP

### Q64.

Explain dynamic method dispatch.

---

### Q65.

How does JVM decide which overridden method to call?

---

### Q66.

Difference between early binding and late binding.

---

### Q67.

How does Java achieve runtime polymorphism internally?

---

### Q68.

Can fields be polymorphic?

---

### Q69.

What happens if subclass hides parent field?

---

### Q70.

Method hiding vs method overriding.

---

## Language Features

### Q71.

What is pass-by-value in Java?

**Common Trap**

Is Java pass-by-reference?

---

### Q72.

Explain parameter passing using objects.

---

### Q73.

Can you modify object passed as parameter?

---

### Q74.

Can you reassign caller reference?

---

### Q75.

What is covariant return type?

---

### Q76.

Explain initialization order in Java.

Expected discussion:

- Static fields
- Static blocks
- Parent
- Child
- Instance variables
- Constructor

---

### Q77.

Can constructor call overridden method?

---

### Q78.

Why is calling overridable methods inside constructor dangerous?

---

### Q79.

Difference between checked and unchecked exceptions.

---

### Q80.

Can interface contain private methods?

---

### Q81.

Can interface contain static methods?

---

### Q82.

Default methods in interfaces.

---

### Q83.

Why were default methods introduced?

---

### Q84.

Multiple default methods conflict.

---

### Q85.

Explain diamond problem with default methods.

---

# 4. Scenario-Based Questions

### Q86.

You have a class with 25 fields.

How would you redesign it?

---

### Q87.

A class has over 100 methods.

What problems do you foresee?

---

### Q88.

A service method accepts 15 parameters.

How would you redesign it?

---

### Q89.

You discover deep inheritance (7 levels).

Would you keep it?

Why?

---

### Q90.

You need to expose read-only object to clients.

How would you design it?

---

### Q91.

Multiple developers keep modifying shared objects causing bugs.

How would you solve this?

---

### Q92.

Your HashMap suddenly behaves incorrectly.

Where would you start debugging?

---

### Q93.

You observe duplicate objects with same values inside HashSet.

Possible reasons?

---

### Q94.

Team frequently misuses equals().

How would you enforce correctness?

---

### Q95.

A class has mutable public fields.

What problems may occur?

---

# 5. Production Experience Questions

### Q96.

Have you ever created custom immutable classes?

Where?

---

### Q97.

How do you design DTOs?

---

### Q98.

How do you design Entity classes?

---

### Q99.

Where have you used interfaces in your project?

---

### Q100.

Where have you used abstract classes?

---

### Q101.

Did inheritance ever create maintenance issues?

---

### Q102.

Have you overridden equals() in production?

Why?

---

### Q103.

Have you overridden hashCode()?

Where?

---

### Q104.

How do you design utility classes?

---

### Q105.

Have you encountered memory-related bugs?

---

### Q106.

Did mutable shared objects ever create concurrency issues?

---

### Q107.

How do you review Java code for OOP violations?

---

### Q108.

How do you avoid tight coupling?

---

### Q109.

What Java feature do developers misuse the most?

---

### Q110.

What Java coding standards does your team follow?

---

# 6. "Why" Questions

These are favorites in senior interviews.

### Q111.

Why is String immutable?

---

### Q112.

Why is Object the root class?

---

### Q113.

Why is Java pass-by-value?

---

### Q114.

Why can't constructors be inherited?

---

### Q115.

Why can't constructors be overridden?

---

### Q116.

Why can't abstract methods be final?

---

### Q117.

Why can't interface fields be mutable?

---

### Q118.

Why should equals() and hashCode() be consistent?

---

### Q119.

Why should mutable objects rarely be keys in HashMap?

---

### Q120.

Why is composition preferred over inheritance?

---

# 7. Trade-off Questions

### Q121.

Abstract class vs Interface.

When would you choose each?

---

### Q122.

Inheritance vs Composition.

---

### Q123.

Mutable object vs Immutable object.

---

### Q124.

Primitive vs Wrapper.

---

### Q125.

Static methods vs Instance methods.

---

### Q126.

DTO vs Entity.

---

### Q127.

Builder pattern vs Constructor.

---

### Q128.

Factory vs Constructor.

---

### Q129.

Deep copy vs Shallow copy.

---

### Q130.

Public fields vs Getters/Setters.

---

# 8. Common Interview Follow-up Questions

These are the questions interviewers ask immediately after your first answer.

## If you mention String

- Why immutable?
- Where stored?
- String Pool?
- Interning?
- Performance implications?
- Security implications?

---

## If you mention Interface

- Why not abstract class?
- Java 8 changes?
- Java 9 changes?
- Multiple inheritance?
- Default methods?

---

## If you mention equals()

- hashCode?
- HashMap?
- HashSet?
- Mutable keys?

---

## If you mention inheritance

- Why not composition?
- SOLID violation?
- Tight coupling?
- Testing implications?

---

## If you mention constructors

- Order of execution?
- Parent constructor?
- Static blocks?
- Instance blocks?
- Exception inside constructor?

---

## If you mention static

- Class loading?
- Memory?
- Thread safety?
- Utility classes?
- Singleton?

---

## If you mention polymorphism

- Runtime dispatch?
- Dynamic binding?
- JVM implementation?
- VTables?
- Performance?

---

## If you mention Object

- hashCode()
- equals()
- clone()
- finalize()
- wait()
- notify()
- toString()

---

# Staff Engineer Discussion Questions

These questions are commonly asked for SDE-2 and above to assess design maturity.

### Q131.

How do you design Java code that remains maintainable after five years?

---

### Q132.

What Java language features are overused in enterprise applications?

---

### Q133.

What Java code smells do you notice most during code reviews?

---

### Q134.

How would you teach Java fundamentals to a junior engineer?

---

### Q135.

If you could remove one Java feature, what would it be and why?

---

### Q136.

How do you balance readability and abstraction in Java?

---

### Q137.

How do you identify over-engineering in Java code?

---

### Q138.

What indicators tell you a Java class violates the Single Responsibility Principle?

---

### Q139.

How do you decide whether a class should be mutable or immutable?

---

### Q140.

What Java design mistakes become expensive as a codebase grows?

---

# Completion Checklist

## Basic
- [ ] Java fundamentals
- [ ] OOP principles
- [ ] String
- [ ] Object class
- [ ] Access modifiers
- [ ] Abstract class
- [ ] Interface
- [ ] Polymorphism
- [ ] Inheritance
- [ ] Encapsulation

## Intermediate
- [ ] Object lifecycle
- [ ] Memory model
- [ ] Static keyword
- [ ] Object copying
- [ ] Immutable classes

## Advanced
- [ ] Dynamic dispatch
- [ ] Binding
- [ ] Parameter passing
- [ ] Initialization order
- [ ] Default methods
- [ ] Covariant returns

## Production
- [ ] DTO design
- [ ] Entity design
- [ ] Utility classes
- [ ] Code review practices
- [ ] OOP in production

## Interview Readiness
- [ ] Can answer every "Why?" question.
- [ ] Can explain trade-offs with examples.
- [ ] Can relate concepts to production experience.
- [ ] Can handle follow-up questions without hesitation.
- [ ] Can discuss design decisions rather than just definitions.

---

**Total Questions:** 140+
**Recommended Time:** 2–3 days
**Interview Weight:** ⭐⭐⭐⭐⭐ (Very High)