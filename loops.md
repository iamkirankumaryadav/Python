# Loops

## `While`

- While loop uses an conditional expression to control the loop.
- When the condition is `True` the body of the loop is executed.
- Loop continues as long as the condition is `True`
- When the condition is `False` the loop ends and the lines of code after the loop is executed.

```python
secret = 'fish123'
pwd = ''

while pwd != secret:
    pwd = input("What is the secret word ?")
```

# `For`

- For loop uses a sequence, like an iterator ( List, Tuple, Set, Dictionary ) to control the loop.
- The body of the loop is executed for each item in the sequence.
- When the sequence is completed the loop ends.

```python
# Sequence | Collection
animals = ('bear', 'bunny', 'dog', 'cat')

# Loop
for animal in animals:
    print(pet)
```

# Clause 

## `Continue`
- Continue clause is used to shortcut a loop.
- Starts it again as if it had reached the end of its body.

## `Break`
- The break clause is used to break out of the loop ( Terminate )

```python
secret = 'alpha123'
passcode = ''
auth = False
attempt_count = 0
max_attempt = 5

while passcode != secret:
    attempt_count += 1
    if attempt_count > max_attempt: break
    passcode = input(f'{attempt_count}: What is the secret passcode ?')
else:
    auth = True

print("Authorized" if auth else "Calling Police...🚓🚨")
```
