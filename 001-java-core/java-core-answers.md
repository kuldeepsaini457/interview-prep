# Q1. What is Java?

### Answer

Java is a high-level, object-oriented programming language designed to be platform independent. You compile Java code once into bytecode, and any system with a compatible JVM can execute it.

The main reasons Java is widely used in backend development are:

* Platform independence through the JVM.
* Strong memory management with Garbage Collection.
* Rich standard library and mature ecosystem.
* Good support for multithreading and concurrency.
* Backward compatibility and long-term stability.

In backend systems, these features make Java suitable for building scalable and maintainable services.

### Expected Follow-up Questions

* Why is Java platform independent?
* Is Java completely object-oriented?
* What makes Java object-oriented?

### Common Mistakes

* Saying Java runs directly on the operating system.
* Saying Java is "100% object-oriented" (primitive types exist).

### Interview Keywords

* JVM
* Bytecode
* Platform Independence
* Garbage Collection
* Object-Oriented Programming

---

# Q2. Explain JVM, JDK and JRE.

### Answer

The easiest way to remember them is:

* **JDK (Java Development Kit)** is used to develop Java applications.
* **JRE (Java Runtime Environment)** is used to run Java applications.
* **JVM (Java Virtual Machine)** is the engine that executes Java bytecode.

Their relationship is:

```
JDK
 ├── JRE
 │    └── JVM
```

* **JDK** contains the compiler (`javac`), debugger, profiler, and other development tools.
* **JRE** contains the JVM and required runtime libraries.
* **JVM** loads classes, verifies bytecode, manages memory, performs garbage collection, and executes the program.

In production servers, we typically only need a runtime environment, while developers require the JDK to compile and build applications.

### Expected Follow-up Questions

* Why do we need the JDK?
* Can multiple JDKs be installed?
* What happens if only JRE is installed?

### Common Mistakes

* Confusing JRE and JVM.
* Saying JVM compiles Java source code.

### Interview Keywords

* javac
* Bytecode
* Runtime
* Class Loader
* Garbage Collection

---

# Q3. Explain Java's "Write Once, Run Anywhere."

### Answer

"Write Once, Run Anywhere" means Java source code is compiled into platform-independent bytecode. That bytecode can run on any operating system that provides a compatible JVM, without recompiling the application.

The compiler generates the same bytecode regardless of whether development happens on Windows, Linux, or macOS. Each platform has its own JVM implementation, which translates the bytecode into native machine instructions.

In practice, this is mostly true. However, if an application depends on native libraries, OS-specific file paths, or platform-specific behavior, additional changes may still be required.

### Expected Follow-up Questions

* Is WORA completely true?
* Why doesn't Java need recompilation for Linux or Windows?

### Common Mistakes

* Saying Java machine code runs everywhere.
* Ignoring platform-specific native dependencies.

### Interview Keywords

* Bytecode
* JVM
* Platform Independence
* Native Code

---

# Q4. How is Java compiled and executed?

### Answer

The execution flow is:

```
Java Source (.java)
        ↓
javac Compiler
        ↓
Bytecode (.class)
        ↓
Class Loader
        ↓
JVM
        ↓
Interpreter + JIT Compiler
        ↓
Machine Code
```

First, the `javac` compiler converts source code into bytecode.

When the application starts:

* The Class Loader loads required classes.
* The JVM verifies the bytecode for safety.
* Initially, the interpreter executes bytecode.
* Frequently executed code (hot methods) is compiled into native machine code by the JIT compiler, improving performance.

This combination gives Java fast startup while allowing long-running applications to achieve near-native performance.

### Expected Follow-up Questions

* What is bytecode?
* What is JIT?
* Why doesn't Java always use JIT immediately?

### Common Mistakes

* Saying JVM directly executes Java source code.
* Confusing the compiler with the JIT compiler.

### Interview Keywords

* Bytecode
* Class Loader
* Interpreter
* JIT Compiler
* HotSpot

---

# Q5. Primitive data types in Java?

### Answer

Java has eight primitive data types:

| Type    | Size          |
| ------- | ------------- |
| byte    | 1 byte        |
| short   | 2 bytes       |
| int     | 4 bytes       |
| long    | 8 bytes       |
| float   | 4 bytes       |
| double  | 8 bytes       |
| char    | 2 bytes       |
| boolean | JVM dependent |

* Integer types store whole numbers.
* `float` and `double` store decimal values.
* `char` stores a UTF-16 Unicode character, so it uses 2 bytes.
* The Java Language Specification does not define the storage size of `boolean`; it only defines its values (`true` and `false`), so the JVM decides the internal representation.

Primitive types are stored by value and are generally faster and more memory-efficient than wrapper classes.

### Expected Follow-up Questions

* Why is `char` 2 bytes?
* Why is `boolean` size JVM dependent?

### Common Mistakes

* Saying `boolean` is always 1 byte.
* Confusing primitive types with wrapper classes.

### Interview Keywords

* Primitive Types
* UTF-16
* Value Type
* Memory Efficient

---

# Q6. Difference between primitive types and wrapper classes.

### Answer

Primitive types store actual values, while wrapper classes are objects that encapsulate those primitive values.

| Primitive | Wrapper |
| --------- | ------- |
| int       | Integer |
| long      | Long    |
| double    | Double  |
| boolean   | Boolean |

Primitives:

* Faster
* Less memory
* Cannot be `null`
* No utility methods

Wrappers:

* Can be `null`
* Required when working with Collections and Generics
* Provide utility methods like `parseInt()` and `valueOf()`

In Spring Boot applications, wrapper classes are commonly used in DTOs, entities, and request/response models because they support `null`, which helps distinguish between "not provided" and default values.

