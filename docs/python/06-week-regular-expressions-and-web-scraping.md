---
sidebar_position: 6
---

# Regular Expressions and Web Scraping

Regex, 're' module, web scraping, BeautifulSoup, requests

- Introduction to regular expressions
- The 're' module
- Web scraping basics
- Using BeautifulSoup and requests

## 1. Regular expressions (regex):

- A sequence of characters that defines a search pattern
- Used for pattern matching and manipulation of strings
- Use the 're' module to work with regular expressions
  Example:

```python
import re

pattern = r"\d+"
text = "There are 42 apples and 7 oranges."
numbers = re.findall(pattern, text)
print(numbers)  # Output: ['42', '7']
```

## 2. Common regex patterns:

- \d: digit (0-9)
- \w: word character (letter, digit, or underscore)
- \s: whitespace character (space, tab, or newline)
- .: any character except newline
- +: one or more occurrences
- \*: zero or more occurrences
- ?: zero or one occurrence

## 3. Web scraping:

- Extracting data from websites
- Use the 'requests' module to make HTTP requests and retrieve web page content
- Use the 'BeautifulSoup' library to parse HTML content
  Example:

```python
import requests
from bs4 import BeautifulSoup

url = "https://example.com"
response = requests.get(url)
soup = BeautifulSoup(response.text, "html.parser")
print(soup.title.text)  # Output: The title of the web page
```

## 4. Navigating the HTML tree with BeautifulSoup:

- Accessing tags: soup.tag_name
- Accessing attributes: tag['attribute_name']
- Accessing text: tag.text or tag.get_text()
- Finding tags: soup.find() and soup.find_all()
  Example:

```python
html = """
<html>
    <body>
        <h1>Welcome to my website!</h1>
        <p class="intro">This is an example paragraph.</p>
        <p class="content">This is another paragraph.</p>
    </body>
</html>
"""
soup = BeautifulSoup(html, "html.parser")
paragraphs = soup.find_all("p")
for p in paragraphs:
    print(p.text)
# Output:
# This is an example paragraph.
# This is another paragraph.
```
