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
  4. Not suitable for all types of problems: Some problems lend themselves well 
  to functional-programming style, logic-programming style, or procedure-based 
  programming style, and applying object-oriented programming in those situations will 
  not result in efficient programs.

# Pillar of OOPS
## Mind Map:-
- Class and Object
- Keywords
- Features
  - Polymorphism
  - Inheritance
  - Encapsulation
  - Abstraction
- Dynamic Binding
- Message Passing
## 1. Class and Object
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
### 1.1 What is class and Object
- Classes are a blueprint or a set of instructions to build a specific type of object.
- It determines how an object will behave and what the object will contain
- **Object** is an instance of a class, Object is a physical entity whereas class is a logical entity. 
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


## 2. Keywords
### Mindmap:- 
- Static
- Virtual
- Abstract Keyword
- Final Keyword
- Explicit Keyword
- this keyword
- new keyword
- const keyword
- super keyword
- sealed keyword
### 2.1 Static
- Meaning: The static keyword means that a variable or function belongs to the class itself rather than to any specific object of the class.
- Usage: It is used to create shared data or methods that can be accessed without creating an instance of the class.
### 2.2 Virtual
- Meaning: The virtual keyword is used in a base class to indicate that a method can be overridden in derived classes.
- Usage: It allows for dynamic (run-time) polymorphism, ensuring the correct method is called for an object, even when accessed through a base class pointer.
### 2.3 Abstract Keyword
- Meaning: The abstract keyword is used to define a class that cannot be instantiated and may contain abstract methods (methods without a body).
- Usage: It sets up a blueprint for derived classes to implement specific functionalities.
### 2.4 Final Keyword
- Meaning: The final keyword is used to prevent a class from being subclassed or to prevent a method from being overridden in derived classes.
- Usage: It enforces that no further modifications can be made to a class or method.
### 2.5 Explicit Keyword
- Meaning: The explicit keyword is used to prevent implicit conversions from one type to another for single-argument constructors.
- Usage: It helps avoid unintentional type conversions that can lead to bugs.
### 2.6 this keyword
- Meaning: The this keyword refers to the current object instance within a class.
- Usage: It is used to access members of the current object, particularly when there is a naming conflict with parameters.
### 2.7 new keyword
- Meaning: The new keyword is used to dynamically allocate memory for an object or array in heap memory.
- Usage: It allows you to create objects at runtime rather than at compile time.
### 2.8 const keyword
- Meaning: The const keyword is used to declare that a variable's value cannot be changed after it is initialized.
- Usage: It helps in protecting data from being modified, which can prevent errors.
### 2.9 super keyword
- Meaning: The super keyword refers to the superclass (parent class) of the current object.
- Usage: It is used to call methods or access members from the parent class, especially when overriding methods in a derived class.
### 2.10 sealed keyword
- Sealed is the keyword if we want to stop inheritance then we use Seale before class & for stopping overriding we use Sealed before the method.
## 3. Features of OOPs
### 3.1 Polymorphism
- Polymorphism is derived from 2 Greek words: poly and morphs. The word "poly" means many and "morphs" means forms. So polymorphism means many forms.
- It refers to the ability of different classes to respond to the same method call in different ways
- You can overload functions across namespaces.
- **Why to use polymorphism**
  - Flexibility and Reusability: It allows developers to write more generic and reusable code.
  - Ease of Maintenance: Changes in the implementation of a class do not affect the classes that use its interface.