### Expected Follow-up Questions

* Why do wrapper classes exist?
* Where have you used wrappers in Spring Boot?

### Common Mistakes

* Using wrappers unnecessarily in performance-critical code.
* Forgetting wrappers can be `null`.

### Interview Keywords

* Primitive
* Wrapper
* Generics
* Collections
* Nullable

---

# Q7. What is autoboxing and unboxing?

### Answer

Autoboxing is the automatic conversion of a primitive type into its corresponding wrapper class. Unboxing is the reverse conversion.

Example:

```java
Integer num = 10;   // Autoboxing
int value = num;    // Unboxing
```

This feature makes code cleaner, especially when working with Collections and Generics.

One important consideration is performance. Autoboxing creates objects, so repeated boxing and unboxing inside loops or performance-critical code can increase memory allocations and CPU overhead.

Also, unboxing a `null` wrapper throws a `NullPointerException`.

```java
Integer num = null;
int value = num; // NullPointerException
```

### Expected Follow-up Questions

* Does autoboxing affect performance?
* Can unboxing cause `NullPointerException`?

### Common Mistakes

* Ignoring object creation overhead.
* Forgetting `null` during unboxing.

### Interview Keywords

* Autoboxing
* Unboxing
* Integer
* NullPointerException
* Performance

---

# Q8. Difference between `==` and `equals()`.

### Answer

`==` compares references for objects, whereas `equals()` compares logical equality if the class overrides it.

For primitives:

* `==` compares actual values.

For objects:

* `==` checks whether both references point to the same object.
* `equals()` checks whether two objects should be considered logically equal.

Example:

```java
String a = new String("Java");
String b = new String("Java");

a == b         // false
a.equals(b)    // true
```

Classes like `String`, `Integer`, and many domain classes override `equals()` to compare content rather than object identity.

### Expected Follow-up Questions

* Why does `String` override `equals()`?
* When is `==` the correct choice?
* How does `equals()` relate to `hashCode()`?

### Common Mistakes

* Using `==` for String comparison.
* Overriding `equals()` without `hashCode()`.

### Interview Keywords

* Reference Equality
* Logical Equality
* equals()
* hashCode()

---

# Q9. Difference between `String`, `StringBuilder` and `StringBuffer`.

### Answer

The main difference is mutability and thread safety.

| Class         | Mutable | Thread Safe     |
| ------------- | ------- | --------------- |
| String        | No      | Yes (Immutable) |
| StringBuilder | Yes     | No              |
| StringBuffer  | Yes     | Yes             |

* `String` is immutable, so every modification creates a new object.
* `StringBuilder` is mutable and is the preferred choice for string manipulation in single-threaded code.
* `StringBuffer` is mutable but synchronizes its methods, making it thread-safe with additional overhead.

In backend applications, `StringBuilder` is the most common choice when constructing large strings efficiently.

### Expected Follow-up Questions

* Why is `String` immutable?
* Which one is faster?
* Which one is thread-safe?

### Common Mistakes

* Using `String` repeatedly inside loops.
* Choosing `StringBuffer` when synchronization isn't needed.

### Interview Keywords

* Immutable
* Mutable
* Synchronization
* Thread Safety
* Performance

---

# Q10. What is String Pool?

### Answer

The String Pool is a special area managed by the JVM that stores string literals. If the same literal is used multiple times, all references point to the same object instead of creating duplicate instances.

Example:

```java
String a = "Java";
String b = "Java";

a == b   // true
```

Only one `"Java"` object exists in the pool.

However:

```java
String s = new String("Java");
```

This creates a new `String` object on the heap, even if `"Java"` already exists in the pool.

Using the `intern()` method returns the pooled instance if one exists.

The String Pool improves memory usage by avoiding duplicate string literals.

### Expected Follow-up Questions

* Where is the String Pool stored?
* What happens with `new String("abc")`?
* What does `intern()` do?

### Common Mistakes

* Assuming every `String` is stored in the pool.
* Believing `new String()` reuses the pooled object.

### Interview Keywords

* String Pool
* Heap
* String Literal
* intern()
* Memory Optimization

# Q11. Why is String immutable?

### Answer

`String` is immutable because it improves security, performance, thread safety, and enables JVM optimizations like the String Pool.

Once a `String` object is created, its value cannot be changed. Any modification creates a new `String` object.

The key benefits are:

* **Security:** Strings are widely used for file paths, URLs, database connections, and class loading. If they were mutable, one part of the code could change their value unexpectedly.
* **String Pool:** Since strings cannot change, multiple references can safely share the same object, reducing memory usage.
* **Hashing:** A `String`'s hash code is cached after the first computation. Since the value never changes, the cached hash remains valid, making lookups in `HashMap` and `HashSet` faster.
* **Thread Safety:** Immutable objects can be shared across threads without synchronization.

### Expected Follow-up Questions

* What are the security implications?
* Why does immutability help HashMap?
* How does it improve thread safety?

### Common Mistakes

* Saying immutability is only for thread safety.
* Forgetting its role in the String Pool and hash code caching.

### Interview Keywords

* Immutability
* String Pool
* Cached HashCode
* Thread Safety
* Security

---

# Q12. Explain Object class.

### Answer

`Object` is the root class of the Java class hierarchy. Every Java class directly or indirectly inherits from it.

It provides common methods that are available to all objects, such as:

* `equals()`
* `hashCode()`
* `toString()`
* `clone()`
* `getClass()`
* `wait()`
* `notify()`
* `notifyAll()`

In practice, the most commonly overridden methods are:

* `equals()`
* `hashCode()`
* `toString()`

For example:

* `equals()` defines logical equality.
* `hashCode()` is required for hash-based collections.
* `toString()` improves logging and debugging.

