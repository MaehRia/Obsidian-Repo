## String class

C++ has in its definition a way to represent a sequence of characters as an object of the class. This class is called std:: string. The string class stores the characters as a sequence of bytes with the functionality of allowing access to the single-byte character.

### String vs Character Array

| String                                                                                                                                                                  | Char Array                                                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A string is a **class that defines objects** that be represented as a stream of characters.                                                                             | A character array is simply an array of characters that can be terminated by a null character.                                                                   |
| In the case of strings, memory is **allocated dynamically**. More memory can be allocated at run time on demand. As no memory is preallocated, **no memory is wasted**. | The size of the character array has to be allocated statically, more memory cannot be allocated at run time if required. Unused allocated memory is also wasted. |
| As strings are represented as objects, **no array decay** occurs.                                                                                                       | There is a threat of array decay in the case of the character array.                                                                                             |
| **Strings are slower** when compared to implementation than character array.                                                                                            | Implementation of character array is faster than std::string.                                                                                                    |
| String class defines **a number of functionalities** that allow manifold operations on strings.                                                                         | Character arrays **do not offer** many inbuilt functions to manipulate strings.                                                                                  |
### Operations on Strings

| Function                                                                | Definition                                                                                              |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [getline()](https://www.geeksforgeeks.org/getline-string-c/)            | This function is used to store a stream of characters as entered by the user in the object memory.      |
| [push_back()](https://www.geeksforgeeks.org/stdstringpush_back-in-cpp/) | This function is used to input a character at the end of the string.                                    |
| pop_back()                                                              | Introduced from C++11(for strings), this function is used to delete the last character from the string. |
Example of using the 3 functions above:

```cpp
#include <iostream>
#include <string> // for string class

using namespace std;

int main()
{
	// declaring string
	string str;
	// taking string input using getline()
	getline(cin, str);
	// displaying string
	cout<<"The initial string is : "<<str<<endl;
	// inserting new character
	str.push_back('abcd');
	//dosplaying changes
	cout<<"The string after push_back operation : "<<str<<endl;
	//deleting a character
	str.pop_back();
	//displaying string
	cout<<"The string after pop_back operation : "<<str<<endl;
	return 0;
}
```

### getline()

There are two different ways of declaring and initializing the C++ getline: three parameters and two parameters. The syntax for declaring the function with three parameters is:

1) istream& getline (istream& is, string& str, char delimiting);

- istream& is: This is the istream class’s object to define the location, to read the input stream.
- istream& str: This is the object where the string is stored after reading.
- char delimiting: This is the delimiting character that marks the end of taking inputs.

2) istream& getline( istream& is, string& str );

- istream& is: This is an istream class’s object to specify the location to read the input stream.
- istream& str: This is the object where the string is stored after reading.


## 