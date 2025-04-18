# OOPS 

# Table of Contents

1. [🚩 Procedural and OOPS Paradigm](#prodecural-and-OOPS-paradigm)
2. [🔍 Key Differences Between Java and C++ in OOP](#key-differences-between-java-and-c-in-oop)
3. [🚩 Topics to Focus On](#topics-to-focus-on)
   - [✅ Four Pillars of OOP](#-four-pillars-of-oop)
   - [✅ Solid Understanding of OOP Principles](#solid-understanding-of-oop-principles)
   - [Memory Management in OOP](#memory-management-in-oop)
4. [🚩 Classes and Objects](#classes-and-objects)
   - [Static vs Dynamic Memory Allocation](#static-vs-dynamic-memory-allocation)
   - [Access Specifiers](#access-specifiers)
   - [Member Functions](#member-functions)
   - [Structure and Class](#structure-and-class)
   - [Templates and Generics](#templates-and-generics)
5. [🚩 Constructor and Destructor](#constructor-and-destructor)
   - [Garbage Collector in Java](#garbage-collector-in-java)
   - [JDK, JRE, and JVM in Java](#jdk-jre-and-jvm-in-java)
   - [Shallow Copy vs Deep Copy](#shallow-copy-vs-deep-copy)
6. [🚩 Important Keywords](#important-keywords)
7. [🚩 Features of OOPs](#features-of-oops)
   - [Inheritance](#inheritance)
   - [Encapsulation](#encapsulation)
   - [Abstraction](#abstraction)
   - [Interface in Java](#interface-in-java)
   - [Polymorphism](#polymorphism)
8. [🚩 OOPS Pillars Comparison Table (with Real-Life Remote Example)](#oops-pillars-comparison-table-with-real-life-remote-example)


# 🚩 Prodecural and OOPS paradigm 
Procedural programming is about writing procedures or functions that perform operations on the data, while **object-oriented programming** is about creating objects that contain both data and functions.   
[What is OOPS ? (and advantages)](https://www.w3schools.com/cpp/cpp_oop.asp)
- **Simula** - first object-oriented programming language.
- **SmallTalk**- first truly object-oriented programming language.
  
- __Java__ is not considered a purely object-oriented programming language. While Java is predominantly object-oriented and most features are based on objects and classes, it does have some non-object-oriented elements. For example:
Primitive Data Types and Static variables

# 🔍 Key Differences Between Java and C++ in OOP

| Feature                    | Java                                           | C++                                                  |
|----------------------------|------------------------------------------------|------------------------------------------------------|
| Paradigm                   | Purely Object-Oriented (except primitive types) | Multi-Paradigm (Supports both procedural & OOP)      |
| Memory Management          | Automatic (Garbage Collector)                  | Manual (uses new and delete)                         |
| Multiple Inheritance       | Not supported (Achieved via Interfaces)        | Supported natively                                   |
| Pointers                   | Not available (only references)                | Fully supports pointers                              |
| Destructors                | No destructors (handled by GC)                 | Requires explicit destructors                        |
| Operator Overloading       | Not supported                                  | Fully supported                                      |
| Method Overriding          | Uses @Override annotation                      | Uses virtual keyword                                 |
| Access Specifiers          | public, private, protected                     | public, private, protected + friend keyword          |
| Exception Handling         | Mandatory (try-catch-finally)                  | Optional                                             |
| Templates vs Generics      | Uses Generics                                  | Uses Templates                                       |

# 🚩 TOPICS TO FOCUS ON 

## ✅ 1. **Four Pillars of OOP**

- **Encapsulation** – Data hiding using classes & private variables.
- **Abstraction** – Hiding implementation details using abstract classes & interfaces.
- **Inheritance** – Creating hierarchies (extends in Java, : in C++).
- **Polymorphism** – Method overloading & overriding.

## ✅ 2. **Solid Understanding of OOP Principles**

- **Constructor & Destructor** – Object lifecycle management.
- **Method Overloading vs Overriding** – Compile-time vs runtime polymorphism.
- **Virtual Functions & Pure Virtual Functions (C++)** – Dynamic polymorphism.
- **Abstract Classes vs Interfaces** – Java uses interfaces, C++ has abstract classes.
- **Multiple Inheritance & Diamond Problem (C++)** – How to resolve it using virtual inheritance.

## 3. **Memory Management in OOP**

- ✅ **Heap vs Stack Allocation** – `new` & `delete` (C++) vs Java’s Garbage Collector.
- ✅ **Shallow vs Deep Copy** – Handling copy constructors in C++.
- ✅ **Smart Pointers (C++ only)** – `unique_ptr`, `shared_ptr`, `weak_ptr`.
- ✅ **Garbage Collection (Java)** – Reference counting, GC roots, `finalize()`.

## Rohit negi OOPS (C++ short notes) ->  
<a>(https://www.linkedin.com/posts/rohit-negi9_oops-by-rohit-negi-activity-7284865865097920512-HYk1/)</a>

# 🚩 Classes and Objects 
A class is a USER-DEFINED DATA TYPE or template (blueprint) for objects, and an object is an instance of a class. A class is a group of objects which have **common properties**.  
It is a logical entity. It **can't be physical**.  
When the individual objects are created, memory is given at that time only. They inherit all the variables and functions from the class.  

**_Common Example:_**   
CLASS: fruit  
OBJECTS: apple, mango 

DO CHK THIS OUT-> <a>https://www.tpointtech.com/java-classes-and-objects</a>  
(fields, methods, nested classes,different ways tp create objects,  etc in java)  

- In **C++**, class name ends with a semicolon whereas in **Java** it isnt needed. (Syntax and other info can be chked through the site link mentioned)
- the **objects** gets the memory in the **heap** memory area. 
  ![image](https://github.com/user-attachments/assets/187747c2-e34c-441f-af41-842974450b24)

## 1. Static vs Dynamic Memory Allocation

| Feature        | Static Memory Allocation    | Dynamic Memory Allocation          |
|----------------|-----------------------------|------------------------------------|
| Timing         | Compile time                | Runtime                            |
| Location       | Stack                       | Heap                               |
| Size           | Fixed                       | Variable                           |
| Management     | Automatic                   | Manual/Garbage Collected           |
| Speed          | Faster                      | Slower                             |
| Use Cases      | Local variables, static variables | Objects, dynamic arrays         |

- **_C_**  
malloc(), calloc()
  - arr = (int*) malloc(5 * sizeof(int));       ( allocates a specified amount of memory but does not initialize the allocated memory (contains garbage values))  
  - arr = (int*) calloc(5, sizeof(int));      (Contiguous Allocation. allocates memory for an array of elements and initializes them to zero.)  
 
- **_C++:_**  
Uses the **new** keyword to allocate memory on the heap and the **delete** keyword to free it.  
- **_Java:_**  
Uses the new keyword to allocate memory for objects on the heap.
memory management is handled automatically by the JVM (Java Virtual Machine).

## 2. ACCESS SPECIFIERS
- default (java)
- public
- private
- protected   
<a>https://www.tpointtech.com/access-modifiers-in-java</a>   

### Access Modifiers

| Access Modifier | Within Class | Within Package | Outside Package by Subclass Only | Outside Package |
|-----------------|--------------|----------------|----------------------------------|-----------------|
| **Private**     | Y            | N              | N                                | N               |
| **Default**     | Y            | Y              | N                                | N               |
| **Protected**   | Y            | Y              | Y                                | N               |
| **Public**      | Y            | Y              | Y                                | Y               |


- **Compile-time errors** occur during code compilation (before execution), often due to syntax or type mismatches, while **runtime errors** occur during program execution (after compilation), such as division by zero or accessing an out-of-bounds array.

## 3. Member Functions  
- In C++, member functions are functions that are part of a class and can operate on its data members.  
- In Java, functions inside a class are called methods, but conceptually, they are the same as member functions in C++.  
- **[Types of MEMBER FUNCTIONS IN C++]**
  - (https://www.studytonight.com/cpp/types-of-member-function.php)
  -   
- Friend Functions is a reason, why C++ is not called as a pure Object Oriented language. Because it violates the concept of Encapsulation.  
- Inside Class Function --> inline keyword  
- Outside Class Function --> scope resolution operator (::) 

### Structure and Class
<a>(https://www.geeksforgeeks.org/structure-vs-class-in-cpp/)</a>

### Templates and Generics  
used to write the data type independent piece of code. The specified placeholder in the code gets replaced by the actual data type at the time of compilation, called the instantiation of code.  
<a>https://www.geeksforgeeks.org/templates-in-c-vs-generics-in-java/</a>  
 _**MACROS:**_
  Macros are the segment of code that is replaced by the macro value. They are defined by #define directive. They are efficient because of inline compilation. There is no type checking in it.   

# 🚩 Constructor and Destructor   
(chk rohit negi notes above for better theory)
- used to initialize the data members of new objects. 
- special function with no return type 
- automatically called when object is created.
- never be static
- name same as of class

## Types : ##
- DEFAULT
- PARAMETRISED
- COPY (Java does not have a built-in copy constructor like C++. Can be mannually implemented in java )

## Destructor  
<a> https://www.geeksforgeeks.org/destructors-c/</a>

## Garbage Collector in java  
GC runs automatically and identifies objects that are no longer referenced.
Unreachable objects are deleted, and memory is reclaimed.  
can Explicitly triggered using System.gc() (not guaranteed to run immediately)

### JDK, JRE AND JVM IN JAVA
```plaintext
  +------------------------------------------------------------+
  |                        Java Application                    |
  +------------------------------------------------------------+
                                |
                                v
                       +--------------------+
                       |   Java Compiler    |
                       +--------------------+
                                |
                                v
                       [Bytecode (.class)]
                                |
                                v
  +------------------------------------------------------------+
  |               Java Runtime Environment (JRE)               |
  |                                                            |
  |   +----------------------------------------------------+   |
  |   |             Java Virtual Machine (JVM)             |   |
  |   |                                                    |   |
  |   |   +--------------------------+   +---------------+ |   |
  |   |   |      Class Loader        |   |  Garbage      | |   |
  |   |   |                          |   |  Collector    | |   |
  |   |   +--------------------------+   +---------------+ |   |
  |   |                                                    |   |
  |   |   +------------------------------+                 |   |
  |   |   |   Memory Area (Heap/Stack)   |                 |   |
  |   |   +------------------------------+                 |   |
  |   |                                                    |   |
  |   |   +------------------------------+                 |   |
  |   |   |       Execution Engine       |                 |   |
  |   |   |   Includes:                  |                 |   |
  |   |   |   - Interpreter              |                 |   |
  |   |   |   - JIT Compiler             |                 |   |
  |   |   +------------------------------+                 |   |
  |   +----------------------------------------------------+   |
  +------------------------------------------------------------+
```

## SHALLOW COPY V/S DEEP COPY  
<a>https://www.tpointtech.com/shallow-copy-vs-deep-copy-in-java </a> (for java especially)    
<!--> <a>https://www.geeksforgeeks.org/difference-between-shallow-and-deep-copy-of-a-class/</a> 
 just asse hi when reading the article -(In Java, primitive data types are basic building blocks of data that store simple values directly in memory. They are not objects and are more efficient in terms of memory and performance.)  

## 🚩 Important Keywords
<!--> will study later
SNo | Topic | Link 
----|-------|------
1 | static | [view](https://www.youth4work.com/Talent/Core-Java/Forum/119567-wat-is-the-use-of-a-static-keyword)  
2 | virtual | [view](https://www.codeproject.com/Questions/270054/why-virtual-keyword-is-used) 
3 | abstract | [view](https://www.tutorialspoint.com/abstract-keyword-in-Java) 
4 | final | [view](https://www.javatpoint.com/final-keyword) 
5 | explicit | [view](https://www.geeksforgeeks.org/g-fact-93/) 
6 | this | [view](https://www.javatpoint.com/this-keyword) 
7 | new | [view](https://www.javatpoint.com/new-keyword-in-java) 
8 | const | [view](https://stackoverflow.com/questions/7428358/why-const-keyword-is-not-used-in-java) 
9 | super | [view](https://www.javatpoint.com/super-keyword)  

# 🚩 Features of OOPs :
- Polymorphism
- Inheritance
- Encapsulation
- Abstraction

##   Inheritance  
**java**- (extends keyword)  class derived extends base{...    
**c++** - class Derived : public Base{ ...  
_**Types :**_  
- Single  
- Mutliple
   - (not in **java** (diamond problem), supported via interfaces ) (in **c++** , issue is resolved via virtual keyword)
   -  Real-World Analogy:  
      Imagine A is a Person, B is a Mother, C is a Father, and D is a Child.
      Without virtual inheritance, the child may inherit two separate Person copies (one from mom, one from dad).  
      With virtual inheritance, there's only one shared Person identity — no confusion    
- Hierarchical  
- Multilevel  
- Hybrid / Virtual (not in java, supported via interfaces)    
  <a>https://www.tpointtech.com/inheritance-in-java</a> (java syntax and theory)    
  <a>https://www.geeksforgeeks.org/inheritance-in-c/?ref=lbp</a> (c++ syntax)  

**REAL LIFE EXAMPLE:**  Vehicle as the parent class and its different types (Car, Bike, Bus) as child classes.  
### Key Concepts/Advantages of Inheritance
- **Code Reusability**  
No need to rewrite `start()` in each child class.
- *Hierarchical Organization*
- **Easier Maintenance**:
  Changes made to a superclass automatically propagate to its subclasses, ensuring consistency and simplifying maintenance efforts
- **Method Overriding (Polymorphism)**  
If needed, child classes can override parent methods.

- While inheritance does NOT directly depend on encapsulation, encapsulation can control how inherited members are accessed using access modifiers (private, protected, public).  
✅ Encapsulation helps restrict access to data in an inherited class  
✅ Inheritance allows reusing code while encapsulation ensures data protection

## Encapsulation 
a process of wrapping code and data together into a single unit  
facilitates data hiding in C++ by using  access specifiers  

<!--> <a>https://www.tpointtech.com/encapsulation-in-java</a>
<a>http://geeksforgeeks.org/encapsulation-in-cpp/?ref=lbp</a>  
<a>https://www.sitesbay.com/java/java-encapsulation</a>

- we use **Access Specifiers** (especially c++)
- in java we can also use **getter** and **setter** methods 
*Real life example* : the phn is a capsule that is encapsulated ([as explained in mock](https://stackoverflow.com/questions/12072980/encapsulation-vs-abstraction-real-world-example)) ,bank account (javatpoint)
A bank application forbids (restrict) a client to change an Account's balance. 

_**Advantages:**_ (gfg)  

- Encapsulation also leads to abstraction
- Encapsulation is the combination of Data hiding and Abstraction

## Abstraction
Data abstraction is a way of hiding the implementation details and showing only the functionality to the users.  
- it shows only essential things to the user and hides the internal details.  
**_Real Life example:_** 1) sending SMS where we type the text and send the message. We do not know the internal processing about the message delivery.  
  2) bike , honda example (chk javatpoint with code.  
  3) header files in c++        
_How to achieve :_     
1) C++  --> Access specifiers and header files  
2) JAVA --> Interfaces and Abstract classes

#### Example of Abstract Class in Java
```java
abstract class Bike {
    abstract void run();  // abstract method
}

class Honda extends Bike {
    void run() {
        System.out.println("running safely");
    }
}
```
(bike class is with default access modifier 😊)   
<a>https://www.tpointtech.com/abstract-class-in-java</a>  

- Encapsulation is one way to achieve abstraction in object-oriented programming — especially in Java, C++, etc.
- A method which is declared as abstract and does not have implementation is known as an abstract method.
- Abstract classes **cannot be instantiated directly**.
- ensures that subclasses provide necessary functionality.
-  define a common interface for a group of related classes, ensuring consistency in their structure and behavior.  

[Diff b/w encapsulation and abstraction](https://www.geeksforgeeks.org/difference-between-abstraction-and-encapsulation-in-c/?ref=lbp)

## Interface in java 
<a>https://www.tpointtech.com/interface-in-java/<a>

#### Abstract Class vs Interface in Java

Here’s a side-by-side table to help you quickly understand the differences:

| Feature              | Abstract Class                                                                                          | Interface                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| **Keyword Used**     | `abstract class`                                                                                        | `interface`                                                                                    |
| **Method Implementation** | Can have both abstract and non-abstract methods                                                   | Only abstract methods (until Java 7), From Java 8 onwards, can have default and static methods |
| **Variables**        | Can have instance variables                                                                             | Only public static final (constants)                                                           |
| **Constructor**      | Yes, can have constructors                                                                              | ❌ No constructors                                                                              |
| **Inheritance Type** | Supports single inheritance                                                                             | Supports multiple inheritance (via multiple interfaces)                                        |
| **Usage**            | When you want to share code (partial implementation)                                                    | When you just want to define method signatures                                                 |
| **Access Modifiers** | Methods can be private, protected, etc.                                                                 | All methods are implicitly public abstract                                                     |
| **Example**          | `abstract class Animal { void breathe(){}; abstract void sound(); }`                                    | `interface AnimalInterface { void breathe(); void sound(); }`                                   |


## Polymorphism

Bike obj = new Honda(); (as used in above example in javatpoint)  
_What’s Happening Here?_  
You're creating an object of the child class Honda, but referencing it using the parent class type Bike.  
This is known as polymorphism — specifically, upcasting.  

### Differences

| Aspect                              | Java                                                                                                                                   | C++                                                                                      |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Polymorphism                        | <img src="https://github.com/user-attachments/assets/f33cf150-04d5-4efc-ac24-23c8ccc8b391" width="300">                                | <img src="https://github.com/user-attachments/assets/ce6cc5d6-10dd-40bb-b5a1-fe7038a6cf90" width="300"> |
| More Info                           | [Polymorphism in Java](https://www.tpointtech.com/polymorphism-in-java)                                                                | [Polymorphism in C++](https://www.geeksforgeeks.org/cpp-polymorphism/?ref=lbp)           |
| Operator Overloading                | Java does not have operator overloading                                                                                               | Supported                                                                                 |
| Runtime Polymorphism                | `@override`                                                                                                                           | `virtual`                                                                                 |

## 🚩 OOPS Pillars Comparison Table (with Real-Life Remote Example)

| Pillar        | Definition                                                   | Key Concept                  | Java Example                                             | Real-Life Example (Remote Control)                                                                 |
|---------------|---------------------------------------------------------------|------------------------------|----------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| **Encapsulation** | Wrapping data & methods into a single unit (class); restrict direct access to data | Data hiding                  | `private int volume; public int getVolume()`              | Volume or battery level is hidden inside the remote, accessed via buttons (not directly touched)   |
| **Abstraction**   | Hiding internal complexity, showing only relevant details to the user               | Hides how, shows what        | `abstract class Remote { abstract void powerOn(); }`     | You press the "Power" button, no need to know internal circuit working                             |
| **Inheritance**   | One class acquires properties/methods of another                                     | Code reuse                   | `class TVRemote extends Remote`                           | A TV remote and AC remote share common features like powerOn, volumeUp — inherited from base Remote|
| **Polymorphism**  | Same method behaves differently based on context                                     | Same name, many forms        | `Remote r = new TVRemote(); r.powerOn();`                 | powerOn() works differently for TV and AC remotes — one starts TV, the other turns on AC 
