# OOPS 

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

## . Structure and Class
<a>(https://www.geeksforgeeks.org/structure-vs-class-in-cpp/)</a>

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
Explicitly triggered using System.gc() (not guaranteed to run immediately)

## SHALLOW COPY V/S DEEP COPY  
<a>https://www.tpointtech.com/shallow-copy-vs-deep-copy-in-java </a> (for java especially)    
<!--> <a>https://www.geeksforgeeks.org/difference-between-shallow-and-deep-copy-of-a-class/</a> 
 just asse hi when reading the article -(In Java, primitive data types are basic building blocks of data that store simple values directly in memory. They are not objects and are more efficient in terms of memory and performance.)  

## Important Keywords
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

# Features of OOPs :
- Polymorphism
- Inheritance
- Encapsulation
- Abstraction

##   Inheritance  
**java**- (extends keyword)  class derived extends base{...    
**c++** - class Derived : public Base{ ...  
_**Types :**_  
- Single  
- Mutliple (not in java (diamond problem), supported via interfaces )    
- Hierarchical  
- Multilevel  
- Hybrid / Virtual (not in java, supported via interfaces)    
  <a>https://www.tpointtech.com/inheritance-in-java</a> (java syntax and theory)    
  <a>https://www.geeksforgeeks.org/inheritance-in-c/?ref=lbp</a> (c++ syntax)  

**REAL LIFE EXAMPLE:**  Vehicle as the parent class and its different types (Car, Bike, Bus) as child classes.  
### Key Concepts in Inheritance
- **Code Reusability**  
No need to rewrite `start()` in each child class.
- **Parent-Child Relationship**  
Car and Bike inherit properties from Vehicle.
- **Method Overriding (Polymorphism)**  
If needed, child classes can override parent methods.

- While inheritance does NOT directly depend on encapsulation, encapsulation can control how inherited members are accessed using access modifiers (private, protected, public).  
✅ Encapsulation helps restrict access to data in an inherited class  
✅ Inheritance allows reusing code while encapsulation ensures data protection



