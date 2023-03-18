# `OOP` : Object Oriented Programming

- `Python` is an object oriented programming language.
- Every real world entity is an `object`, almost everything in Python is an `object`
- OOP allows us to write code that is `repeatable`, `well organized` and `memory efficient`
```
e.g. x = 5 

# We want to store a data i.e. 5, 5 is stored in a computer memory at a particular hexadecimal memory address.
# Remembering the hexadecimal memory address will be very complicated for the developer to manage data.
# We will access the memory address to store and retrieve data, so we map the address with a meaningful variable name.
# We create an integer object with value = 5 and assign its memory address to a variable x.
# Data type, value, reference count and other informations are associated with object, variable just holds the memory address.
```
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

### `Class` 
- `Blueprint` | `Template` for `real world entities` and creating `objects` 
- Defines `Attributes` | `Properties` | `Variables` and `Behavior` | `Action` | Member `Function` or `Methods`

Every class has three essential components:
1. `Identity` : Unique name to identify the object ( class Person  )
2. `Property` : Attributes | Data ( About the object: Name, Gender, Age, Height, Weight )
3. `Method` : Behaviour | Action | Operation ( What the object can do? Read, Write, Walk, Run, Study, Teach )

```python 
class Employee(object):
    pass
```

```python

# Person is a class name
class Person:

    # Special Method or Constructor Method | class Person has two properties name and age.
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    # class Person has method introduce.
    def introduce(self):
        print(f"Hi, my name is {self.name} and I'm {self.age} years old.")

```

### `Instantiate`
- Calling a `class` to create an `object`

```python
emp1 = Employee()
```

### `Object`
- `Instance` of class, that can store value (information) 
- e.g. If Smartphone is a **Class** then Apple, Samsung, Motorola, Oneplus are instances.

```python
emp1 = Employee()

# emp1 is an object name. 
# Employee is the class name.
```     

### `Constructor` Method | Special Method
- Automatically the method is called whenever an `object` is created.
- `Default Constructor` : Constructor with `no` parameters | arguments

```python
def __init__(self, name, age):
    self.name = name
    self.age = age
```

### `__init__()`
- `Special Constructor` or `Constructor Method` or `Special Method` or `Magic Method` or `Init Method`
- `Attributes` are initialized in `__init__()`
- Defined automatically when we create any class object, and automatically invokes whenever an object is created.
- `__init__()` function is executed automatically with every new class instance.
- The arguments or parameters passed with `__init__()` are called `instance attributes`
- First parameter will always be a variable `self`

### `Instantiate` an object
- Process of creating an `object` ( Instance of a class ) is called `instantiation`
- Every new object `instance` is located at a different memory address.
- The process to **create** an `object` is similar to a `function call` ( ObjectName = ClassName() )

### `Function`

``` Python
# Define Function:
def function_name(argument1, argument2):
    pass
    
# Call Function:
function_name(parameter1, parameter2)
```        

```python
def greet(name):
    print(f'Good Morning {name}')
    
print(greet(name='Kirankumar'))    
```
```
# Output:
Good Morning Kirankumar
None
```
`None`: When a function doesn't return anything, we get None.

```python
def greet(name):
    return f'Good Morning {name}'
    
print(greet(name='Kirankumar'))    
```
```
# Output:
Good Morning Kirankumar
```

### Position of `Arguments`

```Python
def example(arg_1, arg_2, *args, **kwargs):
```

### `Method`
- `Function` defined inside body of a `class`
- Defines `action` or `behaviour` of an object.

```python
    def __init__(self, name, age, email, designation):
```

### `Self`
- A reference to the current `instance` ( attributes and methods ) of the class.
- Used to access or reference `attributes` and `methods` of class.
- `self` provides a flexibility to call the `instance attributes` in any method defined inside the class irrespective of it's scope.

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

### `Method`
- `Functions` that belongs to an object are called `methods` or Simply `functions` defined inside `class` are `methods`
```python
name = 'Kirankumar' # String object "name" is created.

name.upper() # upper() is the method of string object.
```

## `Principles` of OOP : `APIE`
1. `Abstraction`
2. `Polymorphism`
3. `Inheritance`
4. `Encapsulation`

### `Abstraction`
- `Show` only important information and `hide` internal implementation details from users.
- e.g. Mobile can do many things like make a call, take pictures, play games, watch movies, etc.
- It doesn't show the inside process of how its doing the things (Implementation parts are hidden)

### `Polymorphism`
- Having more than one form.
- In Python we can use the same function on different data types or different sequence or collections.
- Allow to call methods of base class in derived class.
- e.g A person at same time is a father, a husband, an employee and behaves accordingly.
- Same `method` name but different `attributes` or number of parameters.

```python
# Same function can be used to count the characters in a string as well as number of items in a list

len("Kirankumar") : 10

len([1, 2, 3, 4, 5]) : 5
```
### `Inheritance`
- `Parent` Class or `Base` Class or `Super` Class
- `Child` Class or `Derived` Class or `Sub` Class
- `Inherit` the `attributes` ( properties ) and `methods` ( behaviour ) from base class to a new derived class.
- `Inheritance` enables us to `create` a new `class` from existing class by adding new functionality to it or simply modifying it.
- The pre existing class is known as a `Base Class` and the newly defined class is known as a `Derived Class`
- To inherit `__init__()` method of the `parent class` inside derived class, use `super().__init__()`

### `Multiple` Inheritance

- A `class` can be `derived` from more than one `base class`

``` Python
class Base1:
    pass

class Base2:
    pass

class MultiDerived(Base1, Base2):
    pass
```

