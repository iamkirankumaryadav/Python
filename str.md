# 🐍 Python `str` (String) — Explained in the Simplest Way

Think of a **String (`str`)** as **text**.

Anything written inside **quotes** (`' '` or `" "`) is a **string**.

Examples:

* 👤 Name → `"Kiran"`
* 🌍 Country → `"India"`
* 📧 Email → `"abc@gmail.com"`
* 📱 Phone Number → `"9876543210"` *(stored as text, not for calculations)*

---

# 🧠 Real-Life Analogy

Imagine writing on a piece of paper.

```text
Name : Kiran
City : Mumbai
Company : Google
```

Everything written on the paper is **text**.

Python stores text as a **String**.

---

# Creating a String

Using double quotes:

```python
name = "Kiran"

print(name)
```

Output

```text
Kiran
```

Using single quotes:

```python
city = 'Mumbai'
```

Both are exactly the same.

---

# Checking the Data Type

```python
name = "Kiran"

print(type(name))
```

Output

```python
<class 'str'>
```

---

# A String Can Contain Anything

```python
name = "Kiran"

age = "30"

phone = "9876543210"

address = "Mumbai, India"
```

Even though `"30"` looks like a number...

It is actually **text**.

```python
print(type("30"))
```

Output

```python
<class 'str'>
```

---

# Strings are Ordered 📋

Every character has an **index**.

```text
"Kiran"

Character

 K   i   r   a   n

Index

 0   1   2   3   4
```

---

# Access Characters

```python
name = "Kiran"

print(name[0])
```

Output

```text
K
```

---

```python
print(name[2])
```

Output

```text
r
```

---

# Negative Indexing

Python can count from the end.

```text
K  i  r  a  n

0  1  2  3  4

-5 -4 -3 -2 -1
```

```python
print(name[-1])
```

Output

```text
n
```

---

# String Slicing ✂️

Suppose

```python
name = "Kirankumar"
```

```text
Index

0 1 2 3 4 5 6 7 8 9 10

K i r a n k u m a r
```

---

First five letters

```python
print(name[:5])
```

Output

```text
Kiran
```

---

Middle

```python
print(name[2:7])
```

Output

```text
ranku
```

---

Last three

```python
print(name[-3:])
```

Output

```text
mar
```

---

# Strings are Immutable 🔒

This is one of the most important interview questions.

```python
name = "Kiran"

name[0] = "P"
```

Output

```text
TypeError:
'str' object does not support item assignment
```

You **cannot change individual characters**.

Instead, create a new string.

```python
name = "Piran"
```

---

# Length of a String

```python
name = "Kiran"

print(len(name))
```

Output

```text
5
```

---

# String Concatenation

Joining strings together.

```python
first = "Kiran"

last = "Yadav"

print(first + " " + last)
```

Output

```text
Kiran Yadav
```

---

# String Repetition

```python
print("Hi " * 3)
```

Output

```text
Hi Hi Hi
```

---

# Membership

```python
name = "Kirankumar"

print("Kiran" in name)
```

Output

```text
True
```

---

```python
print("Google" in name)
```

Output

```text
False
```

---

# Loop Through a String

```python
for letter in "Python":
    print(letter)
```

Output

```text
P
y
t
h
o
n
```

---

# Most Important String Methods ⭐⭐⭐

## `upper()`

```python
name = "kiran"

print(name.upper())
```

Output

```text
KIRAN
```

---

## `lower()`

```python
name = "KIRAN"

print(name.lower())
```

Output

```text
kiran
```

---

## `capitalize()`

```python
name = "kiran"

print(name.capitalize())
```

Output

```text
Kiran
```

---

## `title()`

```python
text = "hello world"

print(text.title())
```

Output

```text
Hello World
```

---

## `strip()`

Removes spaces from both ends.

```python
text = "   Python   "

print(text.strip())
```

Output

```text
Python
```

---

## `replace()`

```python
text = "I love Java"

print(text.replace("Java", "Python"))
```

Output

```text
I love Python
```

---

## `find()`

Returns the index of the first match.

```python
text = "Python Programming"

print(text.find("Program"))
```

Output

```text
7
```

