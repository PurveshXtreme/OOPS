![OOPs Interview Questions and Answers](https://media.geeksforgeeks.org/wp-content/uploads/20230314113535/OOPs-Interview-Questions-and-Answers.png)




- [Basics of OOPs](#basics-of-oops)  
- [Classes, Objects, and Memory](#classes-objects-and-memory)  
- [Core OOPs Principles (4 Pillars)](#core-oops-principles-4-pillars)  
- [Special Classes and Interfaces](#special-classes-and-interfaces)  
- [Constructors and Destructors](#constructors-and-destructors)  
- [Functions and Polymorphism](#functions-and-polymorphism)  

----
----

### Basics of OOPs

### Q: What is Object-Oriented Programming (OOPs), how does it differ from other paradigms, which languages support it, what are its advantages/disadvantages, and what are its main features?

**A:**  

Object-Oriented Programming (OOPs) is a programming paradigm where software is structured as a collection of **objects**.  
- Each object represents a real-world entity with **data (attributes)** and **methods (functions)** that operate on that data.  
- OOP helps in building modular, reusable, and maintainable code for large-scale systems.  

---

#### 🔹 Difference from Other Programming Paradigms

![OOP Concepts Overview](https://media.geeksforgeeks.org/wp-content/uploads/20250425104200593184/oops.png)

OOPs is not the only paradigm. Some alternatives include:  

1. **Imperative Programming** – Focuses on step-by-step instructions that change program state.  
   - *Example:* Procedural Programming (functions, routines).  
   - *Example:* Parallel Programming (dividing tasks to run concurrently).  

2. **Declarative Programming** – Focuses on *what* to do, not *how* to do it.  
   - **Logical Programming:** Uses facts and rules (e.g., Prolog).  
   - **Functional Programming:** Builds programs by composing functions (e.g., Haskell).  
   - **Database Programming:** Uses queries to manage structured data.  

👉 OOP differs because it models real-world problems as interacting **objects** with state and behavior.

---

#### 🔹 Common OOP Languages
Some widely used languages that follow OOP principles are:  
- **C++**  
- **Java**  
- **Python**  
- **JavaScript**  
- **C#**  
- **Ruby**

---

#### 🔹 Advantages of OOPs
- ✅ **Reusability:** Code reuse through inheritance and polymorphism.  
- ✅ **Maintainability:** Easier updates and modifications.  
- ✅ **Security:** Data hiding via encapsulation.  
- ✅ **Scalability:** Works well for large, complex systems.  
- ✅ **Flexibility:** Easier to redesign and extend.  

---

#### 🔹 Disadvantages of OOPs
- ❌ Requires developers to think in terms of objects, which may not be intuitive.  
- ❌ More **planning and design effort** needed.  
- ❌ Not suitable for every problem domain.  
- ❌ Programs can become larger compared to procedural approaches.  

---

#### 🔹 Main Features of OOP (4 Pillars)
1. **Encapsulation** – Binding data and methods together while restricting direct access.  
2. **Abstraction** – Showing only essential details, hiding implementation.  
3. **Polymorphism** – Ability of methods/functions to behave differently based on context.  
4. **Inheritance** – Deriving new classes from existing ones to promote reusability.  

---
---

### Classes, Objects, and Memory

### 7. What is a Class?
A **class** is the fundamental building block of Object-Oriented Programming.  
It is a **user-defined data type** that encapsulates:
- **Data members** (variables, attributes, properties)  
- **Member functions** (methods, behaviors, operations)  

A class serves as a **blueprint or template** from which multiple objects can be created.  
Objects created from the same class share a similar structure but may hold **different values** for their attributes.

✅ Example in C++:
```cpp
class Car {
public:
    string brand;
    int speed;

    void drive() {
        cout << brand << " is driving at " << speed << " km/h" << endl;
    }
};
```

---

### 8. What is an Object?
An **object** is an **instance of a class**.  
- It is a real-world entity that has a **state** (data/attributes) and **behavior** (functions/methods).  
- To access a class’s members, we first need to create an object of that class.  

✅ Example:
```cpp
Car myCar;         // Object creation
myCar.brand = "Tesla";
myCar.speed = 120;
myCar.drive();     // Output: Tesla is driving at 120 km/h
```
---
### 20. How much memory does a Class occupy?
- A **class itself does not occupy memory**. It only defines the **structure** and **behavior** of objects.  
- Memory is allocated **only when an object is created** from the class.  
- The memory consumed by an object depends on:
  - The **size of its data members**.  
  - Any **memory alignment/padding** done by the compiler.  

👉 Example:  
```cpp
class Example {
    int x;    // 4 bytes
    double y; // 8 bytes
};
```

---

### 21. Is it always necessary to create objects from a class?
- **No**, it is not always necessary.  
- If a class contains **static members or static methods**, they can be accessed **directly using the class name** without creating an object.  

✅ Example:
```cpp
class MathUtils {
public:
    static int square(int n) {
        return n * n;
    }
};

int result = MathUtils::square(5);  // No object needed
//However, if you want to access non-static members, you must create an object.
```
---
### 22. What is the difference between a structure and a class in C++?

| Feature | Structure (`struct`) | Class (`class`) |
|---------|----------------------|-----------------|
| **Default Access Modifier** | Members are **public** by default | Members are **private** by default |
| **Declaration Keyword** | Declared using `struct` | Declared using `class` |
| **Use Case** | Traditionally used for **grouping simple data** | Used for **modeling complex entities** with both data & behavior |
| **Inheritance** | Supports inheritance but rarely used for it | Fully supports inheritance and polymorphism |
| **Encapsulation** | Less commonly used for encapsulation | Strongly supports encapsulation |

✅ Example:
```cpp
struct Point {
    int x, y;   // public by default
};

class Rectangle {
private:
    int length, width;  // private by default

public:
    void setDimensions(int l, int w) {
        length = l;
        width = w;
    }
    int area() {
        return length * width;
    }
};
```

---
---




