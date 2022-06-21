# Generators

- Creates an iterator.
- Used for large data set which requires hight memory.

### Generator Function:

```python
fruits = ['apple', 'banana', 'orange', 'pineapple', 'grapes', 'kiwi', 'apricot', 'mango']

def contains_i(words):
  i_words = []
  for word in words:
    if 'i' in word:
      i_words.append(word)
  return i_words
  
print(contains_i(fruits)
```

```output
# Output : ['pineapple', 'kiwi', 'apricot']
```      
