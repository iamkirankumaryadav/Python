# `os` module

```python
import os

# Get current working directory.
os.getcwd()                 

# Basename of current working file.
print(f'Basename: {os.path.basename(__file__)}')  

# Absolute path of current working directory
os.path.abspath(__file__)   

# Directory name
os.path.dirname(__file__)   

Output :
/User/Kirankumar/Python/os.py
Basename: os.py
/User/Kirankumar/Python/os.py
/User/Kirankumar/Python
```

`Relative Path`
- Path with reference to only `current directory`
```html
<img src="logo.png">
```

`Absolute Path`
- Path with reference to `root directory`
```html
<img src="https://www.unsplash.com/images/logo.png">
```
