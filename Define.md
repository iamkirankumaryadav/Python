## `Constants`, `Classes`, `Methods`, `Protected Methods` and `Dunder Methods`
```python
# Get all the predefined constants, classes and methods in a module:
dir(module)
```

## `Constants`

- Constants are defined with all characters in `uppercase`
- Find all the `constants` defined inside a module.

```python
# Define Constant:
COMPANY_NAME

# Find all Constants defined in a module:
print(list(filter(lambda c : c.isupper(), dir(module))))
```

## `Classes`

- Classes are defined with first character in `uppercase`
- Find all the `classes` defined inside a module.

```python
# Define Class:
def Class_Name(object):

# Find all Classes defined in a module:
print(list(filter(lambda c : c.istitle(), dir(module))))
```

## `Function`

- `Functions` are defined with `lowercase`
- Find all the `Functions` defined inside a module.

```python
# Define Function:
def function_name(argument1, argument2):

# Call Function:
function_name(parameter1, parameter2)

# Find all Functions defined in a module:
print(list(filter(lambda c : c.islower(), dir(module))))
```

## `Methods`

- `Methods` are defined with `lowercase`
- Find all the `methods` defined inside a module.

```python
# Define Method:
def method_name():

# Call Method:
object.method_name()

# Find all Methods defined in a module:
print(list(filter(lambda c : c.islower(), dir(module))))
```

### `Dunder Methods`

- Methods defined which starts and ends with `__` ( Double underscore )
- Find all the `dunder methods` defined inside a module.

```python
# Define Dunder Method:
def `__init__(self)`

# Find all the dunder methods defined in a module:
print(list(filter(lambda c : c.startswith('__'), dir(module))))
```

### `Protected Methods`

- Methods defined which starts with `_` ( Single Underscore )
- Find all the `protected methods` defined inside a module.

```python
# Define Protected Method:
def _calculate_salary(self):

# Find all the protected methods in a module:
print(list(filter(lambda c : c.startswith('_') and not c.startswith('__'), dir(module))))
``` 

