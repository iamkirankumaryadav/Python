# Class

```python
class Vehicle():
    wheels = 4 # Static attribute | Class attribute
    
    def __init__(self, name): # Instance attribute
        self.name = name
        
    def drive(self):
        print("🚗...")
```

### `Static` Attribute
- Generally static attributes are defined to store constant values or business logic.
- Static attributes can be called by every `functions` defined inside a class irrespective of it's scope.
