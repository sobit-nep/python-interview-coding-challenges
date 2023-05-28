**api_integration.md**

## API Integration Coding Challenges

In this file, we will explore some coding challenges related to API integration in Python.

### Challenge 1: Making GET Requests

Write a Python code snippet that demonstrates making a GET request to an API and retrieving data.

**Example:**

```python
import requests

# Make a GET request to the API
url = "https://api.example.com/users"
response = requests.get(url)

# Process the response
if response.status_code == 200:
    data = response.json()
    # Do something with the data
    print(data)
else:
    print("Error:", response.status_code)
```

### Challenge 2: Making POST Requests

Write a Python code snippet that demonstrates making a POST request to an API and sending data.

**Example:**

```python
import requests

# Data to send in the request
data = {
    "name": "John Doe",
    "email": "johndoe@example.com"
}

# Make a POST request to the API
url = "https://api.example.com/users"
response = requests.post(url, json=data)

# Process the response
if response.status_code == 201:
    data = response.json()
    # Do something with the data
    print(data)
else:
    print("Error:", response.status_code)
```

### Challenge 3: Authentication and Authorization

Write a Python code snippet that demonstrates making a request to an authenticated API by including an access token in the headers.

**Example:**

```python
import requests

# Access token
access_token = "YOUR_ACCESS_TOKEN"

# Make a request to the authenticated API
url = "https://api.example.com/protected"
headers = {"Authorization": f"Bearer {access_token}"}
response = requests.get(url, headers=headers)

# Process the response
if response.status_code == 200:
    data = response.json()
    # Do something with the data
    print(data)
else:
    print("Error:", response.status_code)
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.