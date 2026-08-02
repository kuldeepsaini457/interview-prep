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

# Q51. Can object exist without reference?

### Answer

Yes. An object can exist without any reference variable pointing to it.

Such an object becomes **unreachable** and is eligible for **garbage collection**.

Example:

```java
new Employee();
```

Here, an `Employee` object is created, but no reference is stored. Once the statement completes, the object is no longer reachable and can be reclaimed by the Garbage Collector.

Another common case is when all references to an object are removed:

```java
Employee emp = new Employee();
emp = null;
```

If no other references exist, the object becomes eligible for garbage collection.

**Important:** Eligible for garbage collection does **not** mean it is immediately removed. The JVM decides when to reclaim the memory.

### Expected Follow-up Questions

* When does an object become eligible for garbage collection?
* Is garbage collection immediate?
* Can an unreachable object become reachable again?

### Common Mistakes

* Saying the object is deleted immediately.
* Confusing "eligible for GC" with "GC has already run."

### Interview Keywords

* Reachability
* Garbage Collection
* Heap
* Eligible for GC

---

# Q52. Can multiple references point to same object?

### Answer

Yes. Multiple reference variables can point to the same object in memory.

Example:

```java
Employee emp1 = new Employee();
Employee emp2 = emp1;
```

Both `emp1` and `emp2` refer to the same object on the heap.

So, if one reference modifies the object's state, the change is visible through the other reference as well.

```java
emp1.setName("Alice");

System.out.println(emp2.getName()); // Alice
```

This is an important concept because assigning one reference to another does **not** create a copy of the object.

### Expected Follow-up Questions

* Does assignment create a new object?
* How do you create an actual copy?
* What happens if one reference becomes `null`?

### Common Mistakes

* Assuming `emp2 = emp1` creates a copy.
* Forgetting both references share the same object.

### Interview Keywords

* Reference Variable
* Shared Object
* Heap
* Object Identity

---

# Q53. Difference between shallow copy and deep copy.

### Answer

A **shallow copy** copies the object's fields, but nested object references are shared. A **deep copy** creates copies of both the object and all nested mutable objects.

Example:

```java
class Employee {
    Address address;
}
```

**Shallow Copy**

```text
Employee1 ─────► Address
Employee2 ─────┘
```

Both employees share the same `Address`.

**Deep Copy**

```text
Employee1 ─────► Address1
Employee2 ─────► Address2
```

Each employee has its own copy of the `Address`.

Use:

* **Shallow copy** when shared state is acceptable.
* **Deep copy** when complete independence is required.

### Expected Follow-up Questions

* Which copy does `clone()` perform?
* When do you need deep copying?
* What are the performance implications?

### Common Mistakes

* Assuming copying a reference copies the object.
* Forgetting nested mutable objects in deep copies.

### Interview Keywords

* Shallow Copy
* Deep Copy
* Object Graph
* Mutable Objects

---

# Q54. How would you clone an object?

### Answer

In modern Java, I generally avoid using `Cloneable`. Instead, I prefer one of these approaches:

1. **Copy constructor** (most common)
2. **Factory method**
3. **Builder pattern** (for complex objects)

Example using a copy constructor:

```java
class Employee {
    private String name;

    Employee(Employee other) {
        this.name = other.name;
    }
}
```

This approach is:

* Explicit
* Easy to understand
* Easier to maintain
* Doesn't rely on the limitations of `Cloneable`

I would use `clone()` only if I'm working with legacy code.

### Expected Follow-up Questions

* Why is `Cloneable` discouraged?
* What does `super.clone()` do?
* Which approach do you prefer?

### Common Mistakes

* Recommending `Cloneable` for new code.
* Forgetting to copy nested mutable objects.

### Interview Keywords

* Copy Constructor
* Builder Pattern
* Cloneable
* Deep Copy

---

# Q55. Problems with `Cloneable` interface?

### Answer

`Cloneable` has several design issues, which is why it's generally discouraged in modern Java.

Some major problems are:

* It performs a **shallow copy** by default.
* Nested mutable objects are not cloned automatically.
* `clone()` is `protected` in `Object`, making the API awkward.
* It bypasses constructors, so object initialization logic is skipped.
* It requires handling `CloneNotSupportedException`.

Because of these limitations, Java developers typically prefer:

* Copy constructors
* Factory methods
* Builder-based copying

These approaches are clearer and easier to maintain.

### Expected Follow-up Questions

* Why does `clone()` bypass constructors?
* Why is shallow copying dangerous?
* What is the recommended alternative?

### Common Mistakes

* Assuming `clone()` performs deep copying.
* Forgetting that constructors are not invoked.

### Interview Keywords

* Cloneable
* Shallow Copy
* Copy Constructor
* CloneNotSupportedException

---

# Q56. What is `static` keyword?

### Answer

The `static` keyword makes a member belong to the **class** rather than to individual objects.

It can be applied to:

* Variables
* Methods
* Blocks
* Nested classes

Example:

```java
class Employee {
    static String company = "ABC";
}
```

Here, `company` is shared by all `Employee` objects.

Static members are created when the class is loaded and exist only once per class loader.

They are commonly used for:

* Constants
* Utility methods
* Shared configuration
* Factory methods

### Expected Follow-up Questions

* When are static members created?
* Where are static variables stored?
* Can static methods be overridden?

### Common Mistakes

* Thinking each object has its own copy of static variables.
* Accessing static members through object references.

### Interview Keywords

* Class Member
* Static Variable
* Static Method
* Class Loading

---

# Q57. Static variable vs instance variable.

### Answer

A **static variable** belongs to the class, while an **instance variable** belongs to each object.

| Static Variable              | Instance Variable                |
| ---------------------------- | -------------------------------- |
| One copy per class           | One copy per object              |
| Shared across objects        | Unique for every object          |
| Created during class loading | Created during object creation   |
| Accessed using class name    | Accessed through object instance |

