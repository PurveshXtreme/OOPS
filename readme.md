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
- A class is a building block of Object-Oriented Programs.
- It is a user-defined data type that contains the data members and member functions that operate on the data members.
- It is like a blueprint or template of objects having common properties and methods.

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

### Core OOPs Principles (4 Pillars)

### 10. What is Encapsulation?
![Encapsulation](https://media.geeksforgeeks.org/wp-content/uploads/20230119164955/encapsulation.png)

Encapsulation is the process of **binding data and methods that operate on that data into a single unit**.  
It ensures that sensitive data is hidden from external users and can only be accessed through controlled interfaces.  

#### Key Implementations:
- **Data Hiding**: Restricting access to members of an object using access specifiers like `private` and `protected` in C++.  
- **Bundling Data & Methods Together**: Data members and the functions operating on them are wrapped into a single unit called a **class**.  

---

### 11. What is Abstraction?
![Abstraction](https://media.geeksforgeeks.org/wp-content/uploads/20230125135240/abstraction.png)

Abstraction is the concept of **showing only the necessary information** while hiding the implementation details.  
It focuses on **what a system does** rather than **how it does it**.  

#### Implementation in OOP:
- **Classes**: Hide the implementation details and provide a clean interface.  
- **Interfaces & Abstract Classes**: Define contracts without exposing internal logic.  

---

### 12. What is Inheritance? What is its purpose?
Inheritance is the process where a class (**child/derived class**) acquires properties and behaviors (data & methods) from another class (**parent/base class**).  

- The derived class can reuse and extend the functionality of the base class.  
- The **main purpose of inheritance** is:
  - **Code reusability**  
  - Achieving **runtime polymorphism**  

---

### 13. What is Polymorphism? What are its types?
![Polymorphism](https://media.geeksforgeeks.org/wp-content/uploads/20250425165615062960/polymorphism.png)

The term **Polymorphism** means *"many forms"*.  
It allows the same function, operator, or method to behave differently depending on the context.  

#### Types of Polymorphism:
1. **Compile-Time Polymorphism (Static/Early Binding)**  
   - Binding of function call is resolved at compile time.  
   - Examples:  
     - **Function Overloading**  
     - **Operator Overloading**  

2. **Runtime Polymorphism (Dynamic/Late Binding)**  
   - Actual implementation is determined at runtime.  
   - Example:  
     - **Function Overriding** using virtual functions in C++.  

---

### 16. Are there any limitations of Inheritance?
Although inheritance is powerful, it comes with drawbacks:  
- **Slower Execution**: Since it may involve multiple classes, execution time can increase.  
- **Tight Coupling**: Child and parent classes are closely linked; changes in the base class may affect derived classes.  
- **Complex Implementation**: Misuse of inheritance can lead to unexpected errors or incorrect outputs.  

---

### 17. What are the different types of Inheritance?
![Types of Inheritance](https://media.geeksforgeeks.org/wp-content/uploads/20240730171935/Types-of-inheritance.webp)

Inheritance can be classified into **five types**:

1. **Single Inheritance**  
   - A child class derives directly from one base class.  

2. **Multiple Inheritance**  
   - A child class derives from more than one base class.  

3. **Multilevel Inheritance**  
   - A child class derives from a class which itself is derived from another base class.  

4. **Hierarchical Inheritance**  
   - Multiple child classes derive from a single base class.  

5. **Hybrid Inheritance**  
   - A combination of two or more types of inheritance.  

> ⚠️ Note: Support for inheritance types depends on the programming language.  
> Example: **Java does not support multiple inheritance** directly, but allows it through interfaces.


---
---

### Special Classes and Interfaces

### 18. What is an Interface?
- An **interface** is a unique class type that contains **method declarations but not their definitions**.  
- Inside an interface, only method declarations are permitted.  
- You cannot create objects of an interface. Instead, the interface must be **implemented by a class**, which provides the method definitions.  

---

### 19. How is an Abstract Class different from an Interface?

Both **abstract classes** and **interfaces** are special types of classes that include **method declarations without implementations**. However, they differ in important ways:

| **Abstract Class** | **Interface** |
|---------------------|---------------|
| Can have **both abstract and non-abstract methods** | Can have **only abstract methods** |
| Can contain **final, non-final, static, and non-static variables** | Can only contain **static and final variables** |
| Does **not support multiple inheritance** | **Supports multiple inheritance** |

---

### 30. What is an Abstract Class?
- An **abstract class** is a class that is designed to be used for **inheritance** and **cannot be instantiated** directly.  
- It can contain **both abstract and non-abstract methods**.  
- Purpose: To provide a **base class** with common functionality that other classes can inherit and extend.  

#### Language-Specific Notes:
- **C++:** An abstract class is a class that contains **at least one pure virtual function**.  
- **Java & C#:** Declared using the `abstract` keyword.  
- **Python:** Uses the **ABC (Abstract Base Class)** module to create an abstract class.  

#### Example in C++:
```cpp
class absClass {
public:
    virtual void pvFunc() = 0; // Pure virtual function
};
```

---
---

### Constructors and Destructors

### 23. What is a Constructor?
- A **constructor** is a block of code that initializes a newly created object.  
- It looks like an instance method but **is not a method**, since it has **no return type**.  
- Usually, it has the same name as the class.  
#### Language Specifics:
- **Python:** Constructor is named `__init__`.  
- **C++ & Java:** Constructor has the same name as the class.  
#### Example in C++:
```cpp
class base {
public:
    base() { cout << "This is a constructor"; }
};
```

### 24. What are the Various Types of Constructors in C++?
Constructors in C++ are commonly classified into:
- Default Constructor
- Non-Parameterized Constructor
- Parameterized Constructor
- Copy Constructor

#### 1. Default Constructor
- A constructor that doesn't take any arguments.
- Automatically created by the compiler if no constructor is defined.
- Initializes members to default values.

#### 2. Non-Parameterized Constructor
- A user-defined constructor with no arguments.
- Example:
```cpp
class base {
public:
    base() {
        cout << "This is a non-parameterized constructor";
    }
};
```

#### 3. Parameterized Constructor
- A constructor that accepts arguments to initialize members.
- Example:
```cpp
class base {
public:
    int data;
    base(int var) {
        cout << "Constructor with argument: " << var;
    }
};
```

#### 4. Copy Constructor
- Initializes an object using another object of the same class.
- Example:
```cpp
class base {
    int a, b;
public:
    // copy constructor
    base(base& obj) {
        a = obj.a;
        b = obj.b;
    }
};
```
- **Python:** No built-in copy constructor, but it can be mimicked using methods like `copy.copy()` or custom implementation.

### 25. What is a Destructor?
- A **destructor** is a special method called automatically when an object goes out of scope or is destroyed.
#### Language Specifics:
- **C++:** Destructor name = class name prefixed with `~`.
- **Python:** Destructor is defined using `__del__`.
- **Java:** No destructor (garbage collector handles cleanup).
  - `finalize()` was used earlier but is deprecated since Java 9.
#### Example in C++:
```cpp
class base {
public:
    ~base() { cout << "This is a destructor"; }
};
```

### 26. Can we Overload the Constructor in a Class?
✅ **Yes**, constructors can be overloaded in a class.
- This is called **Constructor Overloading**.
- Multiple constructors with different parameters (number or type).

### 27. Can we Overload the Destructor in a Class?
❌ **No**, a destructor cannot be overloaded in a class.
- A class can have only one destructor.

---
---

### Functions and Polymorphism

### 15. Difference Between Overloading and Overriding
- **Overloading**  
  - A **compile-time polymorphism** feature.  
  - Allows multiple methods or operators with the same name but **different parameter lists** (number or type of parameters).  
  - Example: Method Overloading, Operator Overloading.  
- **Overriding**  
  - A **runtime polymorphism** feature.  
  - Allows a derived class to provide a **different implementation** of a method that already exists in the base class.  
  - Implemented using **virtual functions** (in C++).  

---

### 28. Friend Functions and Friend Classes
- **Friend Function**  
  - A special function that is **not a member** of a class but has access to the class's **private** and **protected** members.  
  - Declared by using the `friend` keyword inside the class.  
  **Example:**
  ```cpp
  class Base {
      int data;
      friend void showData(Base& obj);  // Friend function
  };
  ```

#### Friend Class
- A class declared as a friend inside another class.
- The friend class has access to the private and protected members of the class in which it is declared.
- Example:
```cpp
class A {
    friend class B;  // B can access private members of A
};
```

### 29. Virtual and Pure Virtual Functions
#### Virtual Function
- A function in a base class that can be overridden in a derived class.
- Enables runtime polymorphism.
- Declared using the `virtual` keyword in C++.
#### Language Specifics:
- **C++/C#:** Use `virtual` keyword.
- **Java:** All non-static, non-final public methods are virtual by default.
- **Python:** All methods are virtual by default.
#### Example:
```cpp
class Base {
public:
    virtual void print() {
        cout << "This is a virtual function";
    }
};
```

#### Pure Virtual Function
- A virtual function that has no implementation in the base class.
- Declared by assigning `= 0` in C++.
- Makes the class abstract (cannot be instantiated).
#### Example:
```cpp
class Base {
public:
    virtual void pureVirFunc() = 0;  // Pure Virtual Function
};
```
#### In Python:
- Achieved using `@abstractmethod` from the ABC (Abstract Base Class) module.

---
---