If not found:

```python
print(text.find("Java"))
```

Output

```text
-1
```

---

## `count()`

```python
text = "banana"

print(text.count("a"))
```

Output

```text
3
```

---

## `startswith()`

```python
text = "Python"

print(text.startswith("Py"))
```

Output

```text
True
```

---

## `endswith()`

```python
print(text.endswith("on"))
```

Output

```text
True
```

---

# Split a String ⭐

One of the most commonly used methods.

```python
text = "Apple,Banana,Mango"

fruits = text.split(",")

print(fruits)
```

Output

```python
['Apple', 'Banana', 'Mango']
```

A string becomes a **list**.

---

# Join Strings ⭐

Reverse of `split()`.

```python
fruits = ["Apple", "Banana", "Mango"]

text = ", ".join(fruits)

print(text)
```

Output

```text
Apple, Banana, Mango
```

A list becomes a **string**.

---

# String Formatting

## Old Way

```python
name = "Kiran"

print("Hello " + name)
```

---

## Better Way (f-string) ⭐

```python
name = "Kiran"
age = 30

print(f"My name is {name} and I am {age} years old.")
```

Output

```text
My name is Kiran and I am 30 years old.
```

👉 **f-strings are the preferred modern way** to format strings in Python.

---

# Escape Characters

Suppose you want:

```text
I'm Kiran
```

Wrong:

```python
text = 'I'm Kiran'
```

Python gets confused.

Correct:

```python
text = "I'm Kiran"
```

or

```python
text = 'I\'m Kiran'
```

---

# Multi-line Strings

```python
message = """
Hello
Welcome
Python
"""

print(message)
```

---

# Common Mistakes

### `"100"` vs `100`

```python
x = "100"
```

String

```python
y = 100
```

Integer

Adding them:

```python
print("100" + "50")
```

Output

```text
10050
```

Not

```text
150
```

Because Python joins the text.

---

Convert to integer:

```python
print(int("100") + int("50"))
```

Output

```text
150
```

---

# Time Complexity 🚀

| Operation     | Time |
| ------------- | ---- |
| Indexing      | O(1) |
| Slicing       | O(k) |
| Length        | O(1) |
| Search (`in`) | O(n) |
| Concatenation | O(n) |
| `replace()`   | O(n) |
| `split()`     | O(n) |
| `join()`      | O(n) |

---

# Interview Tips ⭐

1. ✅ Strings are **ordered**.
2. ✅ Strings are **immutable**.
3. ✅ Strings support **indexing** and **slicing**.
4. ✅ Strings can be enclosed in single or double quotes.
5. ✅ `split()` converts a string into a list.
6. ✅ `join()` converts a list into a string.
7. ✅ `find()` returns `-1` if the substring isn't found.
8. ✅ Use **f-strings** for readable and efficient string formatting.

---

# 🧠 Memory Trick

Think of a **String** as a **train 🚆**.

```text
K i r a n

🚃 🚃 🚃 🚃 🚃
```

* Every coach is a **character**.
* Every coach has a **seat number (index)**.
* You can **look** at any coach.
* ❌ You **cannot replace** one coach in the middle—the train (string) is immutable. If you want a different train, you create a new one.
* 🪄 But you can use .replace() method to replace character.

```python
name = "Kirankumar"
name.replace('r', 's', 1)
```

Output:
```python
Kisankumar
```

---

# 🎯 Formula to Remember

> **`str` = Text + Ordered + Immutable + Indexed**

---

# 📊 Comparison of Common Data Types

| Data Type | Example    | Used For          |
| --------- | ---------- | ----------------- |
| `int`     | `25`       | Whole numbers     |
| `float`   | `25.75`    | Decimal numbers   |
| `str`     | `"Python"` | Text              |
| `bool`    | `True`     | True/False values |

---

## 💡 Interview Question

### Q: What is the difference between a List and a String?

| String                 | List                             |
| ---------------------- | -------------------------------- |
| `"Python"`             | `["P", "y", "t", "h", "o", "n"]` |
| Immutable              | Mutable                          |
| Stores text            | Stores any data type             |
| Methods like `upper()` | Methods like `append()`          |
