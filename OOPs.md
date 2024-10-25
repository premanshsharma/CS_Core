# Mind Map of oops:-
- Introduction
  - What is Object-oriented programming
  - Advantages
  - Disadvantages

# Introduction
## Mind Map:-
- What is Object-oriented programming
- Advantages
- Disadvantages
## 1. What is object-oriented programming
- Object-oriented programming is about creating objects that contain both data and functions. 

### Advantages of oops
  1. Improved software-development productivity: Object-oriented programming is 
  modular, as it provides separation of duties in object-based program development. It 
  is also extensible, as objects can be extended to include new attributes and 
  behaviors. Objects can also be reused within and across applications. Because of 
  these three factors – modularity, extensibility, and reusability – object-oriented 
  programming provides improved software development productivity over traditional 
  procedure-based programming techniques.  
  2. Improved software maintainability: For the reasons mentioned above, object
  oriented software is also easier to maintain. Since the design is modular, part of the 
  system can be updated in case of issues without a need to make large-scale 
  changes.  
  3. Faster development: Reuse enables faster development. Object-oriented 
  programming languages come with rich libraries of objects, and code developed 
  during projects is also reusable in future projects.  
  4. Lower cost of development: The reuse of software also lowers the cost of 
  development. Typically, more effort is put into object-oriented analysis and 
  design, which lowers the overall cost of development.  
  5. Higher-quality software: Faster development of software and lower cost of 
  development allow more time and resources to be used in the verification of the 
  software. Although quality depends on the teams' experience,
object-oriented programming tends to result in higher-quality software.  

### Limitations of oops
  1. Steep learning curve: The thought process involved in object-oriented programming 
  may not be natural for some people, and it can take time to get used to it. It is 
  complex to create programs based on the interaction of objects. Some key 
  programming techniques, such as inheritance and polymorphism, can be 
  challenging to comprehend initially.  
  2. Larger program size: Object-oriented programs typically involve more lines of code 
  than procedural programs. 
  3. Slower programs: Object-oriented programs are typically slower than procedure
  based programs, as they typically require more instructions to be executed. 
  4. Not suitable for all types of problems: There are problems that lend themselves well 
  to functional-programming style, logic-programming style, or procedure-based 
  programming style, and applying object-oriented programming in those situations will 
  not result in efficient programs.

# Pillar of OOPS
## Mind Map:-
- Class
- Object
- Keywords
- Features
  - Polymorphism
  - Inheritance
  - Encapsulation
  - Abstraction
- Dynamic Binding
- Message Passing
## 1. Class
### Mind Map:-
- What is class
- Access Modifiers
  - Public
  - Private
  - Protected
  - Friend
    - Protected Friend
- Member Function
  - Simple Function
  - Static Function
  - Const Function
  - Inline Functions
  - Friend Functions
### 1.1 What is class
- Classes are a blueprint or a set of instructions to build a specific type of object.
- It determines how an object will behave and what the object will contain
### 1.2 Access Modifiers
- Access modifiers in Object-Oriented Programming (OOP) control the visibility of
class members (attributes and methods) to other parts of the program. 
#### 1.2.1 Public
- Accessible from anywhere in the program.
- Used when you want class members to be available globally.
#### 1.2.2 Private
- Accessible only within the class itself.
- Used to restrict access and encapsulate data.
#### 1.2.3 Protected
- Accessible within the class and by derived (subclass) classes.
- Used for inheritance while keeping data hidden from other classes.
#### 1.2.4 Friend
- Allows another class or function to access private and protected members of a class.
- It’s used for close relationships between classes.
##### 1.2.4.1 Protected Friend
- A combination of Protected and Friend. Members are accessible within the same assembly
(like Friend) and also by derived classes (like Protected).
### 1.3 Member Function
- Member functions are the functions, which have their declaration inside the class definition 
and work on the data members of the class. 
- The definition of member functions can be inside or outside the definition of class.
- If the member function is defined inside the class definition it can be defined directly,
but if it's defined outside the class, then we have to use the scope resolution :: operator
along with the class name and with function name.
- Example:-
```
class class_name
      {
          public:
          int variable_1;
          int function_1();
      }
      // member function defined outside class definition
      keyword return_type class_name :: function_name()
      {
          return 1;
      }
  ```
#### 1.3.1 Simple Function
- These are the basic member functions, which don't have any special keywords like static etc 
as prefixes. 
#### 1.3.2 Static Function
- A static function is a function that belongs to the class itself, not to any specific object.
This means:
  - It can be called without creating an object of the class.
  - You use the class name and the :: operator to call it (e.g., ClassName::staticFunction()).
  - Since it’s part of the class, not tied to an object, it can't access non-static members
    (like instance variables), but it can access other static variables or functions.
  - Static functions are useful for actions or utilities that are relevant to the class as a
    whole, not to individual objects.
