**recursion.md**

## Recursion Coding Challenges

In this file, we will explore some coding challenges related to recursion in Python.

### Challenge 1: Factorial

Write a Python function `factorial` that takes a positive integer as input and computes its factorial using recursion.

**Example:**

Input: `factorial(5)`

Output: `120`

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

# Test case
result = factorial(5)
print(result)
```

### Challenge 2: Fibonacci Numbers

Write a Python function `fibonacci` that takes a positive integer as input and returns the nth Fibonacci number using recursion.

**Example:**

Input: `fibonacci(7)`

Output: `13`

```python
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

# Test case
result = fibonacci(7)
print(result)
```

### Challenge 3: Sum of Digits

Write a Python function `sum_of_digits` that takes a positive integer as input and calculates the sum of its digits using recursion.

**Example:**

Input: `sum_of_digits(12345)`

Output: `15`

```python
def sum_of_digits(n):
    if n == 0:
        return 0
    else:
        return n % 10 + sum_of_digits(n // 10)

# Test case
result = sum_of_digits(12345)
print(result)
```

### Challenge 4: Binary Search

Write a Python function `binary_search` that takes a sorted list of integers and a target value as input. The function should use recursion to perform a binary search and return the index of the target value in the list, or -1 if the value is not found.

**Example:**

Input: `binary_search([1, 2, 3, 4, 5], 3)`

Output: `2`

```python
def binary_search(arr, target, low, high):
    if low > high:
        return -1
    else:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] > target:
            return binary_search(arr, target, low, mid - 1)
        else:
            return binary_search(arr, target, mid + 1, high)

# Test case
arr = [1, 2, 3, 4, 5]
result = binary_search(arr, 3, 0, len(arr) - 1)
print(result)
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.
