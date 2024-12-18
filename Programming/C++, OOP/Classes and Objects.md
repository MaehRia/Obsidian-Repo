Source: https://www.w3schools.com/cpp/cpp_classes.asp

C++ is an object-oriented programming language.

Everything in C++ is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an **object**. The car has **attributes**, such as weight and color, and methods, such as drive and brake.

Attributes and methods are basically variables and functions that belong to the class. These are often referred to as "class members".

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


- `public` keyword is an access specifier, which specifies that members (attributes and methods) of the class are accessible from the outside of the class. More info about access specifiers -> [[Classes and Objects#^ea8244]]
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

#### Definition

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


#### Parameters

Parameters also can be added.

```cpp
#include <iostream>  
using namespace std;  
  
class Car {  
  public:  
    int speed(int maxSpeed);  
};  
  
int Car::speed(int maxSpeed) {  
  return maxSpeed;  
}  
  
int main() {  
  Car myObj; // Create an object of Car  
  cout << myObj.speed(200); // Call the method with an argument  
  return 0;  
}
```

Output: 200


### Constructors

A constructor in c++ is a special method called automatically when an object of a class is created.

To create a constructor, use the same name as the class, followed by parentheses.

The constructor has the same name as the class, it is always `public`, and it does not have any return value.

```cpp
class MyClass {     // The class  
  public:           // Access specifier  
    MyClass() {     // Constructor  
      cout << "Hello World!";  
    }  
};  
  
int main() {  
  MyClass myObj;    // Create an object of MyClass (this will call the constructor)  
  return 0;  
}
```

#### Constructor Parameters

Here is the code which will serve as an example for explaining constructor parameters.

```cpp
#include <iostream>
#include <string>

class Car {        // The class  
  public:          // Access specifier  
    std::string brand;  // Attribute  
    std::string model;  // Attribute  
    int year;      // Attribute  
    Car(std::string x, std::string y, int z) { // Constructor with parameters  
      brand = x;  
      model = y;  
      year = z;  
    }  
};  
  
int main() {  
  // Create Car objects and call the constructor with different values  
  Car carObj1("BMW", "X5", 1999);  
  Car carObj2("Ford", "Mustang", 1969);  
  
  // Print values  
  std::cout << carObj1.brand << " " << carObj1.model << " " << carObj1.year << "\n";  
  std::cout << carObj2.brand << " " << carObj2.model << " " << carObj2.year << "\n";  
  return 0;  
}
```

> [!question] How does constructor work here?

1. Declaration.

The constructor `Car(string x, string y, int z)` is declared inside the class:
```cpp
Car(string x, string y, int z) { 
  brand = x;
  model = y;
  year = z;
}
```

It takes three parameters (`x`, `y`, `z`) and assigns their values to the respective class attributes (`brand`, `model`, `year`).

2. Execution.

When the object is created with parameters:
```cpp
Car carObj1("BMW", "X5", 1999);
```
The constructor is automatically called, and the parameters `x`, `y`, and `z` are assigned to `brand`, `model`, and `year`.

>[!question] Why use a constructor here?

1. Convenience.
   
The constructor allows us to initialize the `brand`, `model`, and `year` attributes of the `Car` class **in one step** when the object is created:
```cpp
Car carObj1("BMW", "X5", 1999);
```

Without the constructor, you would have to set the attributes one by one after creating the object:
```cpp
Car carObj1;
carObj1.brand = "BMW";
carObj1.model = "X5";
carObj1.year = 1999;

Car carObj2;
carObj1.brand = "Ford";
carObj1.model = "Mustang";
carObj1.year = 1969;
```

2. Ensures proper and fast initialization

With the constructor, you can ensure that all attributes (`brand`, `model`, `year`) are initialized when the object is created.
If you didn’t use a constructor, the attributes might remain uninitialized, leading to potential bugs.

3. Supports Reusability

You can reuse the same constructor for multiple objects with different values.

#### Definition

Just like functions, constructors can also be defined outside the class. First, declare the constructor inside the class, and then define it outside of the class by specifying the name of the class, followed by the scope resolution `::` operator, followed by the name of the constructor (which is the same as the class):

```cpp
#inlude <iostream>
#include <string>

class Car {        // The class  
  public:          // Access specifier  
    std::string brand;  // Attribute  
    std::string model;  // Attribute  
    int year;      // Attribute  
    Car(std::string x, std::string y, int z); // Constructor declaration  
};  
  
// Constructor definition outside the class  
Car::Car(std::string x, std::string y, int z) {  
  brand = x;  
  model = y;  
  year = z;  
}  
  
int main() {  
  // Create Car objects and call the constructor with different values  
  Car carObj1("BMW", "X5", 1999);  
  Car carObj2("Ford", "Mustang", 1969);  
  
  // Print values  
  std::cout << carObj1.brand << " " << carObj1.model << " " << carObj1.year << "\n";  
  std::cout << carObj2.brand << " " << carObj2.model << " " << carObj2.year << "\n";  
  return 0;  
}
```


### Access specifiers

^ea8244
In C++, there are three access specifiers:

- `public` - members are accessible from outside the class
- `private` - members cannot be accessed (or viewed) from outside the class
- `protected` - members cannot be accessed from outside the class, however, they can be accessed in inherited classes. 

By default, all members of a class are `private` if you don't specify an access specifier․