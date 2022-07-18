# Class

`Class` is a blueprint | template of a real world entity.

```python
# Defining class:
class Vehicle(): 
    wheels = 4 # Static attribute | Class attribute
    _doors = 4 # Private attribute (Should not be modified)
    
    def __init__(self, name): # Instance attribute
        self.name = name
        
    def getDoors(self): # Getter function (Access private attribute)
        return self._doors          
        
    def drive(self): # Function defined inside class (Method)
        print("🚗...")
```

### `Object`

- `Object` is an instance of `class`

```python
car1 = Vehicle(name = 'Range Rover Sport')

# car1: Object | Instance
# Vehicle: Class
# name: Parameter
# Range Rover Sport: Argument
```

### `Constructors`

- `Constructors` are generally used for instantiating an object.
- `__init__()` method is the `constructor` called automatically when an object is created.

```python
# Default Constructor:
    def __init__(self):
        pass
    
# Parameterized constructor:
    def __init__(self, first_name, last_name):
        self.first_name = first_name
        self.last_name = last_name
```

### `Destructor`
- `Destructors` are called when an object gets destroyed.
- `Destructors` are not needed in Python unlike C++.
- Python has an inbuilt garbage collector that handles memory management automatically. 

```python
# Destructor:
    def __del__(self):
        pass
```

### `Static` Attribute | `Class` Variable

- `Variables` or `Attribute` assigned in the class declaration.
- Generally static attributes are defined to store constant values or business logic.
- Static attributes can be called by every `functions` defined inside a class irrespective of it's scope.

### `Instance` Attribute | `Instance` Variable

- `Variables` or `Attributes` that are assigned inside methods are `instance` variables.

### `Instance` Method 

- `Function` defined inside an class which can be accessed and modified by every created `instance` (object) of that class.
- `Instance` method takes `self` as a first parameter.

```python
import math
class Orientation():

    def __init__(self, x_pos, y_pos, degree):
        self.x_pos = x_pos # Instance Variable | Insatnce Attribute
        self.y_pos = y_pos # Instance Variable | Instance Attribute
        self.x_dir, self.y_dir = self.getUnitVectorFromDegree(degree) # Direction vectors
        
    # Instance Method    
    def getUnitVectorFromDegree(self, degree): # Getter function
        radians = (degree/180) * self.pi
        return math.sin(radians), -math.cos(radians)
    
    # Instance Method
    def getNextPosition(self):
        return self.x_pos + self.x_dir, self.y_pos + self.y_dir
      
myOrientation = Orientation(5, 5, 75)      
```

### `Class` Method

- `Class` method is bound to the class and not the object of the class.
- `Class` method takes `cls` as the first parameter. 
- `@classmethod` decorator in used to create a `class` method.
- They can access only the class parameters and not the object instance attributes.

### `Static` Method

- `Static` method is also a method that is bound to the class and not the object of the class.
- While defining a `static` method, we don't need to pass `self` as first parameter.
- `@staticmethod` decorator in used to create a `static` method.


```python
from datetime import date

class Person: 

    def __init__(self, name, age): # Instance attribute.
        self.name = name
        self.age = age
 
    # Class method to create a person object by birth year.
    @classmethod
    def fromBirthYear(cls, name, year): # cls is passed as first parameter.
        return cls(name, date.today().year - year)
 
    # Static method to check if a person is adult or not.
    @staticmethod
    def isAdult(age): # No need to pass self as first parameter.
        return age > 18
 
 
person1 = Person('Kirankumar', 25)
person2 = Person.fromBirthYear('Kirankumar', 1996)
 
print(person1.age)
print(person2.age)
 
# print the result
print(Person.isAdult(26))

# Output:
25
26
True
```

### `Decorators`

- `Decorators` modify the behaviour of `function` or `class`
- Decorator `@classmethod` is used to create a `class` method. 
- Decorator `@staticmethod` is used to create a `static` method.

# Class `Inheritance`

### `Parent` Class | `Base` Class | `Super` Class

```python
class Dog():
    _legs = 4 # Static attribute
    
    def __init__(self, name):
        self.name = name
        
    def speak(self):
        print(f'{self.name} says bow bow 🐶')
        
    def getLegs(self):
        return self._legs
```            

### `Child` Class | `Derived` Class | `Sub` Class

```python
class Maltese(Dog): # Child class "Maltese" inherits parent class "Dog".

    # Super Function : Inherit instance attributes from parent and extend with new instance attributes. 
    def __init__(self, name, breed):
        super().__init__(self, name): 
            self.breed = breed        
    
    # Method Overriding: Overwritting or modifying the instance method inherited from parent class.
    def speak(self):
        print(f'{self.name} says wow wow 🐩')
    
    # Extending instance methods: Adding new methods for child class.
    def sit(self):
        print(f'{self.name} is sitting 🐕‍🦺')
        
    def wag(self):
        print(f'{self.name} is wagging tail 🐕')
```

### `Method` Overloading

- Instance methods defined with same name but different parameters