Example:

```java
class Employee {
    static String company = "ABC";
    String name;
}
```

Every employee shares the same `company`, but each employee has its own `name`.

### Expected Follow-up Questions

* Where are static variables stored?
* Can instance methods access static variables?
* Are static variables thread-safe?

### Common Mistakes

* Using static variables for object-specific data.
* Assuming static variables are automatically thread-safe.

### Interview Keywords

* Static Variable
* Instance Variable
* Class Loading
* Shared State

---

# Q58. Static block use cases.

### Answer

A static block is used to perform **one-time class initialization** when the class is loaded.

Example:

```java
class Config {

    static {
        System.out.println("Loading configuration...");
    }
}
```

Typical use cases include:

* Initializing static fields.
* Loading configuration.
* Registering drivers or services.
* Performing one-time setup before objects are created.

Today, static blocks are used less frequently because dependency injection frameworks like Spring manage initialization more cleanly.

### Expected Follow-up Questions

* When does a static block execute?
* Can multiple static blocks exist?
* What happens if a static block throws an exception?

### Common Mistakes

* Putting business logic inside static blocks.
* Assuming they execute every time an object is created.

### Interview Keywords

* Static Block
* Class Initialization
* Class Loading
* One-time Initialization

---

# Q59. When are static blocks executed?

### Answer

Static blocks execute **once**, when the class is initialized by the JVM.

This typically happens when:

