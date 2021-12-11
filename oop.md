# Object Oriented Programming

- `Python` is an object oriented programming language.
- Almost everything in Python is an `object`
- `str()`, `int()`... are the constructor functions.

```python
# string
print(type("a string"))

# integer
print(type(5))

# float
print(type(5.0))

# list
print(type([1, 2, 3]))

# tuple
print(type((1, 2, 3)))

# set
print(type({1, 2, 3}))

# dictionary
print(type({1 : "Kirankumar", 2 : 25, 3 : "Data Scientist"}))

-------------------------------------------------------------
Output :
-------------------------------------------------------------
<class 'str'>
<class 'int'>
<class 'float'>
<class 'list'>
<class 'tuple'>
<class 'set'>
<class 'dict'>

# Constructor Functions

int(2.5) = 2
str(5) = "5"
float(7) = 7.0
```


### `class` 
- Blueprint | Template for creating `objects`
- Attributes | Properties | Variables 
- Behavior | Action | Member `Function` or `Methods`

```python 
class Employee(object):
    pass
```

### `object`
- `Instance` of class, that can store value (information) 

```python
emp1 = Employee()
```     

### `__init__()`
- Special Constructor or Special Method or Magic Function
- `__init__()` function is called automatically whenever we create objects from the class.
- The arguments or parameters passed with `__init__()` are called `instance attributes`

```python
    def __init__(self, name, age, email, designation):
```

### `self`
- A reference to the current `instance` (attributes and methods) of the class.
- Used to access or reference `attributes` and `methods` of class.

```python 
class Employee(object):

    def __init__(self, name, age, email, designation)
    self.name = name
    self.age = age 
    self.email = email
    self.designation = designation
    
instance attributes : name, age, email, designation    
object will be created with initial values passed to the instance attributes
```

### `method`
- `Functions` that belongs to an object are called methods.
- Simply `functions` inside `classes`

### `Inheritance`
- `Base` Class + `Child` Class

### `Encapsulation`
- `_x` : `protected` attribute and method | `Single` underscore | Can be accessed using `instance`
- `__x` : `private` attribute and method | `Double` underscore | Cannot be accessed using `instance`

### `Properties`
- `Getter` / `Setter`
