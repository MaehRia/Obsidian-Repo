Source: https://www.w3schools.com/cpp/cpp_classes.asp

C++ is an object-oriented programming language.

Everything in C++ is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an **object**. The car has **attributes**, such as weight and color, and methods, such as drive and brake.

Attributes and methods are basically **variables** and **functions** that belongs to the class. These are often referred to as "class members".

A class is a user-defined data type that we can use in our program, and it works as an object constructor, or a "blueprint" for creating objects.

### Creating a Class

Creating a class called "MyClass", using `class` keyword.

```cpp
class MyClass { //the class
public: //access specifier
	int myNum; //atribute N1
	std::string myString; //attribute N2
};
```


- `public` keyword is an access specifier, which specifies that members (attributes and methods) of the class are accessible from the outside of the class.
- `myNum` and `myString` are called attributes, because they are declared within the class

### Creating an Object

In C++, an object is created from a class. We have already created the class named `MyClass`, so now we can use this to create objects.

To create an object of `MyClass`, specify the class name, followed by the object name.

To access the class attributes (`myNum` and `myString`), use the dot syntax (`.`) on the object:

```cpp
class MyClass {       // The class
  public:             // Access specifier
    int myNum;        // Attribute (int variable)
    string myString;  // Attribute (string variable)
};

int main() {
  MyClass myObj;  // Create an object of MyClass

  // Access attributes and set values
  myObj.myNum = 15; 
  myObj.myString = "Some text";

  // Print attribute values
  cout << myObj.myNum << "\n";
  cout << myObj.myString;
  return 0;
}
```

Output: 
	15
	Some text

### Class methods

Methods are functions that belong to the class. There are two ways to define a function that belongs to a class.

1. Inside class definition
   
Example.

```cpp
#include <iostream>

class MyClass {         // The class
  public:               // Access specifier
    void myMethod() {   // Method/function
      std::cout << "Hello World!";
    }
};

int main() {
  MyClass myObj;     // Create an object of MyClass
  myObj.myMethod();  // Call the method
  return 0;
}

```


2. Outside class definition
   
   To define a function outside the class definition, you have to declare it inside the class and then define it outside of the class. This is done by specifying the name of the class, followed the scope resolution :: operator, followed by the name of the function:

Example.

```cpp
class MyClass {        // The class  
  public:              // Access specifier  
    void myMethod();   // Method/function declaration  
};  
  
// Method/function definition outside the class  
void MyClass::myMethod() {  
  cout << "Hello World!";  
}  
  
int main() {  
  MyClass myObj;     // Create an object of MyClass  
  myObj.myMethod();  // Call the method  
  return 0;  
}
```