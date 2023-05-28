**control_flow.md**

## Control Flow Coding Challenges

In this file, we will explore some coding challenges related to control flow in Python.

### Challenge 1: Find the Largest of Three Numbers

Write a Python program that takes three numbers as input and returns the largest among them.

**Example:**

Input: 5, 9, 3

Output: 9

```python
def find_largest(num1, num2, num3):
    if num1 >= num2 and num1 >= num3:
        return num1
    elif num2 >= num1 and num2 >= num3:
        return num2
    else:
        return num3
```

### Challenge 2: Check Odd or Even

Write a Python program that takes a number as input and prints whether it is odd or even.

**Example:**

Input: 7

Output: Odd

```python
def check_odd_even(number):
    if number % 2 == 0:
        return "Even"
    else:
        return "Odd"
```

### Challenge 3: Roots of a Quadratic Equation

Write a Python program that takes the coefficients of a quadratic equation (`a`, `b`, and `c`) as input and prints the roots of the equation.

**Example:**

Input: a = 2, b = -5, c = 2

Output: Roots: 2.0, 0.5

```python
import cmath

def find_roots(a, b, c):
    discriminant = (b**2) - (4*a*c)
    root1 = (-b - cmath.sqrt(discriminant)) / (2*a)
    root2 = (-b + cmath.sqrt(discriminant)) / (2*a)
    return root1, root2
```

### Challenge 4: Calculate Factorial Using a Loop

Write a Python program that takes a number as input and calculates its factorial using a loop.

**Example:**

Input: 5

Output: Factorial: 120

```python
def calculate_factorial(n):
    factorial = 1
    for i in range(1, n + 1):
        factorial *= i
    return factorial
```

### Challenge 5: Print Fibonacci Series

Write a Python program that takes a number as input and prints the Fibonacci series up to that number.

**Example:**

Input: 10

Output: Fibonacci Series: 0, 1, 1, 2, 3, 5, 8

```python
def print_fibonacci_series(n):
    fibonacci = [0, 1]
    while fibonacci[-1] <= n:
        fibonacci.append(fibonacci[-1] + fibonacci[-2])
    return fibonacci[:-1]
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.