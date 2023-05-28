**oop.md**

## Object-Oriented Programming (OOP) Coding Challenges

In this file, we will explore some coding challenges related to Object-Oriented Programming (OOP) concepts in Python.

### Challenge 1: Create a Rectangle Class

Write a Python class `Rectangle` that represents a rectangle. The class should have methods to calculate the area (`calculate_area`) and perimeter (`calculate_perimeter`) of the rectangle.

```python
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width
        
    def calculate_area(self):
        return self.length * self.width
    
    def calculate_perimeter(self):
        return 2 * (self.length + self.width)
```

### Challenge 2: Create a Circle Class

Write a Python class `Circle` that represents a circle. The class should have methods to calculate the area (`calculate_area`) and circumference (`calculate_circumference`) of the circle.

```python
import math

class Circle:
    def __init__(self, radius):
        self.radius = radius
        
    def calculate_area(self):
        return math.pi * self.radius**2
    
    def calculate_circumference(self):
        return 2 * math.pi * self.radius
```

### Challenge 3: Create a Bank Account Class

Write a Python class `BankAccount` that represents a bank account. The class should have methods to deposit (`deposit`) and withdraw (`withdraw`) money from the account, as well as to check the current balance (`get_balance`).

```python
class BankAccount:
    def __init__(self):
        self.balance = 0
        
    def deposit(self, amount):
        self.balance += amount
        
    def withdraw(self, amount):
        if self.balance >= amount:
            self.balance -= amount
        else:
            raise ValueError("Insufficient funds")
            
    def get_balance(self):
        return self.balance
```

### Challenge 4: Create a Student Class

Write a Python class `Student` that represents a student. The class should have attributes for the student's name and age, as well as a method to calculate the grade (`calculate_grade`) based on a score.

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
    def calculate_grade(self, score):
        if score >= 90:
            return "A"
        elif score >= 80:
            return "B"
        elif score >= 70:
            return "C"
        elif score >= 60:
            return "D"
        else:
            return "F"
```

### Challenge 5: Create a Car Class

Write a Python class `Car` that represents a car. The class should have attributes for the car's make, model, and year, as well as methods to start the car (`start_engine`) and stop the car (`stop_engine`).

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.engine_started = False
        
    def start_engine(self):
        self.engine_started = True
        
    def stop_engine(self):
        self.engine_started = False
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.