### Expected Follow-up Questions

* Which methods are inherited from Object?
* Which methods are commonly overridden?
* Why is Object the root class?

### Common Mistakes

* Saying every method in `Object` should be overridden.
* Forgetting synchronization methods like `wait()` and `notify()`.

### Interview Keywords

* Root Class
* equals()
* hashCode()
* toString()
* getClass()

---

# Q13. Explain `hashCode()` and `equals()` contract.

### Answer

The `equals()` and `hashCode()` contract ensures that hash-based collections work correctly.

The most important rule is:

> If two objects are equal according to `equals()`, they **must** return the same `hashCode()`.

The reverse is not mandatory. Two different objects can have the same hash code due to collisions.

Collections like `HashMap` and `HashSet` first use `hashCode()` to find the bucket and then use `equals()` to identify the exact object.

If this contract is broken:

* Duplicate objects may appear in a `HashSet`.
* `HashMap` lookups may fail even when logically equal keys exist.

### Expected Follow-up Questions

* What happens if the contract is violated?
* Why does HashMap use both methods?
* Can two unequal objects have the same hash code?

### Common Mistakes

* Overriding `equals()` without overriding `hashCode()`.
* Assuming unique hash codes are guaranteed.

### Interview Keywords

* equals()
* hashCode()
* HashMap
* HashSet
* Contract

---

# Q14. Difference between `final`, `finally`, and `finalize()`.

### Answer

Although their names are similar, they serve completely different purposes.

* **`final`** is a keyword used to prevent modification.

  * Final variable → cannot be reassigned.
  * Final method → cannot be overridden.
  * Final class → cannot be inherited.

* **`finally`** is a block associated with `try-catch` that executes whether an exception occurs or not. It is typically used for resource cleanup.

* **`finalize()`** was a method called by the Garbage Collector before reclaiming an object. It has been **deprecated** because its execution is unpredictable and it can negatively impact performance.

Today, resource cleanup should be handled using **try-with-resources** instead of `finalize()`.

### Expected Follow-up Questions

* Why is `finalize()` deprecated?
* What should replace `finalize()`?
* When is `finally` not executed?

### Common Mistakes

* Confusing `finally` with `finalize()`.
* Saying `finalize()` is guaranteed to execute.

### Interview Keywords

* final
* finally
* finalize()
* try-with-resources
* Garbage Collection

---

# Q15. What are access modifiers?

### Answer

Access modifiers control the visibility of classes, methods, and fields.

There are four access levels:

| Modifier            | Same Class | Same Package | Subclass | Other Package |
| ------------------- | ---------- | ------------ | -------- | ------------- |
| `private`           | ✅          | ❌            | ❌        | ❌             |
| *(package-private)* | ✅          | ✅            | ❌        | ❌             |
| `protected`         | ✅          | ✅            | ✅*       | ❌             |
| `public`            | ✅          | ✅            | ✅        | ✅             |

* **private** → accessible only within the same class.
* **package-private** (no modifier) → accessible within the same package.
* **protected** → accessible within the same package and by subclasses in other packages.
* **public** → accessible everywhere.

In production code, fields are usually kept `private` to maintain encapsulation.

### Expected Follow-up Questions

* What is package-private?
* How does `protected` behave across packages?

### Common Mistakes

* Assuming `protected` means "public to all subclasses and packages."
* Making fields public unnecessarily.

### Interview Keywords

* Encapsulation
* Visibility
* Package-private
* protected
* public

---

# Q16. Difference between abstract class and interface.

### Answer

An **abstract class** is used when multiple related classes share common state or implementation. An **interface** is used to define a contract that unrelated classes can implement.

| Abstract Class                     | Interface                              |
| ---------------------------------- | -------------------------------------- |
| Can have instance variables        | Cannot have instance state             |
| Can have constructors              | Cannot have constructors               |
| Single inheritance                 | Multiple interfaces can be implemented |
| Can provide partial implementation | Defines behavior contract              |

Since Java 8, interfaces can also have:

* `default` methods
* `static` methods

Since Java 9, interfaces can additionally have:

* `private` helper methods

In most cases, I prefer **interfaces** for defining contracts and **abstract classes** only when shared implementation or state is required.

### Expected Follow-up Questions

* What changed in Java 8?
* What changed in Java 9?
* Which one should you prefer?

### Common Mistakes

* Saying interfaces cannot have method implementations.
* Using inheritance when an interface is sufficient.

### Interview Keywords

* Contract
* Abstract Class
* Interface
* Default Methods
* Multiple Inheritance

---

# Q17. Can an interface have constructors?

### Answer

No. An interface cannot have constructors.

A constructor initializes an object's state, but interfaces cannot be instantiated and do not maintain instance state.

Objects are created through implementing classes, so constructors belong to those classes.

### Expected Follow-up Questions

* Why can't interfaces be instantiated?
* Can interfaces have fields?
* Can interfaces have static methods?

### Common Mistakes

* Assuming default methods require constructors.
* Confusing interfaces with abstract classes.

### Interview Keywords

* Constructor
* Interface
* Instantiation
* Contract

---

# Q18. Can an abstract class have constructors?

### Answer

Yes. An abstract class can have constructors.

Although an abstract class cannot be instantiated directly, its constructor is executed whenever a subclass object is created.

The constructor is typically used to initialize common fields shared by all subclasses.

```java
abstract class Animal {
    Animal() {
        System.out.println("Animal constructor");
    }
}
```

When a subclass object is created, the parent constructor runs first.

### Expected Follow-up Questions

* Why does an abstract class need a constructor?
* In what order are constructors executed?
* Can an abstract constructor be declared?

### Common Mistakes

