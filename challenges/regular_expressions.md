**regular_expressions.md**

## Regular Expressions Coding Challenges

In this file, we will explore some coding challenges related to regular expressions in Python.

### Challenge 1: Validate Email Address

Write a Python function `validate_email` that takes an email address as input and validates it using regular expressions. The function should check if the email address is in a valid format (e.g., contains a valid username, domain, and top-level domain).

**Example:**

Input: `validate_email("example@example.com")`

Output: Valid email address

```python
import re

def validate_email(email):
    pattern = r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$'
    if re.match(pattern, email):
        print("Valid email address")
    else:
        print("Invalid email address")

# Test case
validate_email("example@example.com")
```

### Challenge 2: Extract Phone Numbers

Write a Python function `extract_phone_numbers` that takes a text as input and extracts all the phone numbers from it using regular expressions. The function should return a list of phone numbers found in the text.

**Example:**

Input: `extract_phone_numbers("Contact us at 123-456-7890 or 987-654-3210")`

Output: `['123-456-7890', '987-654-3210']`

```python
import re

def extract_phone_numbers(text):
    pattern = r'\d{3}-\d{3}-\d{4}'
    phone_numbers = re.findall(pattern, text)
    return phone_numbers

# Test case
numbers = extract_phone_numbers("Contact us at 123-456-7890 or 987-654-3210")
print(numbers)
```

### Challenge 3: Replace Words in a Text

Write a Python function `replace_words` that takes a text, a word to find, and a word to replace as input. The function should use regular expressions to find all occurrences of the word in the text and replace them with the provided replacement word.

**Example:**

Input: `replace_words("Hello, World! Welcome to the World of Python.", "World", "Universe")`

Output: `Hello, Universe! Welcome to the Universe of Python.`

```python
import re

def replace_words(text, find_word, replace_word):
    pattern = r'\b' + re.escape(find_word) + r'\b'
    replaced_text = re.sub(pattern, replace_word, text)
    return replaced_text

# Test case
replaced_text = replace_words("Hello, World! Welcome to the World of Python.", "World", "Universe")
print(replaced_text)
```

### Challenge 4: Validate Password Strength

Write a Python function `validate_password_strength` that takes a password as input and validates its strength using regular expressions. The function should check if the password meets certain criteria, such as having a minimum length, containing at least one uppercase letter, one lowercase letter, and one digit.

**Example:**

Input: `validate_password_strength("Password123")`

Output: Strong password

```python
import re

def validate_password_strength(password):
    pattern = r'^(?=.*[a-z])(?=.*[A-Z])(?=.*\d).{8,}$'
    if re.match(pattern, password):
        print("Strong password")
    else:
        print("Weak password")

# Test case
validate_password_strength("Password123")
```
You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.