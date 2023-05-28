**web_scraping.md**

## Web Scraping Coding Challenges

In this file, we will explore some coding challenges related to web scraping in Python.

### Challenge 1: Extracting Data from HTML

Write a Python code snippet that demonstrates extracting data from an HTML page using a web scraping library like Beautiful Soup.

**Example:**

```python
import requests
from bs4 import BeautifulSoup

# Fetch the HTML page
url = "https://example.com"
response = requests.get(url)
html_content = response.text

# Create a BeautifulSoup object
soup = BeautifulSoup(html_content, "html.parser")

# Extract data from the HTML
title = soup.title.text
paragraphs = soup.find_all("p")

# Print the extracted data
print("Title:", title)
print("Paragraphs:")
for p in paragraphs:
    print(p.text)
```

### Challenge 2: Scraping Dynamic Content

Write a Python code snippet that demonstrates scraping dynamic content from a website that relies on JavaScript to load data.

**Example:**

```python
import requests
from bs4 import BeautifulSoup

# Fetch the HTML page
url = "https://example.com"
response = requests.get(url)
html_content = response.text

# Create a BeautifulSoup object
soup = BeautifulSoup(html_content, "html.parser")

# Find the element that contains the dynamic content
dynamic_element = soup.find("div", {"id": "dynamic-content"})

# Extract the data from the dynamic element
data = dynamic_element.text

# Print the extracted data
print("Dynamic Content:", data)
```

### Challenge 3: Extracting Data from APIs

Write a Python code snippet that demonstrates extracting data from an API using the requests library.

**Example:**

```python
import requests

# Make a GET request to the API
url = "https://api.example.com/users"
response = requests.get(url)

# Extract data from the response
data = response.json()

# Process the data
for user in data:
    print("User:", user["name"])
    print("Email:", user["email"])
    print("Username:", user["username"])
    print()
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.