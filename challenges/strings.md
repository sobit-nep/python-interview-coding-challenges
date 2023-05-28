**strings.md**

## String Coding Challenges

In this file, we will explore some coding challenges related to strings in Python.

### Challenge 1: Reverse a String

Write a Python function that takes a string as input and returns the reverse of the string.

**Example:**

Input: "Hello, World!"

Output: "!dlroW ,olleH"

```python
def reverse_string(string):
    return string[::-1]
```

### Challenge 2: Check Palindrome

Write a Python function that checks if a given string is a palindrome. A palindrome is a word, phrase, number, or other sequence of characters that reads the same backward as forward.

**Example:**

Input: "racecar"

Output: True

```python
def is_palindrome(string):
    return string == string[::-1]
```

### Challenge 3: Count Character Occurrences

Write a Python function that takes a string and a character as input and returns the number of occurrences of that character in the string.

**Example:**

Input: "Hello, World!", character = "l"

Output: 3

```python
def count_occurrences(string, character):
    count = 0
    for char in string:
        if char == character:
            count += 1
    return count
```

### Challenge 4: Remove Duplicate Characters

Write a Python function that takes a string as input and returns a new string with duplicate characters removed. The order of characters should be preserved.

**Example:**

Input: "Hello, World!"

Output: "Helo, Wrd"

```python
def remove_duplicates(string):
    unique_chars = []
    for char in string:
        if char not in unique_chars:
            unique_chars.append(char)
    return ''.join(unique_chars)
```

### Challenge 5: Check Anagrams

Write a Python function that takes two strings as input and checks if they are anagrams. Anagrams are words or phrases formed by rearranging the letters of another word or phrase.

**Example:**

Input: "listen", "silent"

Output: True

```python
def are_anagrams(string1, string2):
    return sorted(string1) == sorted(string2)
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.