* Saying abstract classes cannot have constructors.
* Forgetting that the parent constructor always executes first.

### Interview Keywords

* Constructor Chaining
* Parent Constructor
* Initialization
* Abstract Class

---

# Q19. What is polymorphism?

### Answer

Polymorphism means the same interface or method call can exhibit different behavior depending on the actual object at runtime.

For example:

```java
Animal animal = new Dog();
animal.sound();
```

Although the reference type is `Animal`, the `Dog` implementation of `sound()` is executed.

This allows code to depend on abstractions rather than concrete implementations, making systems easier to extend and maintain.

Polymorphism is heavily used in frameworks like Spring, where interfaces are injected and different implementations can be swapped without changing client code.

### Expected Follow-up Questions

* What is runtime polymorphism?
* How does JVM choose the method?
* What is dynamic dispatch?

### Common Mistakes

* Confusing polymorphism with inheritance.
* Saying only inheritance provides polymorphism.

### Interview Keywords

* Runtime Polymorphism
* Dynamic Dispatch
* Method Overriding
* Abstraction

---

# Q20. Compile-time vs Runtime polymorphism.

### Answer

The difference lies in **when the method to execute is determined**.

**Compile-time polymorphism** is achieved through **method overloading**. The compiler decides which method to call based on the method signature.

```java
calculate(int a)
calculate(double a)
```

**Runtime polymorphism** is achieved through **method overriding**. The JVM determines the actual method based on the object's runtime type.

```java
Animal animal = new Dog();
animal.sound();
```

In enterprise applications, runtime polymorphism is used much more frequently because it enables extensible designs through interfaces and inheritance.

### Expected Follow-up Questions

* What is method overloading?
* What is method overriding?
* How does JVM implement runtime polymorphism?

### Common Mistakes

* Calling overloading runtime polymorphism.
* Confusing reference type with object type.

### Interview Keywords

* Method Overloading
* Method Overriding
* Early Binding
* Late Binding
* Dynamic Dispatch

# Q21. Method overloading vs overriding.

### Answer

Method **overloading** means multiple methods have the same name but different parameter lists within the same class. Method **overriding** means a subclass provides its own implementation of a method already defined in the parent class.

| Method Overloading                                   | Method Overriding                        |
| ---------------------------------------------------- | ---------------------------------------- |
| Same method name, different parameters               | Same method signature                    |
| Happens in the same class (or inheritance hierarchy) | Happens between parent and child classes |
| Compile-time polymorphism                            | Runtime polymorphism                     |
| Return type alone cannot differentiate methods       | Covariant return types are allowed       |

**Example of overloading:**

```java
class Calculator {
    int add(int a, int b) { return a + b; }
    double add(double a, double b) { return a + b; }
}
```

**Example of overriding:**

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Bark");
    }
}
```

In production, **overriding** is much more common because it enables runtime polymorphism, which frameworks like Spring heavily rely on.

### Expected Follow-up Questions

* Can methods be overloaded by changing only the return type?
* What are the rules for overriding?
* Which one provides runtime polymorphism?

### Common Mistakes

* Saying overloading depends on return type.
* Confusing overloading with overriding.

### Interview Keywords

* Method Overloading
* Method Overriding
* Compile-time Polymorphism
* Runtime Polymorphism
* `@Override`

---

# Q22. Rules of overriding.

### Answer

For a method to be overridden correctly, it must satisfy these rules:

* The method name must be the same.
* The parameter list must be identical.
* The return type must be the same or covariant.
* The overriding method cannot reduce visibility.
* It cannot throw broader checked exceptions than the parent method.
* Static, private, and final methods cannot be overridden.

Using the `@Override` annotation is a best practice because the compiler verifies that the method is actually overriding a parent method.

### Expected Follow-up Questions

* What is a covariant return type?
* Can visibility be increased?
* What happens if the parameter list changes?

### Common Mistakes

* Changing parameters and calling it overriding.
* Reducing access from `public` to `protected`.

### Interview Keywords

* `@Override`
* Covariant Return Type
* Method Signature
* Visibility
* Checked Exceptions

---

# Q23. Can static methods be overridden?

### Answer

No. Static methods cannot be overridden because they belong to the class, not to an object.

If a subclass declares a static method with the same signature, it is **method hiding**, not overriding.

```java
class Parent {
    static void display() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    static void display() {
        System.out.println("Child");
    }
}
```

The method called depends on the **reference type**, not the runtime object.

```java
Parent obj = new Child();
obj.display();   // Parent
```

Since static methods are resolved at compile time, runtime polymorphism does not apply.

### Expected Follow-up Questions

* What is method hiding?
* Why aren't static methods polymorphic?
* Can static methods be overloaded?

### Common Mistakes

* Saying static methods support runtime polymorphism.
* Confusing hiding with overriding.

### Interview Keywords

* Static Method
* Method Hiding
* Compile-time Binding
* Class Method

---

# Q24. Can private methods be overridden?

### Answer

No. Private methods cannot be overridden because they are not inherited by subclasses.

If a subclass declares a private method with the same name and signature, it is an entirely new method.

```java
class Parent {
    private void display() {}
}

