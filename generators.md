 # Generators

- Creates an iterator.
- Used for large data set which requires hight memory.

### Generator Function:

```python
fruits = ['apple', 'banana', 'orange', 'pineapple', 'grapes', 'kiwi', 'apricot', 'mango']

def contains_i(words):
    for word in words:
        if 'i' in word:
            yield word
  
print(list(contains_i(fruits)))
```

```output
# Output: ['pineapple', 'kiwi', 'apricot']
```
```python
deg square(n):
    for i in range(1, n):
        yield i ** 2
        
print(list(square(10)))
```      

```output
# Output: [1, 4, 9, 16, 25, 36, 49, 64, 81]
```

### Generator Expression:

- Comprehensions are faster.
- Comprehensions are single line codes.
- Expressions saves memory. 

```python
# Creating list comprehension:
list_comprehension = [n ** 2 for n in range(1, 10)]

# Output: [1, 4, 9, 16, 25, 36, 49, 64, 81]
```
```python
import sys
sys.getsizeof(list_comprehension)

# Output: 21516
```

```python
# Creating generator object:
generator_expression = (n ** 2 for n in range(1, 10)

# 
sys.getsizeof(generator_expression)
# Output: 56
```

```python
# Converting into list:
list(generator_expression)
# Output: [1, 4, 9, 16, 25, 36, 49, 64, 81]
```
