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
# Define a variable 'age' with a value
age = 25

# Check if age is less than 18
if age < 18:
    print("You are a minor.")
# Check if age is between 18 and 64 (inclusive)
elif 18 <= age < 65:
    print("You are an adult.")
# If none of the above conditions are true, execute the code under 'else'
else:
    print("You are a senior.")
```
### For loop
```python
# initialize a variable to store the sum
total = 0

# iterate over the first 10 positive integers and add them to the total
for i in range(1, 11):
    total += i

# print out the final total
print("The sum of the first 10 positive integers is:", total)
```
### While loop
```python
# initialize a counter variable
i = 1

# loop while the counter is less than or equal to 5
while i <= 5:
    print(i)
    i += 1
```

## Functions
In Python, you can define functions to encapsulate reusable pieces of code.
```python
# define a function to add two numbers
def add_numbers(x, y):
    result = x + y
    return result

# call the function with two arguments and store the result in a variable
sum = add_numbers(3, 5)

# print the result to the console
print("The sum of 3 and 5 is:", sum)
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
