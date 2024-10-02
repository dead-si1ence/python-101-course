# 12-Hour Python Course for Beginners

## Class 1: Introduction to Python and Setup

### 1. What is Python? (10 minutes)

- Brief history and philosophy of Python
- Why Python is popular (readability, versatility, large community)
- Real-world applications of Python

### 2. Installing Python (20 minutes)

- Downloading Python from python.org
- Step-by-step installation guide for Windows, macOS, and Linux
- Verifying the installation using command line

```bash
python --version
```

### 3. Setting Up a Development Environment (20 minutes)

- Introduction to Integrated Development Environments (IDEs)
- Installing and setting up Visual Studio Code
- Installing the Python extension in VS Code

### 4. Your First Python Program (10 minutes)

- Creating a new Python file
- Writing and running "Hello, World!"

```python
print("Hello, World!")
```

- Understanding the print function and string literals

## Class 2: Python Basics - Part 1

### 1. Basic Syntax (15 minutes)

- Indentation and its importance
- Comments (single-line and multi-line)
- Continuation of lines

```python
# This is a single-line comment

"""
This is a
multi-line comment
"""

print("Hello, " + 
      "World!")  # Line continuation
```

### 2. Variables and Data Types (25 minutes)

- Creating and naming variables
- Python's dynamic typing
- Basic data types: int, float, str, bool

```python
age = 25        # int
height = 1.75   # float
name = "Alice"  # str
is_student = True  # bool

print(type(age))
print(type(height))
print(type(name))
print(type(is_student))
```

### 3. Basic Operators (20 minutes)

