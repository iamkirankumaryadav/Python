# 🐍 Python `bool` (Boolean) — Explained in the Simplest Way

Think of a **Boolean (`bool`)** as a **Yes/No question**.

A Boolean can have **only two values**:

* ✅ `True`
* ❌ `False`

That's it.

---

# 🧠 Real-Life Analogy

Imagine a light switch 💡.

```text
Switch ON  → True
Switch OFF → False
```

There is no middle state.

Similarly, in Python:

```python
is_light_on = True
```

or

```python
is_light_on = False
```

---

# Why do we need Boolean?

Computers constantly make decisions.

Examples:

* Is the user logged in?
* Is the password correct?
* Is the payment successful?
* Is the student passed?
* Is the age greater than 18?

Every answer is either:

```text
Yes  → True
No   → False
```

---

# Creating Boolean Values

```python
is_logged_in = True

is_admin = False
```

---

# Checking the Data Type

```python
is_logged_in = True

print(type(is_logged_in))
```

Output

```python
<class 'bool'>
```

---

# Boolean from Comparisons ⭐

Most Booleans come from comparisons.

Suppose

```python
age = 25
```

---

## Equal To (`==`)

```python
print(age == 25)
```

Output

```text
True
```

---

```python
print(age == 18)
```

Output

```text
False
```

---

## Greater Than (`>`)

```python
print(age > 18)
```

Output

```text
True
```

---

## Less Than (`<`)

```python
print(age < 18)
```

Output

```text
False
```

---

## Greater Than or Equal (`>=`)

```python
print(age >= 25)
```

Output

```text
True
```

---

## Less Than or Equal (`<=`)

```python
print(age <= 20)
```

Output

```text
False
```

---

## Not Equal (`!=`)

```python
print(age != 18)
```

Output

```text
True
```

---

# Comparison Operators

| Operator | Meaning               |
| -------- | --------------------- |
| `==`     | Equal                 |
| `!=`     | Not Equal             |
| `>`      | Greater Than          |
| `<`      | Less Than             |
| `>=`     | Greater Than or Equal |
| `<=`     | Less Than or Equal    |

---

# Boolean with `if` Statements ⭐⭐⭐

```python
age = 20

if age >= 18:
    print("You can vote.")
```

Output

```text
You can vote.
```

Python checks:

```text
20 >= 18

↓

True

↓

Execute the code
```

---

# Logical Operators

Suppose

```python
age = 25
salary = 70000
```

---

## `and`

Both conditions must be **True**.

```python
print(age > 18 and salary > 50000)
```

Output

```text
True
```

Think of entering a company:

```text
Age > 18 ✅
ID Card Available ✅

↓

Entry Allowed ✅
```

---

## `or`

At least one condition must be **True**.

```python
print(age > 18 or salary > 100000)
```

Output

```text
True
```

Think of a movie offer:

```text
Student OR Senior Citizen

↓

Discount Available
```

You only need one condition.

---

## `not`

Reverses the result.

```python
is_logged_in = True

print(not is_logged_in)
```

Output

```text
False
```

---

# Truth Table (Interview Favorite ⭐)

## `and`

| A     | B     | Result  |
| ----- | ----- | ------- |
| True  | True  | ✅ True  |
| True  | False | ❌ False |
| False | True  | ❌ False |
| False | False | ❌ False |

---

## `or`

| A     | B     | Result  |
| ----- | ----- | ------- |
| True  | True  | ✅ True  |
| True  | False | ✅ True  |
| False | True  | ✅ True  |
| False | False | ❌ False |

---

## `not`

| A     | Result |
| ----- | ------ |
| True  | False  |
| False | True   |

---

# Truthy and Falsy Values ⭐⭐⭐

In Python, not everything is explicitly `True` or `False`.

Some values behave as **False**.

---

## Falsy Values

```python
bool(0)
```

Output

```text
False
```

---

```python
bool("")
```

Output

```text
False
```

---

```python
bool([])
```

Output

```text
False
```

---

```python
bool({})
```

Output

```text
False
```

---

```python
bool(None)
```

Output

```text
False
```

---

## Truthy Values

```python
bool(10)
```

Output

```text
True
```

---

```python
bool("Python")
```

Output

```text
True
```

---

```python
bool([1,2,3])
```

Output

```text
True
```

---

# Quick Summary

| Value     | Boolean |
| --------- | ------- |
| `0`       | False   |
| `1`       | True    |
| `""`      | False   |
| `"Hello"` | True    |
| `[]`      | False   |
| `[1]`     | True    |
| `{}`      | False   |
| `{"a":1}` | True    |
| `None`    | False   |

---

# Converting to Boolean

```python
print(bool(100))
```

Output

```text
True
```

---

```python
print(bool(0))
```

Output

```text
False
```

---

```python
print(bool(""))
```

Output

```text
False
```

---

```python
print(bool("Google"))
```

Output

```text
True
```

---

# Boolean and Integers

Python treats:

```python
True
```

as

```text
1
```

and

```python
False
```

as

```text
0
```

Example

```python
print(True + True)
```

Output

```text
2
```

---

```python
print(True + False)
```

Output

```text
1
```

Although this works, it's usually better to use booleans for logic rather than arithmetic.

---

# Where Are Booleans Used?

Everywhere!

Examples:

* 🔐 Login successful?
* 💳 Payment completed?
* 📧 Email verified?
* 🚗 Seat belt fastened?
* 📦 Product in stock?
* 🎓 Student passed?
* 🌐 Internet connected?

All of these are either:

```text
True

or

False
```

---

# Time Complexity 🚀

| Operation  | Time |
| ---------- | ---- |
| Comparison | O(1) |
| `and`      | O(1) |
| `or`       | O(1) |
| `not`      | O(1) |
| `bool()`   | O(1) |

---

# Interview Tips ⭐

1. ✅ A Boolean has only **two values**: `True` and `False`.
2. ✅ Comparisons always return a Boolean.
3. ✅ Use `and` when **all** conditions must be true.
4. ✅ Use `or` when **at least one** condition must be true.
5. ✅ Use `not` to reverse a Boolean value.
6. ✅ Empty collections, `0`, `None`, and empty strings are **falsy**.
7. ✅ Non-empty collections, non-zero numbers, and non-empty strings are generally **truthy**.

---

# 🧠 Memory Trick

Think of a **Boolean** as a **door lock 🚪**.

```text
Door Locked? 🔒

Yes  → True

No   → False
```

Or a traffic signal:

```text
🟢 Go  → True

🔴 Stop → False
```

A Boolean is always a **decision**.

---

# 🎯 Formula to Remember

> **`bool` = True or False + Used for Decisions**

---

# 📊 Comparison of Basic Data Types

| Data Type | Example    | Used For        |
| --------- | ---------- | --------------- |
| `int`     | `25`       | Whole numbers   |
| `float`   | `25.5`     | Decimal numbers |
| `str`     | `"Python"` | Text            |
| `bool`    | `True`     | Decisions       |

---

# 💡 Interview Question

### Q: What is the difference between `=` and `==`?

This is one of the most common beginner interview questions.

```python
age = 25
```

* `=` means **assignment**.
* It stores the value `25` in the variable `age`.

```python
print(age == 25)
```

* `==` means **comparison**.
* It checks whether `age` is equal to `25`.

Output:

```text
True
```

### Easy way to remember:

* `=` → **Assign**
* `==` → **Compare**
