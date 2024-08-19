# **Function**

### **User-Defined Function**

### **Parameter vs Argument**
- Parameter: **Defined** with function
- Argument: Passed as value during the **function call**.

``` Python
def function(parameter1, parameter2):
    """
    This is a Doctstring
    """
    print("The Message")

greet(argument1, argument2)
```

### **Arbitrary Arguments**
- When we don't know how many arguments we will pass.

``` Python
def greet(*people):
    """
    Docstring
    parameters (data type): about parameter
    """

    # people is an iterator with arguments (list, tuple, set, string)
    for name in people:
        print("Hello", name)

greet("Kirankumar", "Paramveer", "Gaurav", "Pranit")
```

### **Global Keyword**
- Variable created **inside** a function is a **local** variable by default.
- Variable created **outside** a function is a **global** variable by default.
- Keyword **gobal** is used to declare **global** variable inside a function.

```python
# global variable:
c = 1 

def add():
    # use of global keyword:
    global c
    # increment c by 2:
    c = c + 2 
    print(c)

add()
```
