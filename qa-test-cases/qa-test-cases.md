# QA Test Cases

------------
These should render: (provide absolute paths to the test cases that need them):
------------

# PNG files:
![alt text](checkmark.png)

# Space in name, enclosed in <>:
![alt text](<check mark.png>)

# <img> format properties
![alt text](checkmark.png){width="200" height="200"}

# Optional title
![alt text](checkmark.png "title")

# Missing alt text
![](checkmark.png)

# file:// URIs (Linux/MacOS)
**Need absolute path**
![alt text](file:///path/to/checkmark.png)

# file:// URIs (Windows)
**Need absolute path**
![alt text](file://C:/path/to/checkmark.png)

# Absolute paths (Linux/MacOS)
**Need absolute path**
![alt text](/path/to/checkmark.png)

# Absolute paths (Windows)
**Need absolute path**
![alt text](C:/path/to/checkmark.png)

# Relative paths
![alt text](../checkmark.png)

# JPG files
![alt text](checkmark.jpg)

# GIF files
![alt text](checkmark.gif)

# Remote URLs
![alt text](https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)

# Word wrap
![alt text](checkmark.png){width="200" height="200"}, but with sublime's Word Wrap enabled,
and as long of a line as necessary as needed to wrap. The image should appear
below the entire wrapped line, not interleaved with it.

------------
These should not render, but not cause any problems:
------------

# Space in name, not enclosed in <>
![alt text](check mark.png)

# File that does not exist
![alt text](missing-file.png)

# URL that does not exist
![alt text](https://www.google.com/doesnotexist2222.png)

# Unsupported image format (local)
![alt text](checkmark.svg)

# Unsupported image format (remote)
![alt text](https://api.travis-ci.org/xsleonard/go-merkle.svg)