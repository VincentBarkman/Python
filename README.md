# Python Basics

This tutorial covers the basics of Python programming language. Python is a high-level, interpreted, and general-purpose programming language known for its readability and simplicity.

## Table of Contents

1. [Hello World](#hello-world)
2. [Variables and Data Types](#variables-and-data-types)
3. [Operators](#operators)
4. [Control Structures](#control-structures)
5. [Functions](#functions)
6. [Modules and Packages](#modules-and-packages)

## Hello World

The simplest Python program consists of a single line that prints "Hello, World!" to the screen.

```python
print("Hello, World!")
```

## Variables and Data Types

Python has several built-in data types. The most common ones are:

    `int`: Integer numbers
    `float`: Floating-point numbers
    `str`: String (text)
    `bool`: Boolean (True or False)

You can assign values to variables using the assignment operator `=`.


```python
integer_var = 42
float_var = 3.14
string_var = "Python"
boolean_var = True
```

## Operators

Python provides various operators for performing operations on variables and values. Some common operators are:

    Arithmetic operators: +, -, *, /, //, %, **
    Comparison operators: ==, !=, <, >, <=, >=
    Logical operators: and, or, not

##Control Structures

Python uses control structures to control the flow of code execution. The most common control structures are:
### If, elif, and else

```python
if condition:
    # code executed if condition is True
elif another_condition:
    # code executed if another_condition is True
else:
    # code executed if none of the conditions are True
```
### For loop
```python
for variable in iterable:
    # code executed for each item in the iterable
```
### While loop
```python
while condition:
    # code executed while the condition is True
```

## Functions
In Python, you can define functions to encapsulate reusable pieces of code.
```python
def function_name(parameters):
    # code inside the function
    return result
```

# Modules and Packages
Python has a rich ecosystem of libraries and modules that you can use to extend the 
functionality of your programs. You can import modules using the import statement.
```python
import module_name

# or

from module_name import specific_function_or_class
```
For example, to use the math module, you can do:
```python
import math

result = math.sqrt(16)
print(result)  # Output: 4.0
```
