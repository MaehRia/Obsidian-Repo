
[[Python Course for Beginners + ML]]




 
**Python** is a [high-level](https://en.wikipedia.org/wiki/High-level_programming_language "High-level programming language"), [general-purpose programming language](https://en.wikipedia.org/wiki/General-purpose_programming_language "General-purpose programming language"). Its design philosophy emphasizes [code readability](https://en.wikipedia.org/wiki/Code_readability "Code readability") with the use of [significant indentation](https://en.wikipedia.org/wiki/Off-side_rule "Off-side rule").
Python is [dynamically typed](https://en.wikipedia.org/wiki/Type_system#DYNAMIC "Type system") and [garbage-collected](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science) "Garbage collection (computer science)"). It supports multiple [programming paradigms](https://en.wikipedia.org/wiki/Programming_paradigm "Programming paradigm"), including [structured](https://en.wikipedia.org/wiki/Structured_programming "Structured programming") (particularly [procedural](https://en.wikipedia.org/wiki/Procedural_programming "Procedural programming")), [object-oriented](https://en.wikipedia.org/wiki/Object-oriented_programming "Object-oriented programming") and [functional programming](https://en.wikipedia.org/wiki/Functional_programming "Functional programming"). It is often described as a "batteries included" language due to its comprehensive [standard library](https://en.wikipedia.org/wiki/Standard_library "Standard library").
[Guido van Rossum](https://en.wikipedia.org/wiki/Guido_van_Rossum "Guido van Rossum") began working on Python in the late 1980s as a successor to the [ABC programming language](https://en.wikipedia.org/wiki/ABC_(programming_language) "ABC (programming language)") and first released it in 1991 as Python 0.9.0.
Python consistently ranks as one of the most popular programming languages, and has gained widespread use in the [[machine learning]] community.

==Guido van Rossum==, the designer of Python.

![Guido van Rossum| 500](https://aem.dropbox.com/cms/content/dam/dropbox/blog/files/2019/11/guido_hero.jpg/_jcr_content/renditions/guido_hero.webp)


# Python basics (something like cheat-sheet)

Though, I have created quite comprehensive note abouts python introductory and the basics of coding in python in [[Python Course for Beginners + ML]] note, I felt it necessary to transfer here my cheat-sheet collected more than a year ago.

```python 
# ways to import math

# N1
print(math.sin(30* math.pi / 180))

# N2
from math import sin, pi  
print(sin(30 * pi / 180))

# N3
from math import *

# N4
import math as x  
print(x.sin(30 * x.pi / 180))
```

pow(12, 3) -> 1728
pow(7, 2, 5) -> 7^2 %5 = 5

divmod(7, 3) -> (2, 1)
a, b = divmod(7, 3)
a = 2, b = 1

round(5.4) -> 5
round(5.5) -> 6
round(3.34556, 3) -> 3.346
round(274.45,-2) -> 300.0
round(274.45,-1) -> 270.0  
round(275.45,0) -> 275.0

floor(32.9) -> 32
floor(-3.1) -> -4

ceil(32.1) -> 33
ceil(-3.4) -> -3

float(True) -> 1.0
float(False) -> 0.0
float('True') -> ValueError: could not convert string to float:'True'
float(3,8) -> TypeError: float expected at most 1 argument, got 2
float('3.78') -> 3.78
float(3) -> 3.0
float('3') -> 3.0
float(True) -> 1.0
float(False) -> 0.0

str(23) -> '23'
str(2,3) -> TypeError: str() argument 'encoding' must be str, not int

bool(0) -> False  
bool() -> False  
bool(-5) -> True  
bool(' ') -> True  
bool('') -> False  
bool([]) -> False  
bool({}) -> False


```python
# f string
a = 2  
b = 4.187  
c = 'hello'  
print(f'A={a},B={b},C={c}')
# A=2,B=4.187,C=hello
print('A=%d,B=%f,C=%s' % (a, b, c)) 
# A=2,B=4.187000,C=hello
print('A={},B={}'.format(a, b))
print('A={0},B={1}'.format(a, b))  
print('A={1},B={0},C={2}'.format(a, b, c)) 
# A=4.187,B=2,C=hello
print('A={},B={},C={}'.format(b, a, c)) # the same as line 11 
print(f'A={a:10d},B={b:8.2f},C={c:10s}') 
# A=         2,B=    4.19,C=hello     | here is the end 
print('A=%10d, B=%8.2f' % (a, b))  
# A=         2, B=    4.19
print('A={:10d}, B={:8.2f}'.format(a, b)) # the same as line 16
print('A={1:8.2f}, B={0:10d}'.format(a, b))
# A=    4.19, B=         2
```

Logical operators (by priority)

1) not (logic negation)  
2) and (&)  
3) or ( logical XOR, ^(upwards caret)) 
If one, but not both arguments are true, then the result is true.
Or, we could say, if the number of true inputs is odd, then the result will be true.

0 XOR 0 = 0
1 XOR 0 = 1
0 XOR 1 = 1
1 XOR 1 = 0

5) or (logical or, |(vertical bar or pipe))


==True-False quick exercise:==

x=7  
x>=3  
True  
7>=x>=3  
True  
x>=3 and x<=7  
True  
x=15  
x>=3 and x<=7  
False  
x<3 or x>7  
True  
not(3<=x<=7)  
True  
not(x>=3 and x<=7)  
True  
x=3  
y=-7  
x>y  
True  
x>0 and y>0  
False

18 % 5 != 2 and (9 // 4 * 4 < 4 or not 20//6\==3) 
False  
not False or True and False  
True

![[Screenshot 2024-07-12 002306.png|450]]

> [!error] 
>  It is essential to use two equality signs.
>  One equality sign is used only when assigning some values to arguments.

==More exercises:==

-25%2  
1  
-3%2  
1  
3%-2  
-1  
-7%5  
3
3.25%1\==0  
False  
3%1\==0  
True
pow(x, 1 / 2) == int(pow(x, 1 / 2))  
True  
y = 10  
pow(y, 1 / 2) == int(pow(y, 1 / 2))  
False
math.sqrt(49)%1\==0  
True  
math.sqrt(10)%1\==0  
False

```python
# 1
'''if a > b:
    if a > c:
        m = a
    else:
        m = c
else:
    if b > c:
        m = b
    else:
        m = c
print(m)'''
# 2    
'''m = a
if m < b:
    m = b
if m < c:
    m = c
print(m)'''
# 3
'''if a > b:
    m = a
else:
    m = b
if c > m:
    m = c
print(m)'''
# 4
'''if a > b and a > c:
    m = a
elif b > a and b > c:
    m = b
elif c > a and c > b:
    m = c
print(m)'''
# 5
'''if b < a > c:
    m = a
elif c < b > a:
    m = b
elif a < c > b:
    m = c
print(m)'''
# 6
'''m = max(a, b, c)
print(m)
'''
```



list(map(int, input().split())) 

Let's break it down:

- input() gets user input and returns a string, e.g. "1 2 3 4 5"
 
- input().split() splits that input on whitespaces, e.g. ["1", "2", "3", ...]
 
- int() converts a string to a integer, e.g. "1" -> 1
 
- map(fn, sequence) applies the function fn to each element in the sequence, e.g. fn(sequence[0]), fn(sequence[1]), ...

- map(int, input().split()) applies int to each string element in the input, e.g. ["1", "2", "3", ...] -> int("1"), int("2"), ...

- list() turns any iterator/generator to a list, e.g. int("1"), int("2"), ... => [1, 2, 3, ...]

