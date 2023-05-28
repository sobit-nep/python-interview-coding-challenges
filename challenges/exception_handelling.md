**exception_handling.md**

## Exception Handling Coding Challenges

In this file, we will explore some coding challenges related to exception handling in Python.

### Challenge 1: Divide by Zero

Write a Python function `divide_numbers` that takes two numbers as input and returns their division. Handle the `ZeroDivisionError` exception and print a custom error message if the second number is zero.

**Example:**

Input: `divide_numbers(10, 2)`

Output: `Result: 5.0`

```python
def divide_numbers(num1, num2):
    try:
        result = num1 / num2
        print("Result:", result)
    except ZeroDivisionError:
        print("Error: Division by zero is not allowed")

# Test cases
divide_numbers(10, 2)
divide_numbers(5, 0)
```

### Challenge 2: File Not Found

Write a Python function `read_file` that takes a file name as input and reads the content of the file. Handle the `FileNotFoundError` exception and print a custom error message if the file does not exist.

**Example:**

Input: `read_file("sample.txt")`

Output: File not found: sample.txt

```python
def read_file(filename):
    try:
        with open(filename, 'r') as file:
            content = file.read()
        print(content)
    except FileNotFoundError:
        print("File not found:", filename)

# Test cases
read_file("existing_file.txt")
read_file("non_existing_file.txt")
```

### Challenge 3: Value Error

Write a Python function `calculate_square_root` that takes a number as input and calculates its square root. Handle the `ValueError` exception and print a custom error message if the input number is negative.

**Example:**

Input: `calculate_square_root(16)`

Output: Square root: 4.0

```python
import math

def calculate_square_root(number):
    try:
        if number < 0:
            raise ValueError("Input number cannot be negative")
        result = math.sqrt(number)
        print("Square root:", result)
    except ValueError as e:
        print("Error:", str(e))

# Test cases
calculate_square_root(16)
calculate_square_root(-9)
```

### Challenge 4: Index Error

Write a Python function `get_list_element` that takes a list and an index as input and returns the element at the specified index. Handle the `IndexError` exception and print a custom error message if the index is out of range.

**Example:**

Input: `get_list_element([1, 2, 3, 4, 5], 2)`

Output: Element at index 2: 3

```python
def get_list_element(lst, index):
    try:
        element = lst[index]
        print("Element at index", index, ":", element)
    except IndexError:
        print("Error: Index out of range")

# Test cases
get_list_element([1, 2, 3, 4, 5], 2)
get_list_element([1, 2, 3, 4, 5], 10)
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.