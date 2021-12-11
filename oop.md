# Object Oriented Programming

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
```

### `_x` : `protected` attribute (one underscore)
- Can be accessed using `instance`

### `__x` : `private` attribute (double underscore)
- Cannot be accessed using `instance`