* The class is first actively used.
* A static method is called.
* A static field is accessed.
* An object of the class is created (if the class hasn't already been initialized).

If multiple static blocks exist, they execute in the order they appear in the class.

Static initialization happens before any constructor is executed.

### Expected Follow-up Questions

* What triggers class initialization?
* Can a static block execute multiple times?
* What is the order of static initialization?

### Common Mistakes

* Saying static blocks execute for every object.
* Confusing class loading with object creation.

### Interview Keywords

* Class Initialization
* Static Block
* JVM
* Class Loader

---

# Q60. Can static method access instance variables?

### Answer

No. A static method cannot directly access instance variables because it belongs to the class, not to any specific object.

Example:

```java
class Employee {

    String name;

    static void printName() {
        // name; // Compilation error
    }
}
```

A static method has no `this` reference, so it doesn't know which object's instance variable should be accessed.

However, if an object reference is available, the static method can access the instance variables through that object.

```java
static void print(Employee emp) {
    System.out.println(emp.name);
}
```

### Expected Follow-up Questions

* Why is `this` unavailable in static methods?
* Can an instance method access static members?
* Why are static methods resolved at compile time?

### Common Mistakes

* Trying to access instance fields directly from static methods.
* Assuming static methods have access to object state.

### Interview Keywords

* Static Method
* Instance Variable
* `this`
* Class Context

# Q61. Can instance method access static members?

### Answer

Yes. An instance method can directly access both **instance members** and **static members**.

This is because an instance method is invoked on an object, so it has access to:

* The object's state (`this`)
* Class-level members (`static`)

Example:

```java
class Employee {

    static String company = "ABC";
    String name;

    void printDetails() {
        System.out.println(name);      // Instance variable
        System.out.println(company);   // Static variable
    }
}
```

Although static members can be accessed through an object, it's considered a best practice to access them using the **class name** because they belong to the class, not a particular object.

```java
System.out.println(Employee.company);
```

### Expected Follow-up Questions

* Can a static method access instance members?
* Why is accessing static members via the class name recommended?
* Does an instance method have access to `this`?

### Common Mistakes

* Thinking instance methods cannot access static members.
* Accessing static members through objects instead of the class.

### Interview Keywords

* Instance Method
* Static Member
* `this`
* Class Member

---

# Q62. Can constructors be static?

### Answer

No. Constructors cannot be `static`.

A constructor is responsible for initializing an object, while a static member belongs to the class and exists even before any object is created.

Since constructors are invoked during object creation, making them static would not make sense.

If you need object creation logic that doesn't directly use a constructor, use a **static factory method** instead.

Example:

```java
class Employee {

    private Employee() {}

    public static Employee create() {
        return new Employee();
    }
}
```

Static factory methods provide more flexibility than constructors, such as meaningful names or returning cached instances.

### Expected Follow-up Questions

* Why can't constructors be static?
* What are static factory methods?
* When should you use factory methods over constructors?

### Common Mistakes

* Confusing constructors with static initialization blocks.
* Assuming constructors belong to the class.

### Interview Keywords

* Constructor
* Static Factory Method
* Object Creation
* Class Initialization

---

# Q63. When should utility classes use static methods?

### Answer

Utility classes should use static methods when the methods are **stateless**, don't depend on object state, and provide reusable functionality.

Examples include:

* `Math`
* `Collections`
* `Objects`
* `Arrays`

Example:

```java
class StringUtils {

    public static boolean isBlank(String str) {
        return str == null || str.trim().isEmpty();
    }
}
```

Since these methods don't rely on instance variables, creating objects would be unnecessary overhead.

To prevent instantiation, utility classes are usually declared `final` with a private constructor.

```java
final class StringUtils {

    private StringUtils() {}

    public static boolean isBlank(String str) {
        return str == null || str.trim().isEmpty();
    }
}
```

### Expected Follow-up Questions

* Why use a private constructor?
* When should methods not be static?
* Can utility classes be inherited?

### Common Mistakes

* Making methods static when they require object state.
* Allowing instantiation of utility classes.

### Interview Keywords

* Utility Class
* Static Method
* Stateless
* Private Constructor

---

# Q64. Explain dynamic method dispatch.

### Answer

Dynamic method dispatch is the mechanism by which the JVM decides **at runtime** which overridden method to execute based on the **actual object type**, not the reference type.

Example:

```java
class Animal {
    void sound() {
        System.out.println("Animal");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Bark");
    }
}

Animal animal = new Dog();
animal.sound();   // Bark
```

Although the reference type is `Animal`, the JVM invokes `Dog`'s implementation because the actual object is a `Dog`.

This is the foundation of runtime polymorphism and is widely used in frameworks like Spring through interfaces and dependency injection.

### Expected Follow-up Questions

* How does the JVM decide which method to call?
* Is this compile-time or runtime binding?
* Does it apply to static methods?

### Common Mistakes

* Thinking the reference type determines the method.
* Confusing dynamic dispatch with method overloading.

### Interview Keywords

* Dynamic Dispatch
* Runtime Polymorphism
* Method Overriding
* Late Binding

---

# Q65. How does JVM decide which overridden method to call?

### Answer

The JVM decides based on the **actual runtime type of the object**, not the reference type.

Example:

```java
Animal animal = new Dog();
animal.sound();
```

At compile time, the compiler verifies that `sound()` exists in the `Animal` reference type.

At runtime, the JVM sees that the actual object is `Dog` and invokes `Dog.sound()`.

Internally, the JVM uses method lookup mechanisms (often implemented using virtual method tables or similar optimizations) to efficiently resolve overridden methods.

As developers, the important takeaway is that overridden methods are resolved at **runtime**, enabling polymorphism.

### Expected Follow-up Questions

* What is a virtual method table (vtable)?
* Is this early binding or late binding?
* Does this affect performance?

### Common Mistakes

* Saying the compiler decides overridden methods.
* Confusing compile-time checking with runtime dispatch.

### Interview Keywords

* Runtime Type
* Virtual Method
* Dynamic Dispatch
* Late Binding

---

# Q66. Difference between early binding and late binding.

### Answer

**Early binding** happens at compile time, while **late binding** happens at runtime.

| Early Binding      | Late Binding                |
| ------------------ | --------------------------- |
| Compile time       | Runtime                     |
| Method overloading | Method overriding           |
| Static methods     | Instance overridden methods |
| Final methods      | Runtime polymorphic methods |

Examples of **early binding**:

* Method overloading
* Static methods
* Private methods
* Final methods

Example of **late binding**:

```java
Animal animal = new Dog();
animal.sound();
```

The compiler only verifies that `sound()` exists. The JVM chooses the implementation at runtime.

### Expected Follow-up Questions

* Which methods use early binding?
* Why are static methods early bound?
* How is late binding implemented?

### Common Mistakes

* Saying all instance methods use late binding.
* Forgetting that `final` methods are early bound.

### Interview Keywords

* Early Binding
* Late Binding
* Compile Time
* Runtime
* Dynamic Dispatch

---

# Q67. How does Java achieve runtime polymorphism internally?

### Answer

Java achieves runtime polymorphism through **method overriding** and **dynamic method dispatch**.

When an overridden method is called:

1. The compiler checks that the method exists in the reference type.
2. At runtime, the JVM checks the actual object type.
3. The JVM invokes the overridden implementation of that object.

```java
Animal animal = new Dog();
animal.sound();
```

Although the reference type is `Animal`, the JVM executes `Dog.sound()`.

Internally, JVM implementations optimize this using mechanisms such as virtual method tables, making method lookup very efficient.

### Expected Follow-up Questions

* What is dynamic dispatch?
* Does overloading use runtime polymorphism?
* What is a virtual method table?

### Common Mistakes

* Mixing up overloading and overriding.
* Thinking the compiler chooses overridden methods.

### Interview Keywords

* Runtime Polymorphism
* Method Overriding
* Dynamic Dispatch
* Virtual Method

---

# Q68. Can fields be polymorphic?

### Answer

No. Fields are **not polymorphic**.

Only methods participate in runtime polymorphism.

Example:

```java
class Parent {
    String name = "Parent";
}

class Child extends Parent {
    String name = "Child";
}

Parent obj = new Child();
System.out.println(obj.name);
```

Output:

```text
Parent
```

Field access is resolved using the **reference type**, not the runtime object type.

This is known as **field hiding**, not polymorphism.

### Expected Follow-up Questions

* Why aren't fields polymorphic?
* What is field hiding?
* How is it different from method overriding?

### Common Mistakes

* Assuming fields behave like overridden methods.
* Expecting runtime dispatch for variables.

### Interview Keywords

* Field Hiding
* Reference Type
* Compile-time Resolution
* Polymorphism

---

# Q69. What happens if subclass hides parent field?

### Answer

If a subclass declares a field with the same name as the parent, the child field **hides** the parent field.

Example:

```java
class Parent {
    String name = "Parent";
}

class Child extends Parent {
    String name = "Child";
}

Child child = new Child();

System.out.println(child.name);          // Child
System.out.println(((Parent) child).name); // Parent
```

Unlike methods, fields are resolved using the **reference type**, so both fields exist independently.

Field hiding is generally discouraged because it reduces readability and can cause confusion.

### Expected Follow-up Questions

* Is this overriding?
* Why are fields resolved differently?
* Should field hiding be used?

### Common Mistakes

* Calling field hiding "overriding."
* Assuming the parent field disappears.

### Interview Keywords

* Field Hiding
* Reference Type
* Shadowing
* Compile-time Resolution

---

# Q70. Method hiding vs method overriding.

### Answer

Method hiding applies to **static methods**, while method overriding applies to **instance methods**.

| Method Hiding           | Method Overriding           |
| ----------------------- | --------------------------- |
| Static methods          | Instance methods            |
| Compile-time resolution | Runtime resolution          |
| Based on reference type | Based on actual object type |
| No runtime polymorphism | Runtime polymorphism        |

Example of **method hiding**:

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

Parent obj = new Child();
obj.display(); // Parent
```

Example of **method overriding**:

```java
class Parent {
    void display() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    @Override
    void display() {
        System.out.println("Child");
    }
}

Parent obj = new Child();
obj.display(); // Child
```

As a best practice, avoid hiding static methods unless there's a compelling reason, since it can make code harder to understand.

### Expected Follow-up Questions

* Why can't static methods be overridden?
* How does runtime polymorphism work?
* What is dynamic dispatch?

### Common Mistakes

* Confusing method hiding with overriding.
* Expecting runtime polymorphism for static methods.

### Interview Keywords

* Method Hiding
* Method Overriding
* Static Method
* Runtime Polymorphism
* Dynamic Dispatch

# Q71. What is pass-by-value in Java?

### Answer

Java is **always pass-by-value**. The value that gets passed depends on the type:

* For **primitive types**, the actual value is copied.
* For **objects**, the **reference value** is copied—not the object itself.

This means the called method receives its own copy of the reference. Both references point to the same object initially, so the object can be modified, but reassigning the reference inside the method does not affect the caller's reference.

Example:

```java id="0vwd2h"
void update(Employee emp) {
    emp.setName("Alice");   // Modifies the same object
}

Employee emp = new Employee();
update(emp);
```

The object is modified because both references point to the same object.

### Expected Follow-up Questions

* Is Java pass-by-reference?
* Why do people think Java is pass-by-reference?
* What happens when an object reference is passed?

### Common Mistakes

* Saying Java supports pass-by-reference.
* Confusing object references with objects.

### Interview Keywords

* Pass-by-Value
* Object Reference
* Primitive
* Reference Copy

---

# Q72. Explain parameter passing using objects.

### Answer

When an object is passed to a method, Java copies the **reference value**, not the object.

Example:

```java id="s0vuz4"
void changeName(Employee emp) {
    emp.setName("Alice");
}

Employee emp = new Employee();
changeName(emp);
```

Here:

* The caller and the method have different reference variables.
* Both references point to the same object.
* Modifying the object's state is visible to the caller.

However, reassigning the parameter only changes the local copy of the reference.

### Expected Follow-up Questions

* Why is the object modified?
* Does Java copy the object?
* What happens if the reference is reassigned?

### Common Mistakes

* Saying the object itself is passed.
* Assuming assignment creates a new object.

### Interview Keywords

* Reference Copy
* Pass-by-Value
* Object State
* Method Parameter

---

# Q73. Can you modify object passed as parameter?

### Answer

Yes. You can modify the object's state because both the caller and the method refer to the same object.

Example:

```java id="9n30y0"
void update(Employee emp) {
    emp.setName("Alice");
}

Employee emp = new Employee();
update(emp);
```

After the method call, `emp.getName()` returns `"Alice"`.

This works because the copied reference still points to the same object.

### Expected Follow-up Questions

* Why does the change reflect outside the method?
* Is Java pass-by-reference?
* What if the object is immutable?

### Common Mistakes

* Thinking Java passes the object itself.
* Assuming object modification means pass-by-reference.

### Interview Keywords

* Object Mutation
* Shared Object
* Reference Copy
* Pass-by-Value

---

# Q74. Can you reassign caller reference?

### Answer

No. Reassigning a parameter does **not** change the caller's reference because Java passes a **copy of the reference**.

Example:

```java id="qt3rbd"
void change(Employee emp) {
    emp = new Employee();
}

Employee emp = new Employee();
change(emp);
```

After the method returns, the caller's `emp` still points to the original object.

The reassignment only affects the local parameter inside the method.

### Expected Follow-up Questions

* Why doesn't reassignment affect the caller?
* Can you replace the caller's object?
* What if the method returns the new object?

### Common Mistakes

* Assuming parameter reassignment changes the caller's variable.
* Confusing reassignment with object modification.

### Interview Keywords

* Reference Reassignment
* Pass-by-Value
* Local Variable
* Reference Copy

---

# Q75. What is covariant return type?

### Answer

A **covariant return type** allows an overridden method to return a **subclass** of the original return type.

Example:

```java id="vmuh4r"
class Animal {}

class Dog extends Animal {}

class Parent {
    Animal create() {
        return new Animal();
    }
}

class Child extends Parent {
    @Override
    Dog create() {
        return new Dog();
    }
}
```

Here, `Dog` is a subtype of `Animal`, so the override is valid.

Covariant return types improve type safety and reduce the need for explicit casting.

### Expected Follow-up Questions

* Is this allowed in overloading?
* Why is it useful?
* What are the rules for overriding?

### Common Mistakes

* Thinking any return type is allowed.
* Confusing covariant returns with overloaded methods.

### Interview Keywords

* Covariant Return Type
* Method Overriding
* Inheritance
* Type Safety

---

# Q76. Explain initialization order in Java.

### Answer

The initialization order depends on whether we're talking about **class initialization** or **object creation**.

For the **first object creation**, the order is:

1. Parent static fields
2. Parent static blocks
3. Child static fields
4. Child static blocks
5. Parent instance fields
6. Parent instance initialization blocks
7. Parent constructor
8. Child instance fields
9. Child instance initialization blocks
10. Child constructor

Example:

```java id="wsrkx8"
class Parent {
    static { System.out.println("Parent static"); }
    { System.out.println("Parent instance"); }
    Parent() { System.out.println("Parent constructor"); }
}

class Child extends Parent {
    static { System.out.println("Child static"); }
    { System.out.println("Child instance"); }
    Child() { System.out.println("Child constructor"); }
}
```

The **static initialization** happens only once per class, while the **instance initialization** happens every time an object is created.

### Expected Follow-up Questions

* When do static blocks execute?
* What happens during object creation?
* Why does the parent constructor execute first?

### Common Mistakes

* Forgetting that static initialization happens only once.
* Mixing class initialization with object initialization.

### Interview Keywords

* Initialization Order
* Static Block
* Instance Initializer
* Constructor Chaining
* Class Loading

---

# Q77. Can constructor call overridden method?

### Answer

Yes. A constructor **can** call an overridable method, but it is considered a bad practice.

Example:

```java id="o38w3i"
class Parent {

    Parent() {
        display();
    }

    void display() {}
}

class Child extends Parent {

    private String name = "Alice";

    @Override
    void display() {
        System.out.println(name);
    }
}
```

When a `Child` object is created, the `Parent` constructor executes first. At that point, the `Child` fields haven't been initialized yet, but due to runtime polymorphism, `Child.display()` is invoked.

This may produce unexpected results because the child object is only partially initialized.

### Expected Follow-up Questions

* Why is this dangerous?
* What gets initialized first?
* Does runtime polymorphism still apply inside constructors?

### Common Mistakes

* Assuming child fields are initialized before the parent constructor.
* Forgetting that overridden methods use runtime dispatch.

### Interview Keywords

* Constructor
* Runtime Polymorphism
* Partial Initialization
* Dynamic Dispatch

---

# Q78. Why is calling overridable methods inside constructor dangerous?

### Answer

It's dangerous because the overridden method may execute **before the subclass has finished initializing its fields**.

Example:

```java id="ddqk7x"
class Parent {

    Parent() {
        display();
    }

    void display() {}
}

class Child extends Parent {

    private String message = "Hello";

    @Override
    void display() {
        System.out.println(message);
    }
}
```

When the parent constructor calls `display()`, the `message` field is still at its default value (`null`) because the child initialization hasn't happened yet.

This can lead to:

* Incorrect behavior
* `NullPointerException`
* Using partially initialized objects

A good practice is to avoid calling overridable methods from constructors. If initialization depends on subclass behavior, use factory methods or explicit initialization after construction.

### Expected Follow-up Questions

* What is partial initialization?
* How can this be avoided?
* Does Effective Java recommend avoiding this?

### Common Mistakes

* Assuming subclass fields are initialized first.
* Calling business logic from constructors.

### Interview Keywords

* Partial Initialization
* Constructor
* Runtime Dispatch
* Effective Java

---

# Q79. Difference between checked and unchecked exceptions.

### Answer

The main difference is whether the compiler enforces handling them.

| Checked Exception                                 | Unchecked Exception       |
| ------------------------------------------------- | ------------------------- |
| Checked at compile time                           | Checked at runtime        |
| Must be handled or declared                       | Handling is optional      |
| Extend `Exception` (excluding `RuntimeException`) | Extend `RuntimeException` |

Examples:

**Checked:**

```java id="2f0utp"
IOException
SQLException
```

**Unchecked:**

```java id="l9s9j0"
NullPointerException
IllegalArgumentException
ArithmeticException
```

In general:

* Use **checked exceptions** for recoverable conditions that callers are expected to handle.
* Use **unchecked exceptions** for programming errors or invalid API usage.

### Expected Follow-up Questions

* Why does Spring prefer runtime exceptions?
* Should custom exceptions be checked or unchecked?
* Can checked exceptions be ignored?

### Common Mistakes

* Saying checked exceptions occur only at compile time.
* Catching generic `Exception` everywhere.

### Interview Keywords

* Checked Exception
* RuntimeException
* Exception Handling
* Compile-time Checking

---

# Q80. Can interface contain private methods?

### Answer

Yes. Since **Java 9**, interfaces can contain **private methods**.

They are mainly used to avoid duplicating logic shared by multiple `default` or `static` methods within the same interface.

Example:

```java id="q45tn5"
interface Logger {

    default void logInfo() {
        format("INFO");
    }

    default void logError() {
        format("ERROR");
    }

    private void format(String level) {
        System.out.println(level);
    }
}
```

The private method is only accessible inside the interface itself and cannot be called by implementing classes.

This feature improves code reuse without exposing helper methods as part of the interface's public API.

### Expected Follow-up Questions

* Why were private methods added?
* Can implementing classes override them?
* Can private methods be static?

### Common Mistakes

* Saying interfaces cannot contain private methods.
* Thinking private interface methods are inherited.

### Interview Keywords

* Java 9
* Interface
* Private Method
* Default Method
* Code Reuse

# Q81. Can interface contain static methods?

### Answer

Yes. Since **Java 8**, interfaces can contain **static methods**.

Static methods belong to the interface itself, not to its implementations. They are typically used for utility methods that are closely related to the interface.

Example:

```java id="k3m7x1"
interface Validator {

    static boolean isValid(String input) {
        return input != null && !input.isBlank();
    }
}
```

They are invoked using the interface name:

```java id="p8v2zr"
Validator.isValid("Java");
```

Unlike default methods, static interface methods are **not inherited** by implementing classes.

### Expected Follow-up Questions

* Why were static methods added to interfaces?
* Can implementing classes override static interface methods?
* What is the difference between static and default methods?

### Common Mistakes

* Assuming static interface methods are inherited.
* Calling them through an implementation object.

### Interview Keywords

* Java 8
* Static Method
* Interface
* Utility Method

---

# Q82. Default methods in interfaces.

### Answer

Default methods are methods in an interface that have a default implementation. They were introduced in **Java 8** using the `default` keyword.

Example:

```java id="f6w9qd"
interface Vehicle {

    default void start() {
        System.out.println("Starting vehicle");
    }
}
```

Implementing classes can:

* Use the default implementation as-is.
* Override it with their own implementation.

Default methods allow interfaces to evolve by adding new methods without breaking existing implementations.

### Expected Follow-up Questions

* Why were default methods introduced?
* Can default methods be overridden?
* What happens if two interfaces define the same default method?

### Common Mistakes

* Thinking default methods cannot have implementations.
* Confusing default methods with abstract methods.

### Interview Keywords

* Java 8
* Default Method
* Interface Evolution
* Backward Compatibility

---

# Q83. Why were default methods introduced?

### Answer

Default methods were introduced in **Java 8** to allow interfaces to evolve **without breaking existing implementations**.

Before Java 8, adding a new method to an interface would force every implementing class to implement that method, breaking existing code.

For example, many new methods were added to the Collections Framework in Java 8, such as `forEach()` and `removeIf()`. Default methods allowed these APIs to evolve while remaining backward compatible.

So the primary goal was **backward compatibility**, not multiple inheritance.

### Expected Follow-up Questions

* What problem did default methods solve?
* Why not use abstract classes instead?
* How do default methods affect backward compatibility?

### Common Mistakes

* Saying they were introduced mainly for multiple inheritance.
* Forgetting the backward compatibility motivation.

### Interview Keywords

* Java 8
* Backward Compatibility
* Interface Evolution
* Default Method

---

# Q84. Multiple default methods conflict.

### Answer

If a class implements two interfaces that provide the **same default method**, Java cannot decide which implementation to use.

The implementing class **must explicitly override** the conflicting method.

Example:

```java id="r2h7mt"
interface A {
    default void show() {
        System.out.println("A");
    }
}

interface B {
    default void show() {
        System.out.println("B");
    }
}

class C implements A, B {

    @Override
    public void show() {
        System.out.println("Resolved");
    }
}
```

Without overriding `show()`, the code will not compile because the JVM would face ambiguity.

### Expected Follow-up Questions

* Why doesn't Java choose one automatically?
* How do you call a specific interface's default method?
* Is this related to the Diamond Problem?

### Common Mistakes

* Assuming Java gives priority to the first interface.
* Forgetting that overriding is mandatory.

### Interview Keywords

* Default Method
* Interface Conflict
* Multiple Inheritance
* Ambiguity

---

# Q85. Explain diamond problem with default methods.

### Answer

The **Diamond Problem** occurs when a class inherits the same method from multiple parent types, creating ambiguity about which implementation should be used.

With interfaces, this can happen when two interfaces define the same default method.

Example:

```java id="9x4nua"
interface A {
    default void show() {
        System.out.println("A");
    }
}

interface B {
    default void show() {
        System.out.println("B");
    }
}

class C implements A, B {

    @Override
    public void show() {
        A.super.show(); // or B.super.show()
    }
}
```

Java resolves this by requiring the implementing class to override the method. If needed, it can invoke a specific interface's implementation using `InterfaceName.super.method()`.

This is one reason Java supports multiple inheritance through interfaces but not through classes.

### Expected Follow-up Questions

* How do you resolve the conflict?
* What does `A.super.show()` do?
* Why doesn't Java allow multiple class inheritance?

### Common Mistakes

* Thinking Java automatically picks one implementation.
* Confusing interface conflicts with class inheritance.

### Interview Keywords

* Diamond Problem
* Default Method
* `InterfaceName.super`
* Multiple Inheritance

---

# Q86. You have a class with 25 fields. How would you redesign it?

### Answer

I would first question whether the class has **too many responsibilities**.

My approach would be:

1. Check if the class violates the **Single Responsibility Principle (SRP)**.
2. Group related fields into smaller value objects.
3. Split unrelated responsibilities into separate classes.
4. Use composition instead of creating a "God Object."
5. If construction becomes complex, introduce the **Builder Pattern**.

For example, instead of:

```text id="x0v7pk"
Employee
├── Personal Details
├── Address
├── Salary
├── Bank Details
├── Emergency Contact
```

I'd redesign it as:

```text id="0kq3me"
Employee
├── PersonalInfo
├── Address
├── SalaryDetails
├── BankDetails
├── EmergencyContact
```

This improves readability, maintainability, and testability.

### Expected Follow-up Questions

* Would you always split the class?
* When would you use the Builder pattern?
* How do you identify a God Object?

### Common Mistakes

* Splitting classes without understanding domain boundaries.
* Keeping all fields in one large DTO or entity.

### Interview Keywords

* SRP
* Composition
* Value Object
* Builder Pattern
* God Object

---

# Q87. A class has over 100 methods. What problems do you foresee?

### Answer

A class with over 100 methods is usually a strong indication that it has **too many responsibilities**.

Potential problems include:

* Violation of the Single Responsibility Principle.
* Difficult to understand and maintain.
* Higher chance of merge conflicts.
* Harder to unit test.
* Increased coupling.
* Poor readability and discoverability.

I'd review the methods and group them by responsibility. Often, they can be extracted into smaller services or helper classes with well-defined responsibilities.

### Expected Follow-up Questions

* How would you refactor it?
* What metrics indicate a God Class?
* Would you use inheritance?

### Common Mistakes

* Judging only by the number of methods.
* Splitting classes arbitrarily instead of by responsibility.

### Interview Keywords

* God Class
* SRP
* Maintainability
* Refactoring
* Coupling

---

# Q88. A service method accepts 15 parameters. How would you redesign it?

### Answer

A method with 15 parameters is difficult to read, use, and maintain.

I would redesign it by:

1. Grouping related parameters into domain objects or DTOs.
2. Introducing a request object if the parameters belong to one operation.
3. Using the Builder pattern if many parameters are optional.
4. Validating inputs close to the request object.

Instead of:

```java id="j8t4vs"
createOrder(
    name,
    phone,
    address,
    city,
    state,
    ...
);
```

I'd prefer:

```java id="u1s9gf"
createOrder(CreateOrderRequest request);
```

This makes the API cleaner and easier to extend without constantly changing the method signature.

### Expected Follow-up Questions

* When would you use the Builder pattern?
* Is a DTO always the right choice?
* How do you validate such requests?

### Common Mistakes

* Passing unrelated parameters in one DTO.
* Using a generic `Map<String, Object>` instead of a typed object.

### Interview Keywords

* Parameter Object
* DTO
* Builder Pattern
* API Design
* Maintainability

---

# Q89. You discover deep inheritance (7 levels). Would you keep it? Why?

### Answer

In most cases, **no**. A seven-level inheritance hierarchy is usually a design smell.

Problems include:

* Tight coupling.
* Hard to understand behavior.
* Difficult debugging because logic is spread across many classes.
* Higher risk of breaking subclasses when changing parent classes.
* Reduced flexibility.

I'd first understand whether each level represents a genuine **IS-A** relationship. If not, I'd gradually refactor toward composition where it improves maintainability.

I wouldn't rewrite everything immediately unless there's a business need, but I would avoid extending the hierarchy further.

### Expected Follow-up Questions

* Would you refactor immediately?
* How would composition help?
* What is the Fragile Base Class problem?

### Common Mistakes

* Refactoring large hierarchies without understanding their purpose.
* Using inheritance just for code reuse.

### Interview Keywords

* Deep Inheritance
* Composition
* IS-A
* Fragile Base Class
* Refactoring

---

# Q90. You need to expose a read-only object to clients. How would you design it?

### Answer

The design depends on whether the object itself is mutable.

If possible, I'd make the object **immutable**:

* `final` class
* `private final` fields
* No setters
* Defensive copies for mutable fields

If the object must remain mutable internally, I'd expose a **read-only view** or return defensive copies of mutable state.

For collections, for example:

```java id="n7f3ly"
public List<String> getItems() {
    return List.copyOf(items);
}
```

or

```java id="b6z8qp"
public List<String> getItems() {
    return Collections.unmodifiableList(items);
}
```

This prevents clients from modifying the object's exposed state while still allowing the owning class to manage it internally.

### Expected Follow-up Questions

* Why isn't `final` alone enough?
* `Collections.unmodifiableList()` vs `List.copyOf()`?
* When should defensive copying be used?

### Common Mistakes

* Returning internal mutable collections directly.
* Assuming `final` makes objects immutable.

### Interview Keywords

* Immutable Object
* Defensive Copy
* Encapsulation
* Read-only View
* `List.copyOf()`

# Q91. Multiple developers keep modifying shared objects causing bugs. How would you solve this?

### Answer

My first goal would be to **reduce shared mutable state**, because it's a common source of bugs and race conditions.

Depending on the use case, I'd consider:

1. Make the object immutable if possible.
2. Avoid sharing the same object across multiple components.
3. Use defensive copying when passing mutable objects.
4. Restrict modifications through well-defined methods instead of public setters.
5. If concurrent updates are required, use appropriate synchronization or concurrent data structures.

For example, instead of passing the same mutable DTO across multiple services, I'd create immutable request objects or copy the object before modifying it.

In production, immutability is usually the simplest and safest solution because it eliminates an entire class of concurrency issues.

### Expected Follow-up Questions

* Why are immutable objects thread-safe?
* When would synchronization be required?
* What is defensive copying?

### Common Mistakes

* Sharing mutable objects across multiple threads.
* Exposing mutable collections directly.

### Interview Keywords

* Shared Mutable State
* Immutability
* Defensive Copy
* Thread Safety
* Race Condition

---

# Q92. Your `HashMap` suddenly behaves incorrectly. Where would you start debugging?

### Answer

I'd first verify whether the **key's `equals()` and `hashCode()` implementations are correct**, because most `HashMap` issues originate there.

My debugging approach would be:

1. Check whether `equals()` and `hashCode()` follow the contract.
2. Verify the key object isn't mutable after insertion.
3. Check whether duplicate logical keys exist.
4. Confirm the correct key object is being used during lookup.
5. If it's a concurrent scenario, verify whether `HashMap` is being accessed safely.

For example, if a field used in `hashCode()` changes after insertion, the object may end up in a different logical bucket, causing lookups to fail.

In production, mutable keys are one of the most common causes of unexpected `HashMap` behavior.

### Expected Follow-up Questions

* Why shouldn't mutable objects be HashMap keys?
* How does HashMap use `equals()` and `hashCode()`?
* When should `ConcurrentHashMap` be used?

### Common Mistakes

* Overriding `equals()` without `hashCode()`.
* Modifying key fields after insertion.

### Interview Keywords

* HashMap
* hashCode()
* equals()
* Mutable Key
* Hash Collision

---

# Q93. You observe duplicate objects with same values inside `HashSet`. Possible reasons?

### Answer

The most likely reason is that the class does **not correctly override `equals()` and `hashCode()`**.

`HashSet` determines uniqueness using both methods:

* `hashCode()` finds the bucket.
* `equals()` checks logical equality.

Possible causes include:

* `equals()` not overridden.
* `hashCode()` not overridden.
* Incorrect implementation of either method.
* Mutable fields used in `equals()` or `hashCode()` that changed after insertion.

For a `HashSet`, two logically equal objects should produce the same hash code and be equal according to `equals()`.

### Expected Follow-up Questions

* Why does HashSet use both methods?
* Can hash collisions cause duplicates?
* What happens if the key is mutable?

### Common Mistakes

* Overriding only one of the methods.
* Assuming `HashSet` only checks `equals()`.

### Interview Keywords

* HashSet
* equals()
* hashCode()
* Object Equality
* Hash Contract

---

# Q94. Team frequently misuses `equals()`. How would you enforce correctness?

### Answer

I'd address it through both **coding standards** and **code reviews**.

Some practices I follow are:

* Always override `equals()` and `hashCode()` together.
* Use the `@Override` annotation.
* Add unit tests covering equality and hash code behavior.
* Avoid mutable fields in equality checks whenever possible.
* Use IDE-generated implementations as a starting point and review them carefully.

During code reviews, I'd specifically check:

* Equality contract.
* Null handling.
* Symmetry and consistency.
* Compatibility with hash-based collections.

This helps prevent subtle production bugs involving `HashMap` and `HashSet`.

### Expected Follow-up Questions

* What should unit tests verify?
* Why avoid mutable fields?
* Should IDs always be used in `equals()`?

### Common Mistakes

* Comparing strings with `==`.
* Forgetting to update `hashCode()` after modifying `equals()`.

### Interview Keywords

* equals()
* hashCode()
* Code Review
* Unit Testing
* Equality Contract

---

# Q95. A class has mutable public fields. What problems may occur?

### Answer

Public mutable fields break encapsulation because any code can modify the object's internal state without validation.

Problems include:

* Invalid object state.
* Difficult debugging.
* Harder to enforce business rules.
* Tight coupling.
* Concurrency issues if shared across threads.

Example:

```java id="0qq0zd"
class Account {
    public double balance;
}
```

Any caller can directly change `balance`, bypassing validation.

A better design is to keep fields `private` and expose controlled methods for modification.

### Expected Follow-up Questions

* Why keep fields private?
* How does encapsulation help?
* What if the object is immutable?

### Common Mistakes

* Making entity fields public.
* Using setters without validation.

### Interview Keywords

* Encapsulation
* Data Hiding
* Mutable State
* Validation

---

# Q96. Have you ever created custom immutable classes? Where?

### Answer

I haven't created many completely immutable domain classes in production because most of the objects I work with are **JPA entities, MongoDB documents, or DTOs**, which are typically mutable.

However, I have created immutable helper objects and configuration-style classes where the state should not change after creation. I followed standard practices like:

* `final` class
* `private final` fields
* Constructor initialization
* No setters
* Defensive copying for mutable fields

In general, I prefer immutability for value objects or configuration data because it simplifies reasoning about the code and avoids accidental modifications.

### Expected Follow-up Questions

* Why aren't JPA entities immutable?
* Where would you prefer immutable objects?
* What is defensive copying?

### Common Mistakes

* Claiming every production class should be immutable.
* Ignoring framework requirements like JPA proxies.

### Interview Keywords

* Immutable Class
* Value Object
* DTO
* Defensive Copy

---

# Q97. How do you design DTOs?

### Answer

I design DTOs as **simple data carriers** for communication between layers or services.

Some principles I follow are:

* Keep them focused on a specific API or use case.
* Avoid business logic inside DTOs.
* Include only the fields required by the client.
* Use validation annotations where appropriate.
* Keep them separate from persistence entities.

In Spring Boot applications, DTOs help decouple the API contract from the database model, allowing each to evolve independently.

### Expected Follow-up Questions

* Why not expose entities directly?
* Should DTOs be immutable?
* How do you map DTOs to entities?

### Common Mistakes

* Putting business logic in DTOs.
* Reusing the same DTO for unrelated APIs.

### Interview Keywords

* DTO
* API Contract
* Validation
* Layered Architecture
* Decoupling

---

# Q98. How do you design Entity classes?

### Answer

Entity classes represent the persistence model, so I design them around the database while keeping them maintainable.

Some practices I follow are:

* Model the domain accurately.
* Keep fields `private`.
* Use meaningful relationships.
* Avoid exposing entities directly through REST APIs.
* Keep business logic separate from persistence concerns where appropriate.
* Override `equals()` and `hashCode()` carefully, especially when identity is involved.

In Spring Data or JPA applications, I also avoid placing unnecessary business logic inside entities to keep them focused on persistence.

### Expected Follow-up Questions

* Why not expose entities through APIs?
* Should entities be immutable?
* How do you implement `equals()` for entities?

### Common Mistakes

* Returning entities directly from controllers.
* Mixing persistence logic with API contracts.

### Interview Keywords

* Entity
* Persistence Model
* Encapsulation
* JPA
* Layered Architecture

---

# Q99. Where have you used interfaces in your project?

### Answer

I've primarily used interfaces to define contracts and keep components loosely coupled.

Some common examples from my projects include:

* Spring Data repository interfaces such as `ReactiveMongoRepository`.
* Service interfaces with separate implementation classes.
* Strategy-like components where multiple implementations are possible.
* External client abstractions to simplify testing and mocking.

Using interfaces makes unit testing easier because dependencies can be mocked, and implementations can be changed without affecting callers.

### Expected Follow-up Questions

* Why use interfaces instead of concrete classes?
* Does Spring require interfaces?
* How do interfaces help testing?

### Common Mistakes

* Creating interfaces for every class without a clear need.
* Treating interfaces as a replacement for good design.

### Interview Keywords

* Interface
* Loose Coupling
* Dependency Injection
* Mocking
* ReactiveMongoRepository

---

# Q100. Where have you used abstract classes?

### Answer

In my experience, I've used **interfaces much more frequently than abstract classes**.

I've used abstract classes when multiple related classes shared common implementation or state. For example, a base component that provides common utility methods or shared initialization while allowing subclasses to implement specific behavior.

For most service-layer designs in Spring Boot, I prefer interfaces because they provide more flexibility and align well with dependency injection.

So my general approach is:

* **Interface** for defining contracts.
* **Abstract class** when there is meaningful shared implementation or common state.

### Expected Follow-up Questions

* Why do you prefer interfaces?
* When is an abstract class a better choice?
* Can an abstract class implement an interface?

### Common Mistakes

* Using abstract classes only for code reuse.
* Creating inheritance hierarchies where composition would be simpler.

### Interview Keywords

* Abstract Class
* Interface
* Shared Implementation
* Dependency Injection
* Composition