- **Functions that cannot be overloaded**
  - Function declarations that differ only in the return type.
  - Member function declarations with the same name and the name parameter-type list cannot be overloaded if any of them is a static member function declaration.
    - ![image](https://github.com/user-attachments/assets/c16042a8-ebcf-43a3-b5bc-3b224137ca87)
  - Parameter declarations that differ only in a pointer * versus an array [] are equivalent. That is, the array declaration is adjusted to become a pointer declaration. Only the second and subsequent array dimensions are significant in parameter types.
    - ![image](https://github.com/user-attachments/assets/0e835450-1e61-4787-afc8-0a6ef37f6065)
  - Parameter declarations that differ only in that one is a function type and the other is a pointer to the same function type are equivalent.
    - ![image](https://github.com/user-attachments/assets/85e54535-94f9-4efe-bb1a-36a5300b6470)
  - Parameter declarations that differ only in the presence or absence of const and/or volatile are equivalent. That is, the const and volatile type-specifiers for each parameter type are ignored when determining which function is being declared, defined, or called.
    - ![image](https://github.com/user-attachments/assets/e517722c-b92a-4424-a621-79419d250eb6)
  - Two parameter declarations that differ only in their default arguments are equivalent.
    - ![image](https://github.com/user-attachments/assets/b47aa8c1-a5fc-4e90-9653-8b41c0b0e884)

#### Mind Map
- Types
  - Compile Time 
    - Method Overloading
    - Operator Overloading
  - Run time
    - Method Overriding
- Virtual Function
- Virtual Class
- Derived Class
- Can virtual functions be set to private
- Inline virtual function
- Abstract Class
- Pure Virtual Function
- Pure Virtual Destructor

#### 3.1.1 Types of Polymorphism
#### 3.1.1.1 Compile time polymorphism (static binding)
- This type is resolved during compile time. It includes:
##### 3.1.1.1.1 Method Overloading: 
- Multiple methods with the same name but different parameters (different types or number of parameters).
##### 3.1.1.1.2 Operator Overloading: 
- Customizing the behavior of operators for user-defined types.
#### 3.1.1.2 Run time polymorphism (dynamic binding)
- This type is resolved during runtime and is typically achieved through:
- **Method Overriding:** A derived class provides a specific implementation of a method already defined in its base class.
#### 3.1.2 Virtual Function
- It belongs to the base class.
- It is used to tell the compiler to perform **dynamic linkage or late binding** on the function.
- When the function is made virtual, C++ determines which function is to be invoked at the runtime based on the type of the object pointed by the base class pointer.
- **Rules of virtual function**
  - Virtual functions must be members of some class.
  - Virtual functions cannot be static members.
  - They are accessed through object pointers.
  - They can be a friend of another class.
  - A virtual function must be defined in the base class, even though it is not used.
  - The prototypes of a virtual function of the base class and all the derived classes must be identical. If the two functions with the same name but different prototypes, C++ will consider them as overloaded functions.
  - We cannot have a virtual constructor, but we can have a virtual destructor
#### 3.1.3 Virtual Class
- Need for Virtual Base Classes: Consider the situation where we have one class A. This class A is inherited by two other classes B and C. Both these classes are inherited into another in a new class D as shown in the figure below. 
![Need-of-Containership-in-C](https://github.com/user-attachments/assets/28eb8ca7-1422-4f81-8b62-24a0696ec3e0)
- As we can see from the figure the data members/function of class A are inherited twice by class D. One through class B and second through class C. When any data / function member of class A is accessed by an object of class D, ambiguity arises as to which data/function member would be called. One is inherited through B or the other is inherited through C. This confuses the compiler and it displays an error.
- To resolve this ambiguity when class A is inherited in both class B and class C, it is declared as a virtual base class by placing a keyword virtual as :
```
Syntax 1:
class B : virtual public A 
{
};
Syntax 2:
class C : public virtual A
{
};
```
- Virtual can be written before or after the public. Now only one copy of the data/function member will be copied to class C and class B and class A becomes the virtual base class. Virtual base classes offer a way to save space and avoid ambiguities in class hierarchies that use multiple inheritances. When a base class is specified as a virtual base, it can act as an indirect base more than once without duplication of its data members. A single copy of its data members is shared by all the base classes that use the virtual base.
#### 3.1.4 Derived Class
- A derived class is a class created or derived from another existing class. The existing class from which the derived class is created through the process of inheritance is known as a base class or superclass.
- Derived classes are used for augmenting the functionality of the base class by adding or modifying the properties and methods to suit the requirements of the specialization necessary for the derived class. This allows for defining virtual methods that form the means to implement polymorphism, which allows a group of objects to work uniformly. Thus, the inherent advantages of inheritance and polymorphism like code reuse, faster development, easy maintenance, etc., are realized.
- A derived class is also known as a subclass or child class.
#### 3.1.5 Can virtual functions be set to private
- Yes, virtual functions can be set to private in C++. However, even though the function is marked as private, it can still be overridden by derived classes. The key point is that derived classes cannot directly call the private virtual function from the base class, but they can provide their own implementation of the function.
 ```
  #include <iostream>
using namespace std;

class Base {
private:
    virtual void show() {  // Private virtual function
        cout << "Base class private function" << endl;
    }

public:
    void callShow() {
        show();  // Can be called within the class
    }
};

class Derived : public Base {
private:
    void show() override {  // Overriding the private virtual function
        cout << "Derived class function" << endl;
    }

public:
    void callDerivedShow() {
        show();  // Can be called within the derived class
    }
};

int main() {
    Base* obj = new Derived();  // Base pointer to Derived object
    obj->callShow();  // Output: Derived class function (because of polymorphism)

    // obj->show();  // ERROR: 'show' is a private member of 'Base'

    delete obj;
    return 0;
}

  ```
#### 3.1.6 Inline virtual function
- Virtual Function: Enables dynamic polymorphism by resolving the correct function at runtime via a vtable.
- Inline Function: Replaces the function call with its body at compile-time to optimize performance.
- Conflict:
  - Virtual functions are resolved at runtime, while inline functions are intended for compile-time optimization.
  - The compiler can't inline virtual function calls when they use pointers/references, as the exact function is unknown until runtime.
  - However, the compiler may inline the function if the object type is known at compile-time (i.e., direct object calls, not via pointers/references).
```
class Base {
public:
    virtual inline void show() { cout << "Base class"; }
};

class Derived : public Base {
public:
    inline void show() override { cout << "Derived class"; }
};

Base obj; obj.show();  // May inline
Base* objPtr = new Derived(); objPtr->show();  // Unlikely to inline (vtable)

  ```
#### 3.1.7 Abstract Class
- An abstract class in object-oriented programming is a class that cannot be instantiated on its own and is designed to be a blueprint for other classes. It typically contains one or more abstract methods (methods without implementation) that must be overridden in derived classes.
```
class Shape {
public:
    virtual void draw() = 0;  // Pure virtual function (abstract)
};

class Circle : public Shape {
public:
    void draw() override {  // Implementing abstract method
        cout << "Drawing Circle" << endl;
    }
};
```
```
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def draw(self):
        pass

class Circle(Shape):
    def draw(self):
        print("Drawing Circle")

# shape = Shape()  # ERROR: Cannot instantiate abstract class
circle = Circle()  # OK
circle.draw()  # Output: Drawing Circle

```
#### 3.1.8 Pure Virtual Function
- When the function has no definition, such function is known as a "do-nothing" function.
- The "do-nothing" function is known as a pure virtual function. A pure virtual function is a function declared in the base class that has no definition relative to the base class.
- A class containing the pure virtual function cannot be used to declare the objects of its own, such classes are known as abstract base classes.
- The main objective of the base class is to provide the traits to the derived classes and to create the base pointer used for achieving the runtime polymorphism.
- Pure virtual function can be defined as:
```virtual void display() = 0;```   
#### 3.1.9 Pure Virtual Destructor
- Purpose: It enforces that the class is abstract (can't instantiate the base class) while ensuring the correct destruction of derived class objects.
- Definition: You must still provide an implementation for a pure virtual destructor, unlike other pure virtual functions.
### 3.2 Inheritance
- Inheritance allows us to use one class (derived class) to inherit properties and behaviors (methods) from another class (base class). It promotes code reuse and establishes a relationship between classes.
- **Terms used in Inheritance**
  - Class: A class is a group of objects which have common properties. It is a template or blueprint from which objects are created.
  - Sub Class/Child Class: Subclass is a class which inherits the other class. It is also called a derived class, extended class, or child class.
  - Super Class/Parent Class: Superclass is the class from where a subclass inherits the features. It is also called a base class or a parent class.
  - Reusability: As the name specifies, reusability is a mechanism which facilitates you to reuse the fields and methods of the existing class when you create a new class. You can use the same fields and methods already defined in the previous class.
- **Why we need inheritance**
  - Code Reusability: Allows sharing of common functionality across multiple classes without rewriting code.
  - Maintainability: Changes in the base class automatically reflect in all derived classes, making updates easier.
  - Extensibility: Enables adding new features to derived classes without modifying existing code in the base class.
  - Hierarchical Classification: Models real-world relationships by creating a natural hierarchy between general and specific objects.
  - Polymorphism: Facilitates dynamic method overriding, allowing derived classes to modify base class behavior at runtime.
- **Limitations of Inheritance**
- Tight Coupling: Inheritance creates a strong dependency between base and derived classes, making changes in the base class potentially affect all derived classes.
- Fragile Base Class Problem: Modifying the base class can inadvertently break functionality in derived classes.
- Reduced Flexibility: Inheritance locks classes into a hierarchy, limiting flexibility and making future changes harder to implement.
- Increases Complexity: Deep inheritance hierarchies can make code harder to understand, debug, and maintain.
- Inappropriate Use: Overuse or misuse of inheritance, when composition would be better, can lead to rigid and inefficient designs.
- Single Inheritance Limitation: Languages like Java only support single inheritance, limiting class extension from multiple base classes. (Multiple inheritance in C++ can be complex to manage).
- **Sealed keyword**
  - Sealed is the keyword if we want to stop inheritance then we use Seale before class & for stopping overriding we use Sealed before the method.

#### 3.2.1 Types of Inheritance
1. Single Inheritance![image](https://github.com/user-attachments/assets/061fd0c3-616a-4576-83b2-f4a0527a7eb3)
2. Multiple Inheritance![image](https://github.com/user-attachments/assets/1e3e0c52-9027-4250-82fa-50dc01b2c8ad)
3. Hierarchical Inheritance![image](https://github.com/user-attachments/assets/bfdbd41b-36bc-4f3e-9f01-d56a477cd6dd)
4. Multilevel Inheritance![Uploading image.png…]()
5. Hybrid Inheritance![Uploading image.png…]()

- **Questions**
1. How can we call the base method without creating an instance?:- Use static methods in the base class, which can be called directly using the class name.
2. what is the difference between new and override
3. what is a diamond problem in the case of multiple inheritance:- When a derived class inherits from two classes that share a common base, it causes ambiguity.
4. If class a inherits from class b, then what is inherited from the parent class?:- Public and protected members (variables and methods) of class B, but private members are not directly accessible.
5. how to hide base class methods/functions:- Use the new keyword to hide base class methods in derived classes.
```
class Base {
public:
    void show() { /* Base show */ }
};

class Derived : public Base {
public:
    new void show() { /* Derived show */ }
};
```
6. Friend Function/ Friend Class/ Inline Function
  1. Friend Function: Allows a non-member function to access private/protected members of a class.
  2. Friend Class: Grants access to another class to access private/protected members.
  3. Inline Function: Suggests to the compiler to replace the function call with the function code to improve performance.
7. Local class/nested class/simulating final class
  1. Local Class: A class declared inside a function.
  2. Nested Class: A class declared inside another class.
  3. Final Class: A class that cannot be inherited (use final keyword in some languages like C++).
```
class Outer {
public:
    class Nested { /* Nested class */ };
};

class FinalClass final { /* Cannot be inherited */ };
```
8. Does overloading work with inheritance:- Yes, method overloading works with inheritance. Derived classes can overload methods from the base class by changing the parameter list.
9. difference between polymorphism and inheritance
- Polymorphism: Allows different classes to be treated as instances of the same base class, with the ability to override methods.
- Inheritance: Mechanism by which one class acquires properties (methods and fields) of another.
10. generalization vs aggregation vs composition
- Generalization: Refers to creating a generic class by abstracting common characteristics (parent-child relationship).
- Aggregation: A weaker relationship where the child can exist independently of the parent.
- Composition: A strong relationship where the child cannot exist independently of the parent (lifetime dependency).
```
#include <iostream>
#include <string>
using namespace std;

// Generalization (Inheritance) Example
class Animal {
public:
    void eat() { cout << "Animal is eating..." << endl; }
};

class Dog : public Animal {  // Dog inherits from Animal (Generalization)
public:
    void bark() { cout << "Dog is barking..." << endl; }
};

// Aggregation Example (Weaker HAS-A relationship)
class Department {
public:
    string name;
    Department(string n) : name(n) {}
};

class University {
public:
    string universityName;
    Department* dept;  // Aggregation (University HAS-A Department, but dept exists independently)

    University(string uniName, Department* d) : universityName(uniName), dept(d) {}

    void showDetails() {
        cout << universityName << " has the " << dept->name << " department." << endl;
    }
};

// Composition Example (Stronger HAS-A relationship, Car cannot exist without Engine)
class Engine {
public:
    Engine() { cout << "Engine created!" << endl; }
    void start() { cout << "Engine is starting..." << endl; }
};

class Car {
private:
    Engine engine;  // Composition (Car HAS-A Engine, Engine cannot exist without Car)
public:
    Car() { cout << "Car is being assembled..." << endl; }
    void drive() {
        engine.start();
        cout << "Car is driving..." << endl;
    }
};

int main() {
    // Generalization (Inheritance) Example
    Dog myDog;
    myDog.eat();   // Inherited from Animal
    myDog.bark();  // Specific to Dog

    cout << "\n";

    // Aggregation Example
    Department csDept("Computer Science");
    University techUni("Tech University", &csDept);
    techUni.showDetails();  // University and Department exist independently

    cout << "\n";

    // Composition Example
    Car myCar;
    myCar.drive();  // Car cannot exist without Engine, engine starts when car drives

    return 0;
}
```
### 3.3 Encapsulation
#### Mind Map
- What
- Advantages
- Need
- How to achieve
- Code/Implementation Example
- Real World Example
#### Explanation of above
- **What**
  - Encapsulation is the concept of bundling data (variables) and methods (functions) that operate on the data into a single unit (class), and restricting access to some of the object's components.
- **Advantages**
  - Security: Protects the internal state of an object.
  - Control: Allows controlled access through getters and setters.
  - Modularity: Encapsulated classes are easier to maintain and debug.
- **Need**
  - It ensures that data cannot be accessed or modified directly, which protects the integrity of the object's state.
- **How to achieve**
  - Use private variables (inaccessible outside the class) and provide public methods to access/modify them
- **Code/Implementation Example**
```
class Car:
    def __init__(self):
        self.__speed = 0  # Private variable

    def set_speed(self, speed):
        if speed > 0:
            self.__speed = speed

    def get_speed(self):
        return self.__speed

car = Car()
car.set_speed(50)
print(car.get_speed())  # Output: 50
```
```
class Car {
private:
    int speed;  // Private variable

public:
    void setSpeed(int s) {
        if (s > 0) speed = s;
    }

    int getSpeed() {
        return speed;
    }
};

int main() {
    Car car;
    car.setSpeed(50);
    cout << car.getSpeed();  // Output: 50
    return 0;
}
```
- **Real World Example**
  - ATM Machine: The ATM allows users to check balance or withdraw money but hides internal processes (encapsulation). You cannot directly access or change the bank's database.
  
### 3.4 Abstraction
#### MindMap
- What
- When To use
- How to achieve
  - Python
  - Cpp
- Encapsulation vs abstraction
- What are the differences between Interfaces and abstract class
#### Explanation
- What
  - Abstraction is the concept of hiding complex implementation details and showing only the essential features of an object or process to the user.
- When To use
  - Use abstraction when you want to simplify complex systems by only exposing necessary details, allowing users to interact with the system easily.
- How to achieve
  - Python
```
    from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def area(self):
        return 3.14 * 5 * 5  # Example area calculation

circle = Circle()
print(circle.area())  # Output: 78.5
```
  - Cpp
```
class Shape {
public:
    virtual float area() = 0;  // Pure virtual function
};

class Circle : public Shape {
public:
    float area() override {
        return 3.14 * 5 * 5;  // Example area calculation
    }
};

int main() {
    Circle circle;
    cout << circle.area();  // Output: 78.5
    return 0;
}
```
- Encapsulation vs abstraction
  - Encapsulation: Hides internal state by restricting direct access (focused on data security).
  - Abstraction: Hides complexity by showing only relevant information (focused on design simplicity).
- What are the differences between Interfaces and abstract class
  - Interfaces: Only define method signatures (no implementation at all).
  - Abstract Classes: Can have both complete methods and abstract methods (partially implemented).
## 4. Dynamic Binding
## 5. Message Passing
