### Important Concepts 

### `Flag`
- A flag in Python acts as a signal | `True` or `False`
- We can set the flag to `True` and the program runs continuosly until any event makes it `False`

```python
prompt = "Display something"
prompt += "\nEnter 'quit' to end the program"

# Here active is a flag
active = True
while active:
    message = input(prompt)
    
    if message == 'quit':
        active = False
    else:
        print(message)
```

### `Indexing`

1. `Forward` Indexing: Starting from 0, 1, 2.....
2. `Reverse` Indexing: Starting from -1, -2, -3...

### `Slicing`

Default Slicing 
- `[:index]` (First index is considered as `0` by default)
- `[index:length of the collection]` (Last index is considered as the length of collection)
