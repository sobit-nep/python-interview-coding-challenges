**generators_iterators.md**

## Generators and Iterators Coding Challenges

In this file, we will explore some coding challenges related to generators and iterators in Python.

### Challenge 1: Fibonacci Generator

Write a Python generator function `fibonacci_generator` that generates an infinite sequence of Fibonacci numbers.

**Example:**

```python
def fibonacci_generator():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b

# Usage
fib_gen = fibonacci_generator()
for _ in range(10):
    print(next(fib_gen))
```

### Challenge 2: Range Iterator

Write a Python class `RangeIterator` that implements an iterator for a given range of numbers.

**Example:**

```python
class RangeIterator:
    def __init__(self, start, stop):
        self.current = start
        self.stop = stop

    def __iter__(self):
        return self

    def __next__(self):
        if self.current >= self.stop:
            raise StopIteration
        value = self.current
        self.current += 1
        return value

# Usage
range_iter = RangeIterator(1, 6)
for num in range_iter:
    print(num)
```

### Challenge 3: Prime Number Generator

Write a Python generator function `prime_number_generator` that generates an infinite sequence of prime numbers.

**Example:**

```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def prime_number_generator():
    n = 2
    while True:
        if is_prime(n):
            yield n
        n += 1

# Usage
prime_gen = prime_number_generator()
for _ in range(10):
    print(next(prime_gen))
```

### Challenge 4: Custom Iterator

Write a Python class `CustomIterator` that implements a custom iterator for a given list of elements.

**Example:**

```python
class CustomIterator:
    def __init__(self, elements):
        self.elements = elements
        self.index = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.index >= len(self.elements):
            raise StopIteration
        value = self.elements[self.index]
        self.index += 1
        return value

# Usage
custom_iter = CustomIterator(['a', 'b', 'c', 'd'])
for elem in custom_iter:
    print(elem)
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.