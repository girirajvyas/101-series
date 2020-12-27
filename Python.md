# python 101


## What you can do:
 - AI/ML
 - Web development with Django (youtube, insagram, spotify pinterest)
 - Automation

## First python program - Hello world

### pre-requisites: 
**Home**  
 - https://www.python.org/
 - Documentation: https://docs.python.org/3/  

**Versions:**  
 - python 2.7 and 3.x (Both used)  
 - Python 3
    - introduced in 2010 and future of python
    - few incompatibilities with 2.7
 - Python 2.7
    - Last version of Python 2
    - static since 2012

**Python Installation:**  
 - python from https://www.python.org/ -> Downloads -> latest version of python
 - Run Python installer -> make sure you tick "Add Python 3.x to PATH"

**IDEs:**  
 - Jupyter environment,  
 - JetBrains PyCharm community edition

**Jupyter**  
 - Formerly Ipython Notebook
 - Notebooks contain code and text
 - perfect for iterable work like machine learning
 - shareable
 - support multiple languages (Ruby, R, Haskell, C#, PHP, Scala...)
 - This can be installed bia Anaconda

**Jupyter and conda Installation:**  
 - Anaconda (https://www.anaconda.com/download/) -> downloaded Anaconda3-2020.11-Windows-x86_64 which is latest on 20_November_2020
 - it takes some time to install
 - go to windows -> Anaconda Navigaor -> Jupyter notebook
 - Shift + enter -> runs code
 - new -> folder -> untitled folder -> select checkbox left to it -> rename -> notebooks
 - new -> python 3 -> will open a notebook in new tab
 - esc + m -> markdown mode
 - esc + y -> code mode

`Conda: package and environment manager`

**PyCharm**
 - Pycharm (https://www.jetbrains.com/pycharm/download/ -> download community edition) -> Install

**VS Code**  
 - VS Code https://code.visualstudio.com/docs/?dv=winzip
 - Install python plugin
 - Install ipykernel

### Create Project:
 - Open pycharm -> skip setting with default -> new project 
      - Choose workspace location
      - In case you check "Create a main.py welcome script", it will create that for you
 - Create app.py
 - Type: print "Hello World"
 - Run

You have successfully created your first hello world programme

### Variables
```
age = 20 (declaration)
age = 30 (reassignment)
price = 19.95 (float)
first_name = "Giri" ()
is_online = False/True (false and true is not a keyword as python is case sensitive)
```

Exercise 1:
We check in a patient named john smith
he is 20 years old
he is a new patient

### Receiving input
```
name = input("What is your name? ")
print("Hello " + name)
```
Note: value returned from input function is String

## Type conversion
Data types: Number, String boolean  

Code that fails:
```
birth_year = input("Enter your birth year: ")
age = 22 - birth_year
print(age)
```

Error:
raceback (most recent call last):
  File "D:/Workspaces/workspace_pycharm/app.py", line 10, in <module>
    age = 22 - birth_year
TypeError: unsupported operand type(s) for -: 'int' and 'str'

Code after fix:  
```
birth_year = input("Enter your birth year: ")
age = 22 - int(birth_year)
print(age)
```

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

Intro
The zen of python	
Python Command line terminal is REPL: Read Evaluate Print Loop
_ to print recently printed value only available thru command line(REPL)
print('Hello World') -> HEllo World - This is a side effect of print() not the result of print()
In python 3 parenthesis() are mandatory while in python they were not required. This is because in python 3 print is a function call
Exit REPL - send end of file control character (ctrl + Z on windows, followed by enter)((ctrl + D on mac or linux )
python uses indentation levels rather than the braces used by other languages
indented by four spaces at each level

Rules for spaces:
1. prefer four spaces or tabs (spaces preferred)
2. Never mix spaces and tabs
3. Be consistent on consecutive lines
4. only deviate to improve readability

PEP (similar to JSRs it seems) PEP-8: 4 spaces rule PEP-20: Zen of python, import this in REPL

Python comes with an extensive standard library called batteries
Standard library is divided into modules. To include any module use import module_name
help() or help(math or any module_name), space to navigate and Q to quit 
from math import factorial, from math import factorial as fac
/ float division operator, // integer division operator

Scalar types: 
int - arbitrary precision integer, 
binary 0b10, Octal 0O10, hexadecimal 0X10
covert any type to integer via constructor. int(3.5) = 3, int (-3.5) = 3 -> it rounds towards zero

float -  64 bit floating point numbers
scientific notation (large numbers ): 3e8
planck's constant (small numbers ): 1.616e - 35
float(7), float("1.618"), float ("nan") , float ("inf") , float ("-inf") 

None - the null object
a = None
a is None = True
bool - boolean logical values
bool(0) = false all others true
bool(0.0)=false all others true
bool([])= false, bool([1,2,2]) = true
bool("")=false, bool("value")=true

Relational Operators:
== value equality / equivalence
!= value inequality / inequivalence
<  less-than 
>  greater-than
<= less-than or equal to
>= greater-than or equal to

Conditional statements
if expression :
	print("expression is true")
expression is converted to bool as if by the bool() constructor
*python provides the elif keyword to eliminate the need for nested if..else structures in many cases (flat is better than nested)

Loops:
1. while loop
While expression :
	print("loop till expression is true")
e.g.: c = 5
while c != 0 :
	print(c)
	c -= 1	
augmented assignment shorthand c -= 1 for c = c - 1

2. Do while loop example
while True:
	if expression:
		break -> break statement jumps out of the loop and only the innermost loop in case of nested loops
print("go here on break")

String and collections: 
String str immutable sequence of unicode codepoints

# Resources:
 - https://github.com/vinta/awesome-python
 