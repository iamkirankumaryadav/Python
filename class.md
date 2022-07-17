# Class

```python
class Vehicle():
    wheels = 4 # Static attribute | Class attribute
    _doors = 4 # Private attribute
    
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
