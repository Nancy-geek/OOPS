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
- **_C++:_**  
Uses the **new** keyword to allocate memory on the heap and the **delete** keyword to free it.  
- **_Java:_**  
Uses the new keyword to allocate memory for objects on the heap.

## 2. ACCESS SPECIFIERS
- default (java)
- public
- private
- protected  
<a>https://www.tpointtech.com/access-modifiers-in-java</a>

## 3. Structure and Class
<a>(https://www.geeksforgeeks.org/structure-vs-class-in-cpp/)</a>

# 🚩 Constructor and Destructor   
(chk rohit negi notes above for better theory)  
- special function with no return type 
- automatically called
- never be static
- name same as of class

## Types : ##
- DEFAULT
- PARAMETRISED
- COPY

