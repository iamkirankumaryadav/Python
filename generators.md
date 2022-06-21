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
# Output : 
['pineapple', 'kiwi', 'apricot']
```
```python
deg square(n):
    for i in range(1, n):
        yield i ** 2
        
print(list(square(10)))
```      

```output
# Output:
[1, 4, 9, 16, 25, 36, 49, 64, 81]
```