### `Multi Level` Inheritance
- Inherit from `derived class`
- Features of `base class` and `derived class` are inherited into a `new derived class`

``` Python
class Base:
    pass

class Derived1(Base):
    pass

class Derived2(Derived1):
    pass
```

### `Method Overriding`
- When the `__init__()` method is defined inside `derived` class, it `overrides` the `base` class

``` Python
class Base:
    pass
  
class Derived(Base):
    pass

```

### `Encapsulation`
- `_x` : `protected` attribute and method | `Single` underscore | Can be accessed using `instance`
- `__x` : `private` attribute and method | `Double` underscore | Cannot be accessed using `instance`
- `Bind` together the `data`, `attributes` and `methods` ( Class = Data + Properties + Behaviour )
- `Restrict` access to methods, attributes and variables of Class.
- `Prevents` data from direct `modification`
- e.g. A company has several departments Production, HR, Accounts, Marketing.
- All these departments makes up a company, and each department has it's own purpose and actions.
- We denote `private attribute` using single underscore `_` and a `protected attribute` using double underscore `__`

### `Properties`
- `Getter` / `Setter`
- Pythonic way to `set` and `get` protected attributes. 

### `Decorator`
- Decorator modify or extend the behaviour of a `Function` or `Class` without permanently modifying it.

### `First Class Objects`
- Functions are `First Class Objects` : Can be used or passed as `arguments`
- Function is an `instance` of `Object type`
- Function can be stored in a `variable`
- Function can be created inside a function
- Function can be passed as a `parameter` to another function
- Function can be returned as a result from another function

```python
def uppercase(text):
    return text.upper()
 
capital = uppercase     # Storing function in a variable
 
print(capital('Hello'))
-----------------------
Output :
-----------------------
HELLO
-----------------------

def adder(x):
    def add(y):         # Creating a function inside function
        return x + y 
    return adder        # Returning function as a result
 
add15 = adder(15)
print(add15(10))
-----------------------
Output :
-----------------------
25
```

### Important Concepts in Class
1. Define a `class`
2. Instantiate an `object` a `class`
3. Use `attributes` and `methods` to define the `properties` and `behaviors` of an object.
4. Use `inheritance` to create `child classes` from a `parent class`
5. Reference a method in a `parent class` using `super()`
6. Check if an `object` inherits from another class using `isinstance()`

### Benefits of Object Oriented Programming
- Makes Program **easy** to understand.
- Class is **sharable**, code can be **reused**.
- Data is **safe** and **secure** with **data abstraction**.

### Operator Overloading in Python
- Same operator behaves differently with different `data types` according to **context**.
- (**+**) Operator will perform **arithmetic addition** on two numbers, **merge** two lists and **concatenate** two strings.
- But it does not performs same operations on **user defined class**
- we need to implement **\_\_add\_\_()** function in the class.

### `Python Memory Management`
- Python manages its memory using private `heap space`
- `Objects` are stored in `heap` ( Inaccessible to the programmers )
- In built `garbage collector` to `recycle` the unused memory for the `private heap space`

### `break`
- `Terminates` the `loop` and control flows to the statement after the body of loop.

### `continue`
- `Terminates` current iteration of the statement, `skips` the rest of the code in current iteration
- Control flows to the next iteration of the Loop.

### `pass`
- Empty statement just used to bypass the error situation.

### `Generators`
- Functions that returns an `iterable collection` of items on which we can apply loop or control flow.

### `help()`
- Display `documentation` of `modules`, `classes`, `functions` and `keywords`

### `dir()`
- List of valid `attributes` and `methods` of an object based on its datatype and state.

### Overloading Arithmetic and Logical Operators 

| Operator            | Expression	| Special Function        |
| :---                | :---:       | :---:                   |
| Addition            | p1 + p2	    | p1.\_\_add\_\_(p2)      |
| Subtraction         |	p1 - p2	    | p1.\_\_sub\_\_(p2)      | 
| Multiplication      |	p1 * p2	    | p1.\_\_mul\_\_(p2)      | 
| Power               |	p1 ** p2	| p1.\_\_pow\_\_(p2)      |
| Division            |	p1 / p2	    | p1.\_\_truediv\_\_(p2)  |
| Floor Division      |	p1 // p2	| p1.\_\_floordiv\_\_(p2) | 
| Remainder (modulo)  |	p1 % p2	    | p1.\_\_mod\_\_(p2)      |
| Bitwise Left Shift  |	p1 << p2	| p1.\_\_lshift\_\_(p2)   | 
| Bitwise Right Shift | p1 >> p2	| p1.\_\_rshift\_\_(p2)   |
| Bitwise AND         | p1 & p2	    | p1.\_\_and\_\_(p2)      |
| Bitwise OR          | p1 \| p2    | p1.\_\_or\_\_(p2)       |
| Bitwise XOR         |	p1 ^ p2	    | p1.\_\_xor\_\_(p2)      |
| Bitwise NOT         | ~p1	        | p1.\_\_invert\_\_()     |

### Overloading Comparison Operators 

| Operator	               | Expression | Special Functions     |
| :---                     | :---:      | :---:                 |
| Less than	               | p1 < p2	| p1.\_\_lt\_\_(p2)     |
| Less than or equal to    | p1 <= p2	| p1.\_\_le\_\_(p2)     |
| Equal to	               | p1 == p2	| p1.\_\_eq\_\_(p2)     |
| Not equal to	           | p1 != p2	| p1.\_\_ne\_\_(p2)     | 
| Greater than	           | p1 > p2	| p1.\_\_gt\_\_(p2)     |
| Greater than or equal to | p1 >= p2	| p1.\_\_ge\_\_(p2)     |

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

