# Class

```python
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

### `Static` Attribute
- Generally static attributes are defined to store constant values or business logic.
- Static attributes can be called by every `functions` defined inside a class irrespective of it's scope.

### `Instance` Method | Class Method

```python
import math
class Orientation():

    def __init__(self, x_pos, y_pos, degree):
        self.x_pos = x_pos # Positions
        self.y_pos = y_pos
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

### `Static` Method

```python
import math
class Orientation():
    pi = 3.14 # Static attribute
    
    def __init__(self, x_pos, y_pos, degree):
        self.x_pos = x_pos # Positions
        self.y_pos = y_pos
        self.x_dir, self.y_dir = Orientation.getUnitVectorFromDegree(degree) # Direction vectors
        
    # Static Method    
    def getUnitVectorFromDegree(degree):
        radians = (degree/180) * Orientation.pi
        return math.sin(radians), -math.cos(radians)
    
    # Instance Method
    def getNextPosition(self):
        return self.x_pos + self.x_dir, self.y_pos + self.y_dir
      
myOrientation = Orientation(5, 5, 75)      
```

### `Constructor`

```python
import math
class Orientation():
    pi = 3.14 # Static attribute
    
    def __init__(self, x_pos, y_pos, degree):
        self.x_pos = x_pos # Positions
        self.y_pos = y_pos
        self.x_dir, self.y_dir = self.getUnitVectorFromDegree(degree) # Direction vectors
        
    # Decorator        
    @staticmethod    
    def getUnitVectorFromDegree(degree): # Self is never passed as an argument for static methods.
        radians = (degree/180) * Orientation.pi
        return math.sin(radians), -math.cos(radians)
    
    # Class Method | Instance Method
    def getNextPosition(self):
        return self.x_pos + self.x_dir, self.y_pos + self.y_dir
      
myOrientation = Orientation(5, 5, 75)      
```

# Class `Inheritance`

### `Parent` Class

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

### `Child` Class

```python
class Maltese(Dog): # Dog Class is inherited.
    
    # Overwritting instance method: Modifying the method inherited from parent class.
    def speak(self):
        print(f'{self.name} says wow wow 🐩')
    
    # Extending instance methods: Adding new methods for new child class.
    def sit(self):
        print(f'{self.name} is sitting 🐕‍🦺')
        
    def wag(self):
        print(f'{self.name} is wagging tail 🐕')
```
