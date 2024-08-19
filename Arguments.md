# **Arguments**

```python
def function_name(parameter1, parameter2): # Parameters are defined when the function is declared.
    return parameter1 + parameter2

function_name(argument1, argument2) # Arguments are declared when the function is called.
```

### **1. Positional Arguments**
- Arguments are passed according to the order in which the parameters were listed during the function definition.

```python
def team(name, project):
    print(name, "is working on an", project)
    
team("Kirankumar", "Automatic Label Validation")
```

### **2. Keyword arguments**
- A keyword argument is preceded by a parameter and the assignment operator `=`

```python
def team(name, project):
    print(f'{name} is working on an {project}')

team(name = "Kirankumar", project = 'Automatic Label Validation')
```       