#### 1.3.3 Const Function
- To declare a const function, you add const at the end of the function declaration.
- It can only be called on const objects or regular objects, but it cannot modify any 
member variables or call non-const functions.
#### 1.3.4 Inline Functions
- All the member functions defined inside the class definition are by default declared as Inline.
#### 1.3.5 Friend Functions
- A friend function is a special function that is not a member of a class but has permission to
access the class's private and protected members. It's used when an external function or another
class needs access to the internal details of a class.
- Declared using the friend keyword inside the class.
- It can be a regular function or a member function of another class.
- It breaks encapsulation to some extent but is useful when tight collaboration between two classes
or functions is needed.
```
class MyClass {
private:
    int value;

public:
    MyClass(int v) : value(v) {}

    // Declare the friend function
    friend void showValue(const MyClass& obj);
};

// Friend function definition
void showValue(const MyClass& obj) {
    std::cout << "Value: " << obj.value << std::endl;  // Can access private members
}
```
### 1.4 Constructor
- The name of the constructor is the same as its class name.
- Constructors are mostly declared in the public section of the class though they can be declared in the private section of the class.
- Constructors do not return values; hence they do not have a return type.
- A constructor gets called automatically when we create the object of the class.
#### 1.4.1 Types of Constructors Definition
##### 1.4.1.1 Defining the Constructor Within the Class
```
<class-name> (list-of-parameters) {
     // constructor definition
}
```
##### 1.4.1.2 Defining the Constructor Outside the Class
```
<class-name> {

    // Declaring the constructor
    // Definiton will be provided outside
    <class-name>();

    // Defining remaining class
}

<class-name>: :<class-name>(list-of-parameters) {
      // constructor definition 
}
```
#### 1.4.2 Types of Constructors
##### 1.4.2.1 Default Constructors
- A constructor that takes no parameters (or has all parameters with default values).
- Initializes objects with default values.
```
class MyClass {
public:
    MyClass() { // Default constructor
        // Initialization code
    }
};
```
##### 1.4.2.2 Parameterized Constructors
- A constructor that takes parameters to initialize an object with specific values.
- Allows customization of object creation.
```
class MyClass {
public:
    int value;
    MyClass(int v) { // Parameterized constructor
        value = v;
    }
};
```
##### 1.4.2.3 Copy Constructors
- A constructor that creates a new object as a copy of an existing object.
- Used to initialize one object with another object of the same class.
```
class MyClass {
public:
    int value;
    MyClass(const MyClass &obj) { // Copy constructor
        value = obj.value;
    }
};
```
- **Deep Copy vs Shallow Copy**
  - Shallow Copy
    - Creates a new object but does not create copies of the objects that the original object references. Instead, it copies the references (pointers) to those objects.
    - Both the original and the copied object share the same memory for the referenced objects.
    - If one object modifies the shared data, it affects the other object as well.
  - Deep Copy
    - Creates a new object and also creates copies of all objects referenced by the original object. Each object has a separate copy of the data.
    - Modifications to the copied object do not affect the original object.
- **Copy Constructor vs Assignment Operator**
  - Copy Constructor
    - Initializes a new object using an existing object of the same class.
    - Called when a new object is created as a copy of an existing object
      (e.g., when passing by value).
  -  Assignment Operator:-
    -  Used to copy the contents of one existing object to another existing object of the same class.
    - Called when using the assignment operator (=) to assign one object to another.
 
##### 1.4.2.4 Virtual Constructors
In C++, the constructor cannot be virtual, because when a constructor of a class is executed there is no virtual table in the memory, which means no virtual pointer defined yet. So, the constructor should always be non-virtual.

#### 1.4.3 Constructor Overloading
- Constructor overloading is a feature in C++ (and other object-oriented programming languages) that allows a class to have more than one constructor with different parameter lists. This enables the creation of objects in various ways, providing flexibility in how objects are initialized.
- Each constructor must have a different signature (i.e., a different number of parameters or different types of parameters).
- This allows the same class to be initialized with different sets of data.