- Arithmetic operators (+, -, *, /, //, %, **)
- Comparison operators (==, !=, <, >, <=, >=)
- Logical operators (and, or, not)

```python
# Arithmetic
print(10 + 5)   # Addition
print(10 - 5)   # Subtraction
print(10 * 5)   # Multiplication
print(10 / 5)   # Division
print(10 // 3)  # Floor division
print(10 % 3)   # Modulus
print(2 ** 3)   # Exponentiation

# Comparison
print(10 == 10)  # Equal to
print(10 != 5)   # Not equal to
print(10 > 5)    # Greater than
print(10 < 5)    # Less than
print(10 >= 10)  # Greater than or equal to
print(10 <= 5)   # Less than or equal to

# Logical
print(True and False)  # Logical AND
print(True or False)   # Logical OR
print(not True)        # Logical NOT
```

## Class 3: Python Basics - Part 2

### 1. String Operations (20 minutes)

- String concatenation
- String methods (upper(), lower(), strip(), etc.)
- String formatting (f-strings)

```python
# Concatenation
first_name = "John"
last_name = "Doe"
full_name = first_name + " " + last_name
print(full_name)

# String methods
print(full_name.upper())
print(full_name.lower())
print("  hello  ".strip())

# String formatting
age = 30
print(f"{full_name} is {age} years old")
```

### 2. Input and Output (20 minutes)

- Using the input() function
- Handling different types of input
- Formatting output with print()

```python
name = input("What's your name? ")
age = int(input("How old are you? "))
height = float(input("What's your height in meters? "))

print(f"Name: {name}")
print(f"Age: {age}")
print(f"Height: {height:.2f} meters")
```

### 3. Type Conversion (20 minutes)

- Implicit vs. explicit type conversion
- Using int(), float(), str() functions
- Handling type conversion errors

```python
# Implicit conversion
x = 10
y = 3.14
z = x + y  # z will be a float
print(z)

# Explicit conversion
age_str = "25"
age_int = int(age_str)
print(age_int + 5)

# Handling errors
try:
    invalid_num = int("hello")
except ValueError:
    print("Cannot convert string to integer")
```

## Class 4: Control Flow - Conditional Statements

### 1. If Statements (20 minutes)

- Basic if statement syntax
- Using else and elif
- Nested if statements

```python
age = 20

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")

score = 85
if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
else:
    print("D")

# Nested if
is_weekend = True
is_sunny = False

if is_weekend:
    if is_sunny:
        print("Let's go to the beach")
    else:
        print("Let's watch a movie")
else:
    print("It's a work day")
```

### 2. Logical Operators in Conditions (20 minutes)

- Using and, or, not in if statements
- Short-circuit evaluation

```python
age = 25
has_license = True

if age >= 18 and has_license:
    print("You can drive")
else:
    print("You cannot drive")

is_weekend = False
is_holiday = True

if is_weekend or is_holiday:
    print("You can relax")
else:
    print("It's a work day")

is_working = True
if not is_working:
    print("Time to relax")
else:
    print("Keep working")
```

### 3. Ternary Operator (20 minutes)

- Understanding the ternary operator
- When to use it (and when not to)

```python
age = 20
status = "adult" if age >= 18 else "minor"
print(status)

# Equivalent to:
if age >= 18:
    status = "adult"
else:
    status = "minor"

# More complex example
x = 10
y = 20
larger = x if x > y else y
print(f"The larger number is: {larger}")
```

## Class 5: Control Flow - Loops

### 1. For Loops (25 minutes)

- Basic for loop syntax
- Looping through sequences (lists, strings)
- Using range() function

```python
# Looping through a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# Looping through a string
for char in "Python":
    print(char)

# Using range()
for i in range(5):
    print(i)

# Range with start and stop
for i in range(1, 6):
    print(i)

# Range with step
for i in range(0, 10, 2):
    print(i)
```

### 2. While Loops (20 minutes)

- Basic while loop syntax
- Using while loops for unknown iterations

```python
# Basic while loop
count = 0
while count < 5:
    print(count)
    count += 1

# While loop with user input
while True:
    response = input("Do you want to continue? (yes/no) ")
    if response.lower() != 'yes':
        break
```

### 3. Loop Control Statements (15 minutes)

- Using break, continue, and else in loops

```python
# Using break
for i in range(10):
    if i == 5:
        break
    print(i)

# Using continue
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)

# Using else with for loop
for i in range(5):
    print(i)
else:
    print("Loop completed normally")

# Using else with while loop
n = 0
while n < 5:
    print(n)
    n += 1
else:
    print("Loop completed normally")
```

## Class 6: Functions - Part 1

### 1. Defining and Calling Functions (20 minutes)

- Basic function syntax
- Function parameters and arguments
- Return values

```python
# Simple function
def greet():
    print("Hello, World!")

greet()

# Function with parameters
def greet_person(name):
    print(f"Hello, {name}!")

greet_person("Alice")

# Function with return value
def add(a, b):
    return a + b

result = add(3, 5)
print(result)
```

### 2. Default and Keyword Arguments (20 minutes)

- Setting default values for parameters
- Using keyword arguments

```python
# Default arguments
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()
greet("Alice")

# Keyword arguments
def create_profile(name, age, city):
    print(f"Name: {name}, Age: {age}, City: {city}")

create_profile(name="Bob", age=30, city="New York")
create_profile(age=25, city="London", name="Charlie")
```

### 3. Variable Scope (20 minutes)

- Local vs. global variables
- The global keyword

```python
# Local and global variables
x = 10  # Global variable

def print_x():
    x = 20  # Local variable
    print(f"Local x: {x}")

print_x()
print(f"Global x: {x}")

# Using the global keyword
def modify_global_x():
    global x
    x = 30
    print(f"Modified global x: {x}")

modify_global_x()
print(f"Global x after modification: {x}")
```

## Class 7: Functions - Part 2

### 1. Arbitrary Arguments (20 minutes)

- Using *args for variable-length positional arguments
- Using **kwargs for variable-length keyword arguments

```python
# *args example
def sum_all(*args):
    total = 0
    for num in args:
        total += num
    return total

print(sum_all(1, 2, 3, 4, 5))

# **kwargs example
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=30, city="New York")
```

### 2. Lambda Functions (20 minutes)

- Understanding lambda syntax
- Use cases for lambda functions

```python
# Simple lambda function
square = lambda x: x ** 2
print(square(5))

# Lambda with multiple arguments
sum = lambda a, b: a + b
print(sum(3, 5))

# Using lambda with built-in functions
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x ** 2, numbers))
print(squared_numbers)

# Lambda with filter
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)
```

### 3. Recursive Functions (20 minutes)

- Understanding recursion
- Writing recursive functions
- Pros and cons of recursion

```python
# Factorial using recursion
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))

# Fibonacci sequence using recursion
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

for i in range(10):
    print(fibonacci(i), end=" ")
```

## Class 8: Data Structures - Lists and Tuples

### 1. Lists (30 minutes)

- Creating and accessing lists
- List methods (append, extend, insert, remove, pop)
- List slicing

```python
# Creating lists
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]

# Accessing elements
print(fruits[0])  # First element
print(fruits[-1])  # Last element

# List methods
fruits.append("date")
fruits.extend(["elderberry", "fig"])
fruits.insert(1, "blueberry")
fruits.remove("cherry")
popped_fruit = fruits.pop()
print(fruits)
print(f"Popped fruit: {popped_fruit}")

# List slicing
print(numbers[1:4])  # Elements from index 1 to 3
print(numbers[:3])   # First three elements
print(numbers[2:])   # Elements from index 2 to the end
print(numbers[::2])  # Every second element
```

### 2. List Comprehensions (15 minutes)

- Understanding list comprehensions
- Creating lists using comprehensions

```python
# Simple list comprehension
squares = [x ** 2 for x in range(10)]
print(squares)

# List comprehension with condition
even_squares = [x ** 2 for x in range(10) if x % 2 == 0]
print(even_squares)

# Nested list comprehension
matrix = [[i * j for j in range(1, 4)] for i in range(1, 4)]
print(matrix)
```

### 3. Tuples (15 minutes)

- Creating and accessing tuples
- Tuple packing and unpacking
- Use cases for tuples

```python
# Creating tuples
point = (3, 4)
rgb = (255, 0, 0)

# Accessing tuple elements
print(point[0])
print(rgb[-1])

# Tuple packing and unpacking
coordinates = 5, 6  # Packing
x, y = coordinates  # Unpacking
print(f"x: {x}, y: {y}")

# Using tuples for multiple return values
def get_min_max(numbers):
    return min(numbers), max(numbers)

min_val, max_val = get_min_max([1, 5, 3, 9, 2])
print(f"Min: {min_val}, Max: {max_val}")
```

## Class 9: Data Structures - Sets and Dictionaries

### 1. Sets (25 minutes)

- Creating and using sets
- Set operations (union, intersection, difference)
- Set methods (add, remove, discard)

```python
# Creating sets
fruits = {"apple", "banana", "cherry"}
numbers = set([1, 2, 3, 4, 5])

# Adding and removing elements
fruits.add("date")
fruits.remove("banana")
fruits.discard("elderberry")  # No error if not found

# Set operations
set1 = {1, 2, 3, 4, 5}
set2 = {4, 5, 6, 7, 8}
print(set1.union(set2))
print(set1.intersection(set2))
print(set1.difference(set2))

# Checking membership
print("apple" in fruits)
```

### 2. Dictionaries (35 minutes)

- Creating and accessing dictionaries
- Dictionary methods (keys, values, items)
- Nested dictionaries

```python
# Creating dictionaries
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}

# Accessing and modifying values
print(person["name"])
person["age"] = 31
person["occupation"] = "Engineer"

# Dictionary methods
print(person.keys())
print(person.values())
print(person.items())

# Checking for key existence
if "age" in person:
    print(f"Age: {person['age']}")

# Get method with default value
print(person.get("height", "Not specified"))

# Nested dictionaries
employees = {
    "Alice": {"department": "HR", "salary": 50000},
    "Bob": {"department": "IT", "salary": 60000}
}

print(employees["Alice"]["salary"])

# Dictionary comprehension
squares = {x: x**2 for x in range(5)}
print(squares)
```

## Class 10: File Handling

### 1. Reading Files (20 minutes)

- Opening files using `open()`
- Reading entire file content
- Reading line by line

```python
# Reading entire file
with open("example.txt", "r") as file:
    content = file.read()
    print(content)

# Reading line by line
with open("example.txt", "r") as file:
    for line in file:
        print(line.strip())

# Reading specific number of characters
with open("example.txt", "r") as file:
    chunk = file.read(10)
    print(chunk)
```

### 2. Writing Files (20 minutes)

- Writing to files
- Appending to files
- Using `with` statement for file operations

```python
# Writing to a file
with open("output.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a new line.")

# Appending to a file
with open("output.txt", "a") as file:
    file.write("\nThis line is appended.")

# Writing multiple lines
lines = ["Line 1", "Line 2", "Line 3"]
with open("multiline.txt", "w") as file:
    file.writelines(line + "\n" for line in lines)
```

### 3. Working with CSV Files (20 minutes)

- Reading CSV files
- Writing CSV files
- Using the `csv` module

```python
import csv

# Reading CSV file
with open("data.csv", "r") as file:
    csv_reader = csv.reader(file)
    for row in csv_reader:
        print(row)

# Writing CSV file
data = [
    ["Name", "Age", "City"],
    ["Alice", "30", "New York"],
    ["Bob", "25", "London"]
]

with open("output.csv", "w", newline="") as file:
    csv_writer = csv.writer(file)
    csv_writer.writerows(data)

# Using DictReader and DictWriter
with open("data.csv", "r") as file:
    csv_reader = csv.DictReader(file)
    for row in csv_reader:
        print(row["Name"], row["Age"])

output_data = [
    {"Name": "Charlie", "Age": "35", "City": "Paris"},
    {"Name": "David", "Age": "28", "City": "Tokyo"}
]

with open("output_dict.csv", "w", newline="") as file:
    fieldnames = ["Name", "Age", "City"]
    csv_writer = csv.DictWriter(file, fieldnames=fieldnames)
    csv_writer.writeheader()
    csv_writer.writerows(output_data)
```

## Class 11: Object-Oriented Programming - Classes and Objects

### 1. Introduction to OOP Concepts (15 minutes)

- What is Object-Oriented Programming?
- Classes and objects
- Attributes and methods

### 2. Creating Classes and Objects (25 minutes)

- Defining a class
- Creating class attributes
- Instantiating objects

```python
class Dog:
    # Class attribute
    species = "Canis familiaris"

    # Constructor method
    def __init__(self, name, age):
        self.name = name
        self.age = age

    # Instance method
    def bark(self):
        return f"{self.name} says Woof!"

# Creating objects
buddy = Dog("Buddy", 5)
max = Dog("Max", 3)

print(buddy.name)
print(max.age)
print(buddy.bark())
print(Dog.species)
```

### 3. Methods and `self` (20 minutes)

- Instance methods
- Using `self` in methods
- Special methods (`__str__`, `__repr__`)

```python
class Circle:
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

    def circumference(self):
        return 2 * 3.14 * self.radius

    def __str__(self):
        return f"Circle with radius {self.radius}"

    def __repr__(self):
        return f"Circle({self.radius})"

c = Circle(5)
print(c.area())
print(c.circumference())
print(c)  # Uses __str__
print(repr(c))  # Uses __repr__
```

## Class 12: Object-Oriented Programming - Inheritance and Polymorphism

### 1. Inheritance (25 minutes)

- Concept of inheritance
- Creating child classes
- Overriding methods

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

dog = Dog("Buddy")
cat = Cat("Whiskers")

print(dog.speak())
print(cat.speak())
```

### 2. Polymorphism (20 minutes)

- Concept of polymorphism
- Method overriding
- Using polymorphism with functions

```python
def animal_sound(animal):
    return animal.speak()

print(animal_sound(dog))
print(animal_sound(cat))

# Polymorphism with built-in functions
numbers = [1, 2, 3]
string = "Hello"

print(len(numbers))
print(len(string))
```

### 3. Advanced OOP Concepts (15 minutes)

- Multiple inheritance
- Method Resolution Order (MRO)
- Abstract classes and interfaces (brief introduction)

```python
class A:
    def method(self):
        print("Method from A")

class B:
    def method(self):
        print("Method from B")

class C(A, B):
    pass

c = C()
c.method()  # Which method will be called?

print(C.mro())  # Method Resolution Order

from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side ** 2

# s = Shape()  # This will raise an error
square = Square(5)
print(square.area())
```
