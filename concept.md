### Important concepts that we never give attention to

### `Module`
`.py` file

### `Package`
- Collection of `Modules`
- Must contain `.init.py` file

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