### 1.5 Destructor
- A destructor is also a special member function like a constructor. Destructor destroys the class objects created by the constructor. 
- Destructor has the same name as their class name preceded by a tilde (~) symbol.
- It is not possible to define more than one destructor.
- The destructor is only one way to destroy the object created by the constructor. Hence, the destructor cannot be overloaded.
- It cannot be declared static or const.
- Destructor neither requires any argument nor returns any value.
- It is automatically called when an object goes out of scope. 
- Destructor releases memory space occupied by the objects created by the constructor.
- In destructor, objects are destroyed in the reverse of an object creation.
- **How to call destructors explicitly?** ```object_name.~class_name()```
- **When do we need to write a user-defined destructor?**
  - Default Destructor: The compiler provides a default destructor that works for simple cases.
  - Dynamic Memory: If the class has pointers to dynamically allocated memory, you need to write your destructor to release that memory.
  - Avoid Memory Leaks: Custom destructors prevent memory leaks by ensuring that all allocated resources are properly freed when the object is destroyed.
 
#### 1.5.1 Private Destructor
Whenever we want to control the destruction of objects of a class, we make the destructor private. For dynamically created objects, you may pass a pointer to the object to a function and the function deletes the object. If the object is referred after the function call, the reference will become dangling.
#### 1.5.2 Virtual Destructor
- Definition: A virtual destructor is declared with the virtual keyword in a base class. It allows derived classes to override the destructor while ensuring that the correct destructor is called when an object is deleted through a base class pointer.
- Purpose: The primary purpose of a virtual destructor is to ensure that the destructor of the derived class is called when an object is deleted, even if it is referenced by a base class pointer. This prevents resource leaks and ensures proper cleanup.
- Usage: Always declare the destructor of a base class as virtual when using polymorphism.
```
class Base {
public:
    virtual ~Base() { // Virtual destructor
        // Cleanup for Base
    }
};

class Derived : public Base {
public:
    ~Derived() override { // Overrides Base destructor
        // Cleanup for Derived
    }
};

int main() {
    Base* obj = new Derived();
    delete obj; // Calls Derived destructor first, then Base destructor
    return 0;
}
```
#### 1.5.3 Pure Virtual Destructor
- Definition: A pure virtual destructor is a virtual destructor that is declared with = 0 in the base class. It makes the base class abstract, meaning it cannot be instantiated directly.
- Purpose: It allows derived classes to provide their own implementation of the destructor while ensuring that the base class cannot be instantiated. This is useful when you want to define a common interface for all derived classes but do not want to allow the direct creation of base class objects.
- Implementation: Even though the destructor is pure virtual, you can still define for it outside the class, which is necessary for cleanup in derived classes.
```
class AbstractBase {
public:
    virtual ~AbstractBase() = 0; // Pure virtual destructor
};

AbstractBase::~AbstractBase() {
    // Optional: Cleanup for AbstractBase
}

class ConcreteDerived : public AbstractBase {
public:
    ~ConcreteDerived() override {
        // Cleanup for ConcreteDerived
    }
};

int main() {
    AbstractBase* obj = new ConcreteDerived();
    delete obj; // Calls ConcreteDerived destructor first
    return 0;
}
```
- **Differences Between Destructors and Normal Member Functions:**
  - Purpose: Destructors clean up resources when an object is destroyed, while normal member functions perform regular operations on the object.
  - Naming: Destructors are named with a tilde (~) followed by the class name (e.g., ~MyClass()), whereas normal member functions can have any valid name.
  - Invocation: Destructors are called automatically when an object goes out of scope or is deleted; normal member functions are called explicitly by the programmer.
  - Return Type: Destructors do not have a return type; normal member functions can have any return type.
- **Can There Be More Than One Destructor in a Class?**
  - No, a class can only have one destructor.
- **When Do We Need to Write a User-Defined Destructor?**
  - You need to write a user-defined destructor when your class manages resources that require explicit cleanup, such as dynamically allocated memory or file handles, to prevent memory leaks.
- **Can a Destructor Be Virtual? When to Use It?**
  - Yes, a destructor can be virtual. You should use a virtual destructor when you have a base class that will be inherited, ensuring the derived class's destructor is called correctly when an object is deleted through a base class pointer, preventing resource leaks.

### Questions
1. **Difference between structure and class**
- The most important of them is hiding implementation details.
- A structure will by default not hide its implementation details from whoever uses it in code,
while a class by default hides all its implementation details and will therefore by default
prevent the programmer from accessing them.
- Class is normally used for data abstraction and inheritance whereas structure is normally used
for the grouping of different datatypes.
#### When to use structure and class
- Use struct when:
  - You need a lightweight, simple data type.
  - Value semantics (copy by value) are preferred.
  - No inheritance or shared state is needed.
- Use class when:
  - You need reference semantics (shared objects).
  - Inheritance and polymorphism are required.
  - The object is complex or has large, mutable data.
