---
media_link: https://www.youtube.com/watch?v=_uQrJ0TkZlc
---

This is a video course made by Mosh_Hamadani, about  basics of [[Python_Intro]].

[21:00](https://www.youtube.com/watch?t=1260&v=_uQrJ0TkZlc) Receiving Input:

```python
name = input("What's your name? " )  
color = input("What's your fav color? " )  
print(name + " likes " + color + ".")
```

[1:04:42](https://www.youtube.com/watch?t=3882&v=_uQrJ0TkZlc) if statement:

```python
price = 1000000  
good_credit = True  
if good_credit:  
    payment = 100000
else:  
    payment = 200000
print(f"Payment is ${payment}.")  
```

 [1:10:47](https://www.youtube.com/watch?t=4247&v=_uQrJ0TkZlc) if statement:
 
```python
has_high_income = True  
has_criminal_record = False  
if has_high_income and not has_criminal_record:  
    print("Eligible for loan.")
```

[1:14:38](https://www.youtube.com/watch?t=4478&v=_uQrJ0TkZlc) Comparison operators:

```python
name = "J"  
  
if len(name) < 3:  
    print("Name must be at least 3 characters.")
elif len(name) > 50:  
    print("Name must be maximum of 50 characters")
else:  
    print("Nmase looks good.")
```

[1:20:49](https://www.youtube.com/watch?t=4849&v=_uQrJ0TkZlc) While loop:

```python
i = 1
while i <= 5:
    print("*" * i)
    i += 1
print("Done")

```

[1:24:08](https://www.youtube.com/watch?t=5048&v=_uQrJ0TkZlc) Guessing game:

```python
secret_number = 5
guess_count = 0
guess_limit = 3
while guess_count < guess_limit:
    guess = int(input("Guess: "))
    guess_count += 1
    if guess == secret_number:
        print("You won!")
        break
else:
    print("You failed.")
```

[1:30:50](https://www.youtube.com/watch?t=5450&v=_uQrJ0TkZlc) Car racing game:

```python
command = ""
started = False
stopped = False
while True:
    command = input(">").lower()
    if command == "start":
        if started:
            print("Car already started!")
        else:
            started = True
            print("Car started...")
    elif command == "stop":
        if not started:
            print("Car is already stopped.")
        else:
            started = False
            print("Car stopped.")
    elif command == "help":
        print("""
start -> to start the car
stop -> to stop the car
quit -> to quit
        """)
    elif command == "quit":
        break
    else:
        print("Sorry, i don't understand the command.")
        
```

[1:51:25](https://www.youtube.com/watch?t=6685&v=_uQrJ0TkZlc) Drawing "F":

```python
#1ST WAY

numbers = [5, 2, 5, 2, 2]
for i in numbers:
    output = ""
    for count in range(i):
        output += "x"
    print(output)

#2ND WAY

numbers = [5, 2, 5, 2, 2]
for i in numbers:
    print("x" * i)
```

[2:01:52](https://www.youtube.com/watch?t=7312&v=_uQrJ0TkZlc) 2D lists:

```python
matrix = [
    [1, 2, 3],
    [4, 5 ,6],
    [7, 8, 9]
]
matrix[0][1] = 20
for row in matrix:
    for item in row:
        print(item)
```

[2:12:05](https://www.youtube.com/watch?t=7925&v=_uQrJ0TkZlc) Program that removes the duplicates in a list:

```python
numbers = [2, 2, 4, 5, 6, 4]  
uniques = []  
for number in numbers:  
    if number not in uniques:      
		uniques.append(number)print(uniques)
```

[2:16:12](https://www.youtube.com/watch?t=8172&v=_uQrJ0TkZlc) Unpacking:

```python
coordinates = (1, 2, 3)
x = coordinates[0]
y = coordinates[1]
z = coordinates[2]

x, y, z = coordinates
```

[2:18:26](https://www.youtube.com/watch?t=8306&v=_uQrJ0TkZlc) Dictionaries:

```python
customer = {
    "name": "John Smith",
    "age": 30,
    "is_verified": True
}
customer["name"] = "Jack Smith"
customer["birthday"] = "Aug 18"
print(customer["name"])
print(customer.get("birthday", "Jan 1, 1980"))
```

```python
phone = input("Phone: ")
digits_mapping = {
    "1": "One",
    "2": "Two",
    "3": "Three",
    "4": "Four",
    "5": "Five",
    "6": "Six",
    "7": "Seven",
    "8": "Eight",
    "9": "Nine",
}
output = ""
for char in phone:
    output += digits_mapping.get(char, "!") + " "
print(output)
```

[2:26:26](https://www.youtube.com/watch?t=8786&v=_uQrJ0TkZlc) Emoji converter:

```python
message = input(">")  
words = message.split(' ')  
emojis = {  
    ":)": "😁",  
    ":(": "😒"  
}  
output = ""  
for word in words:  
    output += emojis.get(word, word) + " "
print(output)
```

[2:30:37](https://www.youtube.com/watch?t=9037&v=_uQrJ0TkZlc) Functions:

(here are also used ***Keyword Arguments***)

```python
def greet_user(name, surname):
    print(f"Hi {name} {surname}!")
    print("Welcome abroad!")


print("Start")
greet_user(surname = "Smith", name = "Jon")
greet_user("Mary", "Jane")
print("Finish")
```

```python
def square(number):
    return number * number

print(square(3))
```

(example of reusable function)

```python
def emoji_converter(message):
    words = message.split(" ")
    emojis = {
        ":)": "😁",
        ":(": "😒"
    }
    output = ""
    for word in words:
        output += emojis.get(word, word) + " "
    return output

message = input(">")
print(emoji_converter(message))
```

[2:43:29](https://www.youtube.com/watch?t=9809&v=_uQrJ0TkZlc) Keyword Arguments:

```python
calc_cost(50, 5, 0.1) <=> calc_cost(toatl = 50, shipping = 5, discount = 0.1)
```

[2:53:49](https://www.youtube.com/watch?t=10429&v=_uQrJ0TkZlc) Exceptions: (try & except)

```python
try:
    age = int(input("Age: "))
    income = 20000
    risk = income / age
    print(age)
except ValueError:
    print("Invalid value")
except ZeroDivisionError:
    print("Age cannot be 0")
```

> [!important] 
> It's important and eye-catching that <u>[[Pascal Naming Convention]]</u> were used while naming error types, classes and etc. 

[3:01:52](https://www.youtube.com/watch?t=10912&v=_uQrJ0TkZlc) Classes:

```python
class Point(): # or EmailClient
    def move(self):
        print("move")

    def draw(self):
        print("draw")


point1 = Point()
point1.x = 10
point1.y = 20
print(point1.x)
point1.draw()

point2 = Point()
point2.x = 1
print(point2.x)
```

[3:07:51](https://www.youtube.com/watch?t=11271&v=_uQrJ0TkZlc) Constructions:

```python
class Person:
    def __init__(self, name):
        self.name = name

    def talk(self):
        print(f"Hi, I am {self.name}.")


Jon = Person("Jon Snow")
print(Jon.name)
Jon.talk()

Sansa = Person("Sansa Stark")
Sansa.talk()
```

[3:14:48](https://www.youtube.com/watch?t=11688&v=_uQrJ0TkZlc) Inheritance:

```python
#both Dog and Cat are inheriting all the methods defined in the parent class
class Mammal:
    def walk(self):
        print("walk")


class Dog(Mammal):
    #here we add methods specific for dogs
    def bark(self):
        print("bark")
    # here we don't need to add "pass", because we have defined a method


class Cat(Mammal):
    pass

dog1 = Dog()
dog1.walk()
```

> [!note]  
> If there's needed to change a variables name, which was used multiple times it's more efficient to use ==Shift + F6== shortcut. Or by using right click on the variable > refactor > rename.

[3:19:40](https://www.youtube.com/watch?t=11980&v=_uQrJ0TkZlc) Modules: 

```python
# It's the part used in main.py
import converters  
from converters import kgs_to_lbs  
  
kgs_to_lbs(100)
```

```python
# it's the part used in converters.py file
# projects > main project > file(or python file)
def lbs_to_kgs(weight):
    return weight * 0.45

def kgs_to_lbs(weight):
    return weight / 0.45
```

[3:23:58](https://www.youtube.com/watch?t=12238&v=_uQrJ0TkZlc) Modules (Exercise find_max()):

```python
# way 1
# main.py part
from utils import find_max
from utils import creating_list

creating_list()
find_max()
```

```python
#utils file part
lst = []  
  
  
def creating_list():  
    n = int(input("Enter the number of elements : "))  
    for i in range(0, n):  
        element = int(input())  
        lst.append(element)  
    print(lst)  
  
  
def find_max():  
    max = lst[0]  
    for item in lst:  
        if item > max:  
            max = item  
    print(max)
```

```python
# way 2
# main.py part
from utils1 import find_max

numbers = [10, 3, 6, 2]
max = find_max(numbers)
print(max)
```

```python 
#utils1 file part
def find_max(numbers):  
    maximum = numbers[0]  
    for number in numbers:  
        if number > maximum:  
            maximum = number  
    return maximum
```

[3:30:22](https://www.youtube.com/watch?t=12622&v=_uQrJ0TkZlc) Packages:

It is essential to know how to work with packages while programming with Django.

```python
# way 1
import ecommerce.shipping  
  
ecommerce.shipping.calc_shipping()
```

```python
# way 2
from ecommerce.shipping import calc_shipping  
calc_shipping()
```

```python
# in case we want to access all teh funcyions in a certain module
from eccomerce import shipping

shipping.calc_shipping()
```

```python
# here is the "shipping" module
def calc_shipping():  
    print("calculate shipping")
```

[3:36:30](https://www.youtube.com/watch?t=12990&v=_uQrJ0TkZlc) Generating random values:

> [!note] 
>  There are built-in modules in python, so python comes with a standard libraries  that contains several modules for common tasks (generate rand values, sending emails, working with date and time search in google): It's easy to have access to them by typing "python 3 module index" in  browser:

```python
# generating random values
import random

for i in range(3):
    print(random.randint(10, 20))
```

```python
# picking random item in a list
import random

members = ["Mary", "Ann", "Joan", "Mosh", "Alex"]
leader = random.choice(members)
print(leader)
```

[3:42:15](https://www.youtube.com/watch?t=13335&v=_uQrJ0TkZlc) Exercise:

```python
# exercise about creatinf possible values that 2 dices can give, where dice is a class, and roll() is module inside it
import random


class Dice:
    def roll(self):
        first = random.randint(1, 6)
        second = random.randint(1, 6)
        return first, second

dice = Dice()
print(dice.roll())
```

[3:44:48](https://www.youtube.com/watch?t=13488&v=_uQrJ0TkZlc) Files and Directions:

There are two types of paths: Absolute in relative.
Example of absolute path:
c:\\Programm Files\\Microsoft\\... (in Windows)
/usr/local/bin (in MacOS)

```python
from pathlib import Path # P is capital, because Pth is class
path = Path("ecommerce")  
print(path.exists())
```

```python
# making directory that doesn't exist
path = Path("emails")
print(path.mkdir())
```

```python
# removing/deleting directory 
path = Path("emails")
print(path.rmdir())
```

```python
# glob(),with this method we can search for current paths and directories
path = Path()
print(path.glob("*"))
```

"\*" or "*.*" all files and all directories, we this pattern we only get the files in the current directory, but we don't get the directories
 "\*.py" - only py files
 "\*.xls" - Excel spreadsheets
```python
for file in path.glob("*"):
    print(file)
```

[3:53:32](https://www.youtube.com/watch?t=14012&v=_uQrJ0TkZlc) Pypi and Pip. Project 1:

```python
import openpyxl as xl
from openpyxl.chart import BarChart, Reference

def process_workbook(filename):
    wb = xl.load_workbook(filename)
    sheet = wb["Sheet1"]

    '''cell = sheet["a1"] #its the same as the line below
    cell = sheet.cell(1, 1,)'''

    for row in range(2, sheet.max_row + 1):
        cell = sheet.cell(row, 3)
        corrected_price = cell.value * 0.9
        corrected_price_cell = sheet.cell(row, 4)
        corrected_price_cell.value = corrected_price

    values = Reference(sheet,
              min_row=2,
              max_row=sheet.max_row,
              min_col=4,
              max_col=4)

    chart = BarChart()
    chart.add_data(values)
    sheet.add_chart(chart, "e2")

    wb.save(filename)
```

![[Spredsheet.xlsx]]![[spredsheet1.xlsx]]
[4:11:00](https://www.youtube.com/watch?t=15060&v=_uQrJ0TkZlc) [[Machine Learning]]:

Imagine a situation, where it is given a picture and the main goal is to identify whether there is cat or dog on the picture. ML is a technique for solving that kind of problems, so here is how it works: we build a module (or an engine), and give it lots of data, in this case thousands of pictures where cats and dogs are depicted. Our module will then find and read patterns in the input data. After analyzing that it will determine whether there is cat or dog by itself. 

> [!note] 
> The more input data we give it the more accurate our model is going to be. 

# Project


**STEPS :** (these are high level steps)
1. Import the Data
2. Clean Data
3. Split the Data into Training / Test Sets
4. Create a Model
5. Train the Model
6. Make prediction
7. Evaluate the predictions and Improve them

[4:15:46](https://www.youtube.com/watch?t=15346&v=_uQrJ0TkZlc) Popular Python Libraries that are used in ML:

  1. Numpy (provides multidimensional arrays)
  2. Pandas (provides data frames)
  3. MatPlotLib (two dimensional plotting library for creating graphs on plots)
  4. Scikit-Learn

  > [!info]  What is plotting data in Python?
  > A **plot** is a [graphical technique](https://en.wikipedia.org/wiki/Graphical_technique "Graphical technique") for representing a [data set](https://en.wikipedia.org/wiki/Data_set "Data set"), usually as a [graph](https://en.wikipedia.org/wiki/Graph_of_a_function "Graph of a function") showing the relationship between two or more variables. The plot can be drawn by hand or by a computer. In the past, sometimes mechanical or electronic [plotters](https://en.wikipedia.org/wiki/Plotter "Plotter") were used. Graphs are a visual representation of the relationship between variables, which are very useful for humans who can then quickly derive an understanding which may not have come from lists of values.
  > 
  > P.S. The [wiki link](https://en.wikipedia.org/wiki/Plot_(graphics)#:~:text=A%20plot%20is%20a%20graphical,or%20electronic%20plotters%20were%20used.), just in case: 

[4:23:27](https://www.youtube.com/watch?t=15807&v=_uQrJ0TkZlc)

```python
import pandas as pd
df = pd.read_csv('vgsales.csv')
df
```

> [!error]  File Not Found Error
>  This guys video helped me to solve a huge problem described in [video](https://youtu.be/uPB37sESdro?si=fbFNYfLq7H7hT53a), I'll attach it here just in case for future possible errors.

Some of the most useful methods and attributes:

Input: df.shape
Output: (16598, 11)

Input: df.describe()
Output: description of columns

Input: df.values
Output: 2D array

```python
import pandas as pd
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

data = pd.read_csv('music.csv')
X =data.drop(columns = ['genre'])
y = data['genre']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2)


model = DecisionTreeClassifier()
model.fit(X_train, y_train)
predictions = model.predict(X_test)

score = accuracy_score(y_test, predictions)
score
```

[5:00:48](https://www.youtube.com/watch?t=18048&v=_uQrJ0TkZlc) First Django Project:

