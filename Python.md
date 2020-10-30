# python 101


## What you can do:
 - AI/ML
 - Web development with Django (youtube, insagram, spotify pinterest)
 - Automation

## First python program - Hello world

### pre-requisites: 
 - python from https://www.python.org/ -> Downloads -> latest version of python
 - Run Python installer -> make sure you tick "Add Python 3.x to PATH"
 - Code editor: 
     - Pycharm (https://www.jetbrains.com/pycharm/download/ -> download community edition) -> Install
     - Jupyter (you can get it with anaconda or directly)

### Create Project:
 - Open pycharm -> skip setting with default -> new project 
      - Choose workspace location
      - In case you check "Create a main.py welcome script", it will create that for you
 - Create app.py
 - Type: print "Hello World"
 - Run
You have successfully created your first hello world programme

### Variables
age = 20 (declaration)
age = 30 (reassignment)
price = 19.95 (float)
first_name = "Giri" ()
is_online = False/True (false and true is not a keyword as python is case sensitive)

Exercise 1:
We check in a patient named john smith
he is 20 years old
he is a new patient

### Receiving input
name = input("What is your name? ")
print("Hello " + name)

Note: value returned from input function is String

## Type conversion
Data types: Number, String boolean

Code that fails:
birth_year = input("Enter your birth year: ")
age = 22 - birth_year
print(age)

Error:
raceback (most recent call last):
  File "D:/Workspaces/workspace_pycharm/app.py", line 10, in <module>
    age = 22 - birth_year
TypeError: unsupported operand type(s) for -: 'int' and 'str'

Cod after fix:
birth_year = input("Enter your birth year: ")
age = 22 - int(birth_year)
print(age)

Built in functions for type conversion
int()
float()
bool()
str()

Exercise 2:
Writ a calculator to print sum. Input can be integer or float

Solution 1:
first = input("First: ")
second = input("Second: ")

sum = float(first) + float(second)

print("sum " + str(sum))

Solution 2:
first = float(input("First: "))
second = float(input("Second: "))

sum = first + second

print("sum " + str(sum))

## Strings
course = "Python for beginners"

# In built string functions
print(course.)