class Child extends Parent {
    private void display() {}
}
```

These two methods are unrelated because the child class has no access to the parent's private method.

### Expected Follow-up Questions

* Why aren't private methods inherited?
* Can private methods be overloaded?
* What if the child declares the method as public?

### Common Mistakes

* Assuming matching signatures imply overriding.
* Forgetting that private members are inaccessible outside their class.

### Interview Keywords

* Private Method
* Inheritance
* Access Control
* Method Visibility

---

# Q25. Can constructors be overridden?

### Answer

No. Constructors cannot be overridden because they are not inherited.

A constructor is responsible for initializing a new object of its own class. Since subclasses do not inherit constructors, there is nothing to override.

When creating a subclass object, the parent constructor is invoked using `super()`, but it is **called**, not overridden.

### Expected Follow-up Questions

* Why aren't constructors inherited?
* Can constructors be overloaded?
* How does constructor chaining work?

### Common Mistakes

* Saying constructors participate in polymorphism.
* Confusing constructor chaining with overriding.

### Interview Keywords

* Constructor
* Constructor Chaining
* `super()`
* Object Initialization

---

# Q26. What is inheritance?

### Answer

Inheritance allows one class to acquire the properties and behavior of another class using the `extends` keyword.

It promotes code reuse and enables runtime polymorphism.

```java
class Animal {
    void eat() {}
}

class Dog extends Animal {
    void bark() {}
}
```

Here, `Dog` inherits the `eat()` method from `Animal` and adds its own behavior.

In production code, inheritance should be used only when there is a clear **IS-A** relationship. Otherwise, composition is generally preferred because it reduces coupling.

### Expected Follow-up Questions

* What is the IS-A relationship?
* Why is composition often preferred?
* What types of inheritance does Java support?

### Common Mistakes

* Using inheritance only for code reuse.
* Creating deep inheritance hierarchies.

### Interview Keywords

* Inheritance
* IS-A Relationship
* Code Reuse
* Polymorphism

---

# Q27. Multiple inheritance in Java?

### Answer

Java does **not** support multiple inheritance for classes, but it does support multiple inheritance through interfaces.

The main reason is to avoid the **Diamond Problem**, where a class inherits the same method from multiple parent classes, leading to ambiguity.

```java
interface A {
    void display();
}

interface B {
    void display();
}

class C implements A, B {
    @Override
    public void display() {
        System.out.println("Resolved");
    }
}
```

If multiple interfaces provide conflicting default methods, the implementing class must explicitly override the method to resolve the conflict.

### Expected Follow-up Questions

* What is the Diamond Problem?
* How do default methods create conflicts?
* Why are interfaces allowed?

### Common Mistakes

* Saying Java completely disallows multiple inheritance.
* Forgetting that interfaces support it.

### Interview Keywords

* Multiple Inheritance
* Interface
* Diamond Problem
* Default Methods

---

# Q28. What is encapsulation?

### Answer

Encapsulation is the practice of bundling data and the methods that operate on it within a class while restricting direct access to the internal state.

Typically, fields are declared `private`, and controlled access is provided through methods.

```java
class Account {
    private double balance;

    public void deposit(double amount) {
        balance += amount;
    }

    public double getBalance() {
        return balance;
    }
}
```

This protects the object's state and allows validation, business rules, or logging to be added without affecting callers.

In production systems, encapsulation improves maintainability and prevents accidental misuse of domain objects.

### Expected Follow-up Questions

* Why keep fields private?
* How is encapsulation different from abstraction?
* Can encapsulation be broken?

### Common Mistakes

* Making fields public with no validation.
* Confusing encapsulation with abstraction.

### Interview Keywords

* Encapsulation
* Data Hiding
* Access Modifiers
* Information Hiding

---

# Q29. What is abstraction?

### Answer

Abstraction means exposing only the essential behavior while hiding implementation details.

In Java, abstraction is achieved using **interfaces** and **abstract classes**.

For example, a service may expose a `PaymentService` interface, while different implementations handle payment through different providers. The caller only depends on the contract, not the implementation.

Abstraction reduces coupling and makes code easier to extend and test.

### Expected Follow-up Questions

* How is abstraction different from encapsulation?
* Which should you use: interface or abstract class?
* How does Spring use abstraction?

### Common Mistakes

* Treating abstraction and encapsulation as the same concept.
* Exposing implementation details through the API.

### Interview Keywords

* Abstraction
* Interface
* Abstract Class
* Loose Coupling
* Contract

---

# Q30. Composition vs Inheritance.

### Answer

**Composition** means building a class using other objects (**HAS-A** relationship), while **inheritance** extends an existing class (**IS-A** relationship).

```java
// Composition
class Car {
    private Engine engine;
}
```

```java
// Inheritance
class Dog extends Animal {
}
```

In most enterprise applications, I prefer **composition** because it provides:

* Lower coupling
* Better flexibility
* Easier testing
* Easier maintenance
* Ability to change behavior without changing the class hierarchy

Inheritance is appropriate only when there is a genuine IS-A relationship and shared behavior naturally belongs in the parent class.

A good example is that Spring itself favors composition through dependency injection rather than deep inheritance hierarchies.

### Expected Follow-up Questions

* Why is composition preferred?
* What problems can deep inheritance create?
* What are IS-A and HAS-A relationships?

### Common Mistakes

* Using inheritance only to reuse code.
* Creating deep inheritance hierarchies that are difficult to maintain.

### Interview Keywords

* Composition
* Inheritance
* HAS-A
* IS-A
* Loose Coupling
* Dependency Injection

# Q31. When should you use composition over inheritance?

### Answer

Use **composition** when classes have a **HAS-A** relationship or when you want flexibility without tightly coupling classes.

Composition allows a class to reuse functionality by containing another object instead of extending it.

```java
class Car {
    private Engine engine;
}
```

I generally prefer composition because it:

* Reduces coupling.
* Makes classes easier to test and maintain.
* Allows implementations to be swapped without changing the class hierarchy.
* Avoids problems caused by deep inheritance.

Inheritance should only be used when there is a true **IS-A** relationship and the child naturally extends the parent's behavior.

In enterprise applications, frameworks like Spring heavily encourage composition through dependency injection.

### Expected Follow-up Questions

* Why is composition preferred?
* What are the drawbacks of inheritance?
* What is the HAS-A relationship?

### Common Mistakes

* Using inheritance only for code reuse.
* Creating inheritance hierarchies just to share utility methods.

### Interview Keywords

* Composition
* HAS-A
* Loose Coupling
* Dependency Injection
* Code Reuse

---

# Q32. What problems does inheritance create?

### Answer

Inheritance can introduce **tight coupling** between parent and child classes. Changes in the parent may unintentionally affect all subclasses.

Common problems include:

* Tight coupling between classes.
* Fragile base class problem.
* Deep inheritance hierarchies become difficult to understand.
* Reduced flexibility because behavior is fixed by the hierarchy.
* Harder unit testing due to inherited behavior.
* Violation of the **Liskov Substitution Principle (LSP)** if subclasses don't behave as expected.

In production systems, deep inheritance often increases maintenance cost, which is why composition is usually preferred.

### Expected Follow-up Questions

* What is the Fragile Base Class problem?
* How does inheritance violate LSP?
* Why does Spring prefer composition?

### Common Mistakes

* Using inheritance for every code reuse scenario.
* Creating long inheritance chains.

### Interview Keywords

* Tight Coupling
* Fragile Base Class
* LSP
* Composition
* Maintainability

---

# Q33. How do SOLID principles influence Java class design?

### Answer

SOLID principles help design classes that are easier to maintain, test, and extend.

Briefly:

* **S — Single Responsibility Principle (SRP):** A class should have one reason to change.
* **O — Open/Closed Principle (OCP):** Open for extension, closed for modification.
* **L — Liskov Substitution Principle (LSP):** Subclasses should be replaceable with their parent.
* **I — Interface Segregation Principle (ISP):** Prefer small, focused interfaces over large ones.
* **D — Dependency Inversion Principle (DIP):** Depend on abstractions instead of concrete implementations.

In Spring Boot applications, dependency injection naturally supports DIP by injecting interfaces instead of concrete classes.

### Expected Follow-up Questions

* Which SOLID principle do you use most?
* How does Spring support DIP?
* Give an example of SRP.

### Common Mistakes

* Memorizing SOLID without understanding practical usage.
* Treating every class as an interface unnecessarily.

### Interview Keywords

* SOLID
* SRP
* DIP
* OCP
* LSP

---

# Q34. Difference between IS-A and HAS-A relationship.

### Answer

An **IS-A** relationship represents inheritance, while a **HAS-A** relationship represents composition.

**IS-A (Inheritance):**

```java
class Dog extends Animal {}
```

A Dog **is an** Animal.

**HAS-A (Composition):**

```java
class Car {
    private Engine engine;
}
```

A Car **has an** Engine.

As a design guideline:

* Use **IS-A** only when inheritance is semantically correct.
* Use **HAS-A** when building objects from reusable components.

In most production systems, HAS-A is preferred because it provides greater flexibility.

### Expected Follow-up Questions

* Why is HAS-A preferred?
* Can HAS-A replace inheritance?
* Give a real-world example.

### Common Mistakes

* Confusing code reuse with inheritance.
* Treating every relationship as IS-A.

### Interview Keywords

* IS-A
* HAS-A
* Composition
* Inheritance
* Object Modeling

---

# Q35. Can you break encapsulation accidentally?

### Answer

Yes. Encapsulation can be broken even if fields are declared `private`.

Some common ways are:

* Returning mutable internal objects directly.
* Exposing mutable collections.
* Making fields `public`.
* Providing setters that bypass validation.
* Using reflection improperly.

Example:

```java
class Student {
    private List<String> subjects;

    public List<String> getSubjects() {
        return subjects;
    }
}
```

The caller can modify the internal list directly, violating encapsulation.

A better approach is to return an unmodifiable view or a defensive copy.

### Expected Follow-up Questions

* How do you protect mutable collections?
* What is defensive copying?
* Can reflection break encapsulation?

### Common Mistakes

* Returning internal collections directly.
* Exposing mutable state through getters.

### Interview Keywords

* Encapsulation
* Mutable Objects
* Defensive Copy
* Unmodifiable Collection

---

# Q36. Why should mutable fields be private?

### Answer

Mutable fields should be `private` so that only the class controls how they are modified.

This helps:

* Maintain object consistency.
* Enforce validation rules.
* Prevent invalid states.
* Protect against accidental modifications.
* Make debugging easier.

Instead of exposing mutable fields directly, modifications should happen through well-defined methods.

This follows the principle of encapsulation and keeps business rules centralized.

### Expected Follow-up Questions

* Why not make fields public?
* How do setters help?
* How does this improve maintainability?

### Common Mistakes

* Declaring mutable fields as public.
* Allowing unrestricted modification.

### Interview Keywords

* Encapsulation
* Data Hiding
* Mutable State
* Validation

---

# Q37. How do immutable classes improve concurrency?

### Answer

Immutable classes are inherently thread-safe because their state cannot change after creation.

Since no thread can modify the object's state:

* No synchronization is required.
* There are no race conditions on the object's fields.
* Multiple threads can safely share the same instance.

This reduces complexity and improves reliability in concurrent applications.

Examples include `String`, `Integer`, and `LocalDate`.

### Expected Follow-up Questions

* Why don't immutable objects need synchronization?
* Are immutable objects always thread-safe?
* What are some immutable classes in Java?

### Common Mistakes

* Assuming immutable objects eliminate all concurrency issues.
* Forgetting that referenced mutable objects can still cause problems.

### Interview Keywords

* Immutability
* Thread Safety
* Race Condition
* Synchronization

---

# Q38. How would you create your own immutable class?

### Answer

To create an immutable class:

1. Declare the class as `final`.
2. Make all fields `private` and `final`.
3. Initialize fields through the constructor.
4. Do not provide setters.
5. Return defensive copies for mutable objects.
6. Store defensive copies of mutable constructor arguments.

Example:

```java
final class Employee {

    private final String name;
    private final List<String> skills;

    Employee(String name, List<String> skills) {
        this.name = name;
        this.skills = List.copyOf(skills);
    }

    public String getName() {
        return name;
    }

    public List<String> getSkills() {
        return List.copyOf(skills);
    }
}
```

This prevents external code from modifying the object's internal state.

### Expected Follow-up Questions

* Why should the class be final?
* Why use defensive copying?
* What if a field is mutable?

### Common Mistakes

* Forgetting defensive copies.
* Returning mutable references directly.

### Interview Keywords

* Immutable Class
* final
* Defensive Copy
* Encapsulation

---

# Q39. What should be final in an immutable class?

### Answer

In an immutable class:

* The **class** should usually be `final` to prevent subclasses from introducing mutability.
* All **instance fields** should be `private` and `final`.
* References to mutable objects should also be `final`, although the referenced object still needs defensive copying.

Making fields `final` ensures they are assigned only once during construction.

### Expected Follow-up Questions

* Why make the class final?
* Is making fields final enough?
* What if a field references a mutable object?

### Common Mistakes

* Thinking `final` makes mutable objects immutable.
* Forgetting to make fields private.

### Interview Keywords

* final
* Immutable Class
* Encapsulation
* Defensive Copy

---

# Q40. Why should defensive copying be used?

### Answer

Defensive copying protects an object's internal state from being modified by external code.

Without defensive copying, callers can change mutable objects after passing them to a constructor or after receiving them from a getter.

Example:

```java
class Employee {

    private final List<String> skills;

    Employee(List<String> skills) {
        this.skills = List.copyOf(skills);
    }

    public List<String> getSkills() {
        return List.copyOf(skills);
    }
}
```

Here:

* The constructor copies the incoming list instead of storing the caller's reference.
* The getter returns a new copy instead of exposing the internal list.

This is essential when designing immutable classes or protecting encapsulated mutable state.

### Expected Follow-up Questions

* When should defensive copying be used?
* Why isn't `final` enough?
* What's the difference between `Collections.unmodifiableList()` and `List.copyOf()`?

### Common Mistakes

* Returning internal mutable collections directly.
* Assuming `final` prevents object mutation.

### Interview Keywords

* Defensive Copy
* Immutability
* Encapsulation
* Mutable Objects
* `List.copyOf()`

# Q41. Where are objects created?

### Answer

Objects are created in the **Heap Memory**.

Whenever we use the `new` keyword, the JVM allocates memory for the object on the heap and returns a reference to it.

```java
Employee emp = new Employee();
```

Here:

* The `Employee` object is created on the **heap**.
* The reference variable `emp` is stored in the **stack** (if it's a local variable).

The heap is shared among all threads, which is why objects can be accessed by multiple threads if their references are shared.

### Expected Follow-up Questions

* Where are object references stored?
* Why are objects stored in the heap?
* Who manages heap memory?

### Common Mistakes

* Saying objects are stored on the stack.
* Confusing object references with objects themselves.

### Interview Keywords

* Heap Memory
* Object Allocation
* `new`
* Reference Variable
* Garbage Collection

---

# Q42. Where are local variables stored?

### Answer

Local variables are stored in the **stack memory** inside the current method's stack frame.

```java
public void process() {
    int count = 10;
    Employee emp = new Employee();
}
```

Here:

* `count` is stored directly in the stack.
* `emp` (the reference) is stored in the stack.
* The actual `Employee` object is stored in the heap.

When the method completes, its stack frame is removed automatically, and all local variables are destroyed.

### Expected Follow-up Questions

* What happens to local variables after method execution?
* Where are instance variables stored?
* Can local variables be shared across threads?

### Common Mistakes

* Saying local objects are stored on the stack.
* Forgetting that only the reference is on the stack.

### Interview Keywords

* Stack Frame
* Local Variable
* Reference
* Method Call

---

# Q43. What is stack memory?

### Answer

Stack memory stores **method execution data**, such as local variables, method parameters, and references to heap objects.

Each thread has its own stack, and every method call creates a new **stack frame**.

A stack frame typically contains:

* Local variables
* Method parameters
* Operand stack
* Return information

Stack memory is:

* Fast to allocate and deallocate.
* Automatically managed by the JVM.
* Thread-specific.

If too many stack frames are created, for example due to deep or infinite recursion, a `StackOverflowError` occurs.

### Expected Follow-up Questions

* What is a stack frame?
* Is stack memory shared?
* What causes `StackOverflowError`?

### Common Mistakes

* Saying objects are stored in the stack.
* Confusing stack memory with heap memory.

### Interview Keywords

* Stack Memory
* Stack Frame
* Method Call
* Thread Stack
* StackOverflowError

---

# Q44. What is heap memory?

### Answer

Heap memory is the runtime memory area where Java objects and arrays are allocated.

All threads share the heap, making it suitable for storing objects that may be accessed across different parts of the application.

The JVM manages heap memory automatically using the **Garbage Collector**, which reclaims memory occupied by objects that are no longer reachable.

Because object allocation and garbage collection are more expensive than stack operations, excessive object creation can impact application performance.

### Expected Follow-up Questions

* Who manages heap memory?
* Is heap shared across threads?
* What causes `OutOfMemoryError`?

### Common Mistakes

* Saying heap memory is thread-local.
* Assuming garbage collection happens immediately after an object becomes unreachable.

### Interview Keywords

* Heap Memory
* Garbage Collection
* Object Allocation
* Shared Memory

---

# Q45. Difference between stack and heap.

### Answer

The main difference is what they store and how they are managed.

| Stack                                         | Heap                            |
| --------------------------------------------- | ------------------------------- |
| Stores method frames and local variables      | Stores objects and arrays       |
| Thread-specific                               | Shared across threads           |
| Automatically released after method execution | Managed by Garbage Collector    |
| Very fast allocation                          | Comparatively slower allocation |
| Limited size                                  | Usually much larger             |

Example:

```java
Employee emp = new Employee();
```

* `emp` (reference) → Stack
* `Employee` object → Heap

Understanding this distinction is useful for debugging memory-related issues like `StackOverflowError` and `OutOfMemoryError`.

### Expected Follow-up Questions

* Which memory is faster?
* Why is heap shared?
* What is stored in each?

### Common Mistakes

* Saying primitives are always stored on the stack (instance primitives are part of heap objects).
* Confusing references with objects.

### Interview Keywords

* Stack
* Heap
* Stack Frame
* Garbage Collection
* Memory Model

---

# Q46. What causes `StackOverflowError`?

### Answer

`StackOverflowError` occurs when the JVM runs out of stack space due to too many stack frames.

The most common reason is **infinite or very deep recursion**.

Example:

```java
void recurse() {
    recurse();
}
```

Each recursive call creates a new stack frame. Eventually, the thread's stack limit is reached, and the JVM throws `StackOverflowError`.

Although recursion is the most common cause, extremely deep method call chains can also lead to this error.

### Expected Follow-up Questions

* Why doesn't the Garbage Collector fix this?
* How is it different from `OutOfMemoryError`?
* Can increasing stack size solve it?

### Common Mistakes

* Confusing it with heap exhaustion.
* Thinking it's related to object allocation.

### Interview Keywords

* StackOverflowError
* Recursion
* Stack Frame
* JVM Stack

---

# Q47. What causes `OutOfMemoryError`?

### Answer

`OutOfMemoryError` occurs when the JVM cannot allocate more memory even after attempting garbage collection.

Common causes include:

* Memory leaks due to lingering references.
* Creating too many large objects.
* Holding large collections in memory.
* Insufficient heap size.
* Excessive object creation.

Example:

```java
List<byte[]> data = new ArrayList<>();

