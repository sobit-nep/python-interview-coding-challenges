**file_handling.md**

## File Handling Coding Challenges

In this file, we will explore some coding challenges related to file handling in Python.

### Challenge 1: Count Lines in a File

Write a Python program that takes a file name as input and counts the number of lines in the file.

**Example:**

Input: "file.txt"

Output: Number of lines: 10

```python
def count_lines(filename):
    with open(filename, 'r') as file:
        lines = file.readlines()
    return len(lines)
```

### Challenge 2: Copy File

Write a Python program that takes two file names as input, source file and destination file, and copies the contents of the source file to the destination file.

**Example:**

Input: Source file: "source.txt", Destination file: "destination.txt"

```python
def copy_file(source_file, destination_file):
    with open(source_file, 'r') as source:
        content = source.read()
    with open(destination_file, 'w') as destination:
        destination.write(content)
```

### Challenge 3: Read and Print File Content

Write a Python program that takes a file name as input and reads the content of the file, then prints it to the console.

**Example:**

Input: "file.txt"

```python
def read_and_print_file(filename):
    with open(filename, 'r') as file:
        content = file.read()
    print(content)
```

### Challenge 4: Append Content to a File

Write a Python program that takes a file name and a string as input, and appends the string to the end of the file.

**Example:**

Input: File: "file.txt", Content: "Hello, World!"

```python
def append_to_file(filename, content):
    with open(filename, 'a') as file:
        file.write(content)
```

### Challenge 5: Count Words in a File

Write a Python program that takes a file name as input and counts the number of words in the file.

**Example:**

Input: "file.txt"

Output: Number of words: 50

```python
def count_words(filename):
    with open(filename, 'r') as file:
        words = file.read().split()
    return len(words)
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.