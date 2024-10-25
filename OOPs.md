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
```class class_name
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
```class MyClass {
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
### Difference between structure and class
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