while (true) {
    data.add(new byte[1024 * 1024]);
}
```

This continuously allocates memory without releasing references, eventually exhausting the heap.

In production, the first step is usually to analyze a **heap dump** to identify which objects are consuming memory and why they remain reachable.

### Expected Follow-up Questions

* What is a memory leak in Java?
* How do you investigate `OutOfMemoryError`?
* Can garbage collection prevent it?

### Common Mistakes

* Assuming Java cannot have memory leaks.
* Confusing `OutOfMemoryError` with `StackOverflowError`.

### Interview Keywords

* OutOfMemoryError
* Heap Dump
* Memory Leak
* Garbage Collection
* Heap Analysis

---

# Q48. Difference between reference variable and object.

### Answer

A **reference variable** stores the address-like reference to an object, while the **object** contains the actual data and behavior.

Example:

```java
Employee emp = new Employee();
```

* `emp` is the reference variable.
* `new Employee()` creates the actual object.

Multiple reference variables can point to the same object.

```java
Employee e1 = new Employee();
Employee e2 = e1;
```

Here, `e1` and `e2` refer to the same object in the heap.

This distinction is important because assigning one reference to another does **not** create a copy of the object.

### Expected Follow-up Questions

* Can multiple references point to one object?
* Can an object exist without a reference?
* What happens during assignment?

### Common Mistakes

* Assuming assignment copies the object.
* Confusing references with pointers.

### Interview Keywords

* Reference Variable
* Object
* Heap
* Assignment
* Shared Reference

---

# Q49. What happens during object creation?

### Answer

When an object is created using `new`, the JVM performs several steps in order:

1. Memory is allocated on the heap.
2. All instance fields are assigned default values.
3. The parent class constructor is invoked.
4. Instance field initializers and instance initialization blocks are executed.
5. The constructor body of the current class executes.
6. The reference to the newly created object is returned.

For example:

```java
Employee emp = new Employee();
```

The object is fully initialized before `emp` receives its reference.

Understanding this sequence is useful when debugging constructor behavior and initialization issues.

### Expected Follow-up Questions

* What is the initialization order?
* When are constructors called?
* When are default values assigned?

### Common Mistakes

* Thinking constructors allocate memory.
* Forgetting that parent constructors execute first.

### Interview Keywords

* Object Creation
* Heap Allocation
* Constructor Chaining
* Initialization Order

---

# Q50. What happens if a constructor throws an exception?

### Answer

If a constructor throws an exception, object creation fails and the object is **not** successfully constructed.

Any memory allocated for that partially constructed object becomes eligible for garbage collection because no usable reference is returned.

Example:

```java
class Employee {

    Employee() {
        throw new RuntimeException("Initialization failed");
    }
}

Employee emp = new Employee(); // Exception thrown
```

Here, `emp` is never assigned a valid object because construction did not complete.

In production, constructors should perform only essential initialization. Complex operations like database calls or network requests are usually kept outside constructors to avoid partially initialized objects and make error handling simpler.

### Expected Follow-up Questions

* Does the object get created partially?
* Can the constructor catch its own exception?
* What happens to allocated memory?

### Common Mistakes

* Assuming a partially initialized object is returned.
* Performing heavy business logic inside constructors.

### Interview Keywords

* Constructor Exception
* Object Initialization
* Garbage Collection
* Constructor Chaining


