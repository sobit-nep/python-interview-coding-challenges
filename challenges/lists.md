**lists.md**

## List Coding Challenges

In this file, we will explore some coding challenges related to lists in Python.

### Challenge 1: Find Maximum and Minimum

Write a Python function that takes a list of numbers as input and returns the maximum and minimum numbers in the list.

**Example:**

Input: [5, 9, 3, 1, 7]

Output: Maximum: 9, Minimum: 1

```python
def find_max_min(numbers):
    maximum = max(numbers)
    minimum = min(numbers)
    return maximum, minimum
```

### Challenge 2: Calculate Sum and Average

Write a Python function that takes a list of numbers as input and returns the sum and average of the numbers.

**Example:**

Input: [2, 4, 6, 8, 10]

Output: Sum: 30, Average: 6.0

```python
def calculate_sum_average(numbers):
    total_sum = sum(numbers)
    average = total_sum / len(numbers)
    return total_sum, average
```

### Challenge 3: Remove Duplicates

Write a Python function that takes a list as input and returns a new list with duplicate elements removed. The order of elements should be preserved.

**Example:**

Input: [1, 2, 3, 2, 4, 1, 5]

Output: [1, 2, 3, 4, 5]

```python
def remove_duplicates(numbers):
    unique_numbers = []
    for num in numbers:
        if num not in unique_numbers:
            unique_numbers.append(num)
    return unique_numbers
```

### Challenge 4: Sort a List

Write a Python function that takes a list of numbers as input and returns a new list with the numbers sorted in ascending order.

**Example:**

Input: [5, 2, 8, 1, 9]

Output: [1, 2, 5, 8, 9]

```python
def sort_list(numbers):
    return sorted(numbers)
```

### Challenge 5: Find the Second-Largest Element

Write a Python function that takes a list of numbers as input and returns the second-largest element in the list.

**Example:**

Input: [5, 9, 3, 1, 7]

Output: 7

```python
def find_second_largest(numbers):
    sorted_numbers = sorted(numbers)
    return sorted_numbers[-2]
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.