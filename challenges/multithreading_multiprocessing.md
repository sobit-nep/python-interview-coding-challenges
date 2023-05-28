**multithreading_multiprocessing.md**

## Multithreading and Multiprocessing Coding Challenges

In this file, we will explore some coding challenges related to multithreading and multiprocessing in Python.

### Challenge 1: Multithreading

Write a Python code snippet that demonstrates creating multiple threads to perform concurrent tasks.

**Example:**

```python
import threading

# Function to perform the task
def task(name):
    print(f"Thread {name} is running")

# Create multiple threads
threads = []
for i in range(5):
    t = threading.Thread(target=task, args=(i,))
    threads.append(t)
    t.start()

# Wait for all threads to finish
for t in threads:
    t.join()
```

### Challenge 2: Multiprocessing

Write a Python code snippet that demonstrates creating multiple processes to perform parallel tasks.

**Example:**

```python
import multiprocessing

# Function to perform the task
def task(name):
    print(f"Process {name} is running")

# Create multiple processes
processes = []
for i in range(5):
    p = multiprocessing.Process(target=task, args=(i,))
    processes.append(p)
    p.start()

# Wait for all processes to finish
for p in processes:
    p.join()
```

### Challenge 3: Synchronization

Write a Python code snippet that demonstrates using locks for thread synchronization.

**Example:**

```python
import threading

# Shared variable
counter = 0

# Create a lock
lock = threading.Lock()

# Function to increment the counter
def increment():
    global counter
    for _ in range(100000):
        with lock:
            counter += 1

# Create multiple threads
threads = []
for _ in range(5):
    t = threading.Thread(target=increment)
    threads.append(t)
    t.start()

# Wait for all threads to finish
for t in threads:
    t.join()

# Print the final counter value
print(f"Counter value: {counter}")
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.