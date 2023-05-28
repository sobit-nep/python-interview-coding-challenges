**functions.md**

## Function Coding Challenges

In this file, we will explore some coding challenges related to functions in Python.

### Challenge 1: Check Prime Number

Write a Python function that takes a number as input and returns `True` if it is a prime number, and `False` otherwise.

**Example:**

Input: 13

Output: True

```python
def is_prime(number):
    if number < 2:
        return False
    for i in range(2, int(number**0.5) + 1):
        if number % i == 0:
            return False
    return True
```

### Challenge 2: Calculate Factorial

Write a Python function that takes a number as input and returns its factorial using recursion.

**Example:**

Input: 5

Output: 120

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)
```

### Challenge 3: Reverse a List

Write a Python function that takes a list as input and returns a new list with the elements reversed.

**Example:**

Input: [1, 2, 3, 4, 5]

Output: [5, 4, 3, 2, 1]

```python
def reverse_list(lst):
    return lst[::-1]
```

### Challenge 4: Generate Fibonacci Numbers

Write a Python function that takes a number as input and returns a list of Fibonacci numbers up to that number.

**Example:**

Input: 8

Output: [0, 1, 1, 2, 3, 5, 8]

```python
def generate_fibonacci(n):
    fibonacci = [0, 1]
    while fibonacci[-1] + fibonacci[-2] <= n:
        fibonacci.append(fibonacci[-1] + fibonacci[-2])
    return fibonacci
```

### Challenge 5: Exponentiation

Write a Python function that takes two numbers as input, `base` and `exponent`, and returns the result of `base` raised to the power of `exponent`.

**Example:**

Input: base = 2, exponent = 3

Output: 8

```python
def exponentiation(base, exponent):
    return base ** exponent
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.
