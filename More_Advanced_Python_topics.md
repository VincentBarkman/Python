# Python Advanced Concepts

This tutorial covers some advanced concepts in Python programming language. Python is a high-level, interpreted, and general-purpose programming language known for its readability and simplicity.

## Table of Contents

1. [List Comprehension](#list-comprehension)
2. [Lambda Functions](#lambda-functions)
3. [Error Handling](#error-handling)
4. [Classes and Objects](#classes-and-objects)
5. [Inheritance](#inheritance)
6. [File Handling](#file-handling)
7. [Decorators](#decorators)
8. [Context Managers](#context-managers)
9. [Multiprocessing](#multiprocessing)

## List Comprehension

List comprehensions provide a concise way to create lists. It consists of an expression followed by a `for` statement inside square brackets.

```python
# Without list comprehension
squares = []
for x in range(10):
    squares.append(x ** 2)

# With list comprehension
squares = [x ** 2 for x in range(10)]

# List comprehension with a condition
even_squares = [x ** 2 for x in range(10) if x % 2 == 0]

# Lambda Functions

Lambda functions are small, anonymous functions that are defined using the lambda keyword. They can have any number of arguments but only one expression.

```python
# Regular function
def add(x, y):
    return x + y

# Lambda function
add_lambda = lambda x, y: x + y

result = add_lambda(3, 5)
print(result)  # Output: 8
```

# Error Handling

Errors can be handled using try and except blocks. When an error occurs, the code inside the except block will be executed.

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("You can't divide by zero!")

# Multiple exceptions can be caught in a single `except` block
try:
    x = 10 / 'a'
except (TypeError, ZeroDivisionError):
    print("An error occurred!")
```
# Classes and Objects

Classes are user-defined types that allow you to create objects with specific attributes and methods.

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print("Woof!")

# Create a Dog object
my_dog = Dog("Buddy", 3)

# Access attributes and call methods
print(my_dog.name)  # Output: Buddy
my_dog.bark()  # Output: Woof!
```
# Inheritance

Inheritance allows you to create a new class that inherits the attributes and methods from a parent class.

```python
class Animal:
    def __init__(self, species):
        self.species = species

    def speak(self):
        print("Some generic animal sound")

class Cat(Animal):
    def __init__(self, name):
        super().__init__("Cat")
        self.name = name

    def speak(self):
        print("Meow!")

# Create a Cat object
my_cat = Cat("Whiskers")

# Call the inherited and overridden methods
print(my_cat.species)  # Output: Cat
my_cat.speak()  # Output: Meow!
```

# File Handling

Python has built-in functions for reading and writing files. The most common way to work with files is by using the with statement.

```python
# Reading a file
with open("example.txt", "r") as file:
    content = file.read()
    print(content)

# Writing a file
with open("output.txt", "w") as
file:
    file.write("This is an example.")

# Appending to a file
with open("output.txt", "a") as file:
    file.write("\nThis is an appended line.")

# Reading a file line by line
with open("example.txt", "r") as file:
    for line in file:
        print(line.strip())

# Working with CSV files
import csv

# Reading a CSV file
with open("example.csv", "r") as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print(row)

# Writing a CSV file
with open("output.csv", "w") as csvfile:
    writer = csv.writer(csvfile)
    writer.writerow(["Name", "Age", "City"])
    writer.writerow(["Alice", 30, "New York"])

# Working with JSON files
import json

# Reading a JSON file
with open("example.json", "r") as jsonfile:
    data = json.load(jsonfile)
    print(data)

# Writing a JSON file
with open("output.json", "w") as jsonfile:
    data = {"name": "Alice", "age": 30, "city": "New York"}
    json.dump(data, jsonfile)
    ```

## Decorators

Decorators are a way to modify or enhance a function or method without changing its source code. They are functions that take another function as input and return a new function.

```python
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

def say_hello():
    print("Hello!")

decorated_say_hello = my_decorator(say_hello)
decorated_say_hello()

# Using the decorator syntax
@my_decorator
def say_goodbye():
    print("Goodbye!")

say_goodbye()
```
## Context Managers

Context managers simplify the management of resources, such as file handling, sockets, or database connections. They are typically used with the with statement to ensure that resources are properly acquired and released.

```python
class MyContextManager:
    def __enter__(self):
        print("Entering the context")
        return self

    def __exit__(self, exc_type, exc_value, traceback):
        print("Exiting the context")

with MyContextManager() as cm:
    print("Inside the context")

# Using contextlib for simpler context managers
from contextlib import contextmanager

@contextmanager
def my_context_manager():
    print("Entering the context")
    yield
    print("Exiting the context")

with my_context_manager():
    print("Inside the context")
```

## Multiprocessing

Multiprocessing allows you to run multiple tasks concurrently, taking advantage of multiple CPU cores. The multiprocessing module provides an easy way to parallelize tasks.

```python
import multiprocessing

def worker(number):
    print(f"Worker {number} is running")

if __name__ == "__main__":
    processes = []

    for i in range(5):
        process = multiprocessing.Process(target=worker, args=(i,))
        processes.append(process)
        process.start()

    for process in processes:
        process.join()

    print("All workers have finished.")
    ```
