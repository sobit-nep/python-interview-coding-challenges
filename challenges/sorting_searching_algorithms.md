**sorting_searching_algorithms.md**

## Sorting and Searching Algorithms Coding Challenges

In this file, we will explore some coding challenges related to sorting and searching algorithms in Python.

### Challenge 1: Bubble Sort

Write a Python function `bubble_sort` that takes a list of integers as input and sorts it using the Bubble Sort algorithm.

**Example:**

Input: `bubble_sort([5, 2, 8, 1, 9])`

Output: `[1, 2, 5, 8, 9]`

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n - 1):
        for j in range(n - 1 - i):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr

# Test case
result = bubble_sort([5, 2, 8, 1, 9])
print(result)
```

### Challenge 2: Binary Search

Write a Python function `binary_search` that takes a sorted list of integers and a target value as input. The function should perform a binary search and return the index of the target value in the list, or -1 if the value is not found.

**Example:**

Input: `binary_search([1, 2, 3, 4, 5], 3)`

Output: `2`

```python
def binary_search(arr, target):
    low = 0
    high = len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1

# Test case
arr = [1, 2, 3, 4, 5]
result = binary_search(arr, 3)
print(result)
```

### Challenge 3: Merge Sort

Write a Python function `merge_sort` that takes a list of integers as input and sorts it using the Merge Sort algorithm.

**Example:**

Input: `merge_sort([5, 2, 8, 1, 9])`

Output: `[1, 2, 5, 8, 9]`

```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    result.extend(left[i:])
    result.extend(right[j:])
    return result

# Test case
result = merge_sort([5, 2, 8, 1, 9])
print(result)
```

### Challenge 4: Linear Search

Write a Python function `linear_search` that takes a list of integers and a target value as input. The function should perform a linear search and return the index of the target value in the list, or -1 if the value is not found.

**Example:**

Input: `linear_search([5, 2, 8, 1,9])`
Output: `[1, 2, 5, 8, 9]`
```python
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1

# Test case
arr = [5, 2, 8, 1, 9]
result = linear_search(arr, 8)
print(result)
```

### Challenge 5: Quick Sort

Write a Python function `quick_sort` that takes a list of integers as input and sorts it using the Quick Sort algorithm.

**Example:**

Input: `quick_sort([5, 2, 8, 1, 9])`

Output: `[1, 2, 5, 8, 9]`

```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)

# Test case
result = quick_sort([5, 2, 8, 1, 9])
print(result)
```

### Challenge 6: Binary Search Tree

Implement a Binary Search Tree class in Python that supports insertion, deletion, and searching of values.

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

class BinarySearchTree:
    def __init__(self):
        self.root = None

    def insert(self, value):
        if self.root is None:
            self.root = Node(value)
        else:
            self._insert_recursive(self.root, value)

    def _insert_recursive(self, node, value):
        if value < node.value:
            if node.left is None:
                node.left = Node(value)
            else:
                self._insert_recursive(node.left, value)
        else:
            if node.right is None:
                node.right = Node(value)
            else:
                self._insert_recursive(node.right, value)

    def search(self, value):
        return self._search_recursive(self.root, value)

    def _search_recursive(self, node, value):
        if node is None or node.value == value:
            return node
        if value < node.value:
            return self._search_recursive(node.left, value)
        else:
            return self._search_recursive(node.right, value)

    def delete(self, value):
        self.root = self._delete_recursive(self.root, value)

    def _delete_recursive(self, node, value):
        if node is None:
            return node
        if value < node.value:
            node.left = self._delete_recursive(node.left, value)
        elif value > node.value:
            node.right = self._delete_recursive(node.right, value)
        else:
            if node.left is None:
                return node.right
            elif node.right is None:
                return node.left
            min_node = self._find_min(node.right)
            node.value = min_node.value
            node.right = self._delete_recursive(node.right, min_node.value)
        return node

    def _find_min(self, node):
        while node.left is not None:
            node = node.left
        return node
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.