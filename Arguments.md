# **Arguments**

### **1. Positional Arguments**
- Values passed into a function based on the order in which the parameters were listed during the function definition.

```python
def team(name, project):
    print(name, "is working on an", project)
    
team("Kirankumar", "Automatic Label Validation")
```

### **2. Keyword arguments**

- Keyword arguments (named arguments) are values that, when passed into a function, are identifiable by specific parameter names. 
- A keyword argument is preceded by a parameter and the assignment operator, =

```python
def team(name, project):
    print(f'{name} is working on an {project}')

team(project = "Kirankumar", name = 'Automatic Label Validation')
```       

