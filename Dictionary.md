# 🐍 Python Dictionary — Explained in the Simplest Way

Think of a **Dictionary** as a **real-life phone contacts app 📱**.

Instead of searching by position (index), you search by **name**.

For example:

```text
Rahul  → 9876543210
Kiran  → 9988776655
Anita  → 9123456789
```

Here:

* **Rahul** is the **Key** 🔑
* **9876543210** is the **Value** 📞

That's exactly how a Python Dictionary works.

---

# 🧠 Real-Life Analogy

Imagine your Aadhaar card.

```text
Aadhaar Number → 1234 5678 9012
Name           → Kiran
DOB            → 07-Feb-1996
City           → Mumbai
```

Everything has a **label (Key)** and a corresponding **value**.

Python stores this using a Dictionary.

```python
person = {
    "name": "Kiran",
    "age": 30,
    "city": "Mumbai"
}
```

---

# Why do we need Dictionaries?

Suppose you're storing employee information.

Without a dictionary:

```python
name = "Kiran"
age = 30
city = "Mumbai"
salary = 1200000
```

Imagine managing 10,000 employees!

Instead:

```python
employee = {
    "name": "Kiran",
    "age": 30,
    "city": "Mumbai",
    "salary": 1200000
}
```

Everything is grouped together.

---

# Creating a Dictionary

```python
student = {
    "name": "Rahul",
    "marks": 95,
    "city": "Delhi"
}
```

Output

```python
{
    'name': 'Rahul',
    'marks': 95,
    'city': 'Delhi'
}
```

Notice:

* List → `[]`
* Tuple → `()`
* Set → `{}`
* Dictionary → `{ key : value }`

---

# Keys and Values 🔑

```python
student = {
    "name": "Rahul",
    "marks": 95,
    "city": "Delhi"
}
```

Think of it like this:

```text
Key        Value

name   →   Rahul
marks  →   95
city   →   Delhi
```

---

# Accessing Values

Use the **key**, not an index.

```python
print(student["name"])
```

Output

```text
Rahul
```

---

```python
print(student["marks"])
```

Output

```text
95
```

---

# Using `get()` (Safer Way)

```python
print(student.get("city"))
```

Output

```text
Delhi
```

If the key doesn't exist:

```python
print(student.get("salary"))
```

Output

```text
None
```

Unlike:

```python
print(student["salary"])
```

Output

```text
KeyError
```

👉 **Interview Tip:** Prefer `get()` when a key may be missing.

---

# Dictionaries are Mutable ✏️

You can change values.

```python
student = {
    "name": "Rahul",
    "marks": 95
}

student["marks"] = 99

print(student)
```

Output

```python
{
    'name': 'Rahul',
    'marks': 99
}
```

---

# Adding New Items

```python
student["city"] = "Delhi"

print(student)
```

Output

```python
{
    'name': 'Rahul',
    'marks': 99,
    'city': 'Delhi'
}
```

---

# Removing Items

## `pop()`

```python
student.pop("city")

print(student)
```

Output

```python
{
    'name': 'Rahul',
    'marks': 99
}
```

---

## `del`

```python
del student["marks"]
```

---

## `clear()`

```python
student.clear()
```

Output

```python
{}
```

---

# Dictionary Keys Must Be Unique

```python
student = {
    "name": "Rahul",
    "name": "Kiran"
}
```

Output

```python
{
    'name': 'Kiran'
}
```

The second value replaces the first.

👉 Keys must be unique.

---

# Values Can Repeat

```python
students = {
    "student1": 90,
    "student2": 90,
    "student3": 90
}
```

Duplicate **values** are allowed.

---

# Different Data Types

```python
person = {
    "name": "Kiran",
    "age": 30,
    "height": 5.9,
    "is_employee": True
}
```

---

# Nested Dictionary 📦

```python
employee = {
    "name": "Kiran",
    "address": {
        "city": "Mumbai",
        "state": "Maharashtra"
    }
}
```

Access nested value:

```python
print(employee["address"]["city"])
```

Output

```text
Mumbai
```

---

# Dictionary Inside a List

Very common in APIs and JSON.

```python
employees = [
    {"name": "Rahul", "salary": 100},
    {"name": "Kiran", "salary": 200},
    {"name": "Anita", "salary": 300}
]
```

Access:

```python
print(employees[1]["name"])
```

Output

```text
Kiran
```

---

# Loop Through Dictionary

## Keys

```python
for key in student:
    print(key)
```

Output

```text
name
marks
city
```

---

## Values

```python
for value in student.values():
    print(value)
```

Output

```text
Rahul
95
Delhi
```

---

## Keys and Values Together

```python
for key, value in student.items():
    print(key, value)
```

Output

```text
name Rahul
marks 95
city Delhi
```

---

# Useful Dictionary Methods

## `keys()`

```python
student.keys()
```

Output

```text
dict_keys(['name', 'marks', 'city'])
```

---

## `values()`

```python
student.values()
```

Output

```text
dict_values(['Rahul', 95, 'Delhi'])
```

---

## `items()`

```python
student.items()
```

Output

```text
dict_items([
('name','Rahul'),
('marks',95),
('city','Delhi')
])
```

---

# Update Multiple Values

```python
student.update({
    "marks": 98,
    "city": "Mumbai"
})
```

---

# Copy Dictionary

```python
new_student = student.copy()
```

---

# Dictionary Comprehension ⭐

```python
squares = {
    x: x*x
    for x in range(5)
}

print(squares)
```

Output

```python
{
0:0,
1:1,
2:4,
3:9,
4:16
}
```

---

# Time Complexity 🚀

| Operation     | Time         |
| ------------- | ------------ |
| Access by key | O(1) Average |
| Add           | O(1) Average |
| Update        | O(1) Average |
| Delete        | O(1) Average |
| Search key    | O(1) Average |
| Loop          | O(n)         |
| Copy          | O(n)         |

> ⚠️ Like sets, dictionaries are implemented using **hash tables**, making key lookups very fast on average.

---

# List vs Tuple vs Set vs Dictionary

| Feature     | List  | Tuple | Set   | Dictionary       |
| ----------- | ----- | ----- | ----- | ---------------- |
| Ordered     | ✅ Yes | ✅ Yes | ❌ No  | ✅ Yes*           |
| Mutable     | ✅ Yes | ❌ No  | ✅ Yes | ✅ Yes            |
| Duplicates  | ✅ Yes | ✅ Yes | ❌ No  | Keys ❌, Values ✅ |
| Indexing    | ✅ Yes | ✅ Yes | ❌ No  | By Key           |
| Fast Search | ❌ No  | ❌ No  | ✅ Yes | ✅ Yes            |
| Syntax      | `[]`  | `()`  | `{}`  | `{key: value}`   |

> *From Python 3.7 onward, dictionaries preserve insertion order.

---

# When Should You Use a Dictionary? 🤔

Use a **dictionary** when you need to store data as **key-value pairs**.

Examples:

* 👤 Employee details
* 📦 Product information
* 🌐 JSON data from APIs
* ⚙️ Configuration settings
* 📱 Phone contacts
* 🧾 Student records

---

# Interview Tips ⭐

1. ✅ Dictionaries store **key-value pairs**.
2. ✅ Keys must be **unique** and **hashable** (e.g., strings, numbers, tuples of immutable values).
3. ✅ Values can be of any type and may be duplicated.
4. ✅ Dictionaries are **mutable**.
5. ✅ Access values using keys, not indexes.
6. ✅ Use `get()` to safely access keys that might not exist.
7. ✅ Iterate with `items()` when you need both keys and values.
8. ✅ Average-case lookup, insertion, and deletion are **O(1)** because dictionaries use **hash tables**.

---

# 🧠 Memory Trick

Think of a **Dictionary** as a **library catalog 📚**.

Instead of asking:

> "Give me the **3rd book**."

You ask:

> "Give me the book with **ISBN 978...**."

The **ISBN** is the **key** 🔑, and the **book information** is the **value**.

This lets the librarian find the right book quickly without scanning every shelf.

**Formula to remember:**

> **Dictionary = Key → Value + Mutable + Unique Keys + Fast Lookup**

This one-line formula is enough to answer one of the most common interview questions about Python dictionaries.

---

# 🎯 Summary: Which Data Structure Should I Use?

| If you want...                           | Use            |
| ---------------------------------------- | -------------- |
| 📋 Ordered collection that changes       | **List**       |
| 🔒 Ordered collection that never changes | **Tuple**      |
| 🚫 Unique values with fast search        | **Set**        |
| 🔑 Key → Value mapping                   | **Dictionary** |

## ⭐ One important thing to know is:

> **❌ You cannot directly rename a key in a Python dictionary.**

Instead, you:

1. ✅ Create a new key.
2. ✅ Copy the old value.
3. ✅ Delete the old key.

---

# 🧠 Real-Life Analogy

Imagine your office ID card.

Before:

```text
Employee ID : E101
Name        : Kiran
```

The company changes your ID.

After:

```text
Employee ID : EMP101
Name        : Kiran
```

They don't edit the old ID—they create a new one and remove the old one.

That's exactly how Python dictionaries work.

---

# Method 1: Using `pop()` ⭐ (Most Common)

```python
student = {
    "marks": 95,
    "name": "Kiran"
}

student["score"] = student.pop("marks")

print(student)
```

**Output**

```python
{
    'score': 95,
    'name': 'Kiran'
}
```

### What happened?

```python
student.pop("marks")
```

returns:

```python
95
```

Then:

```python
student["score"] = 95
```

So Python:

* ✅ Creates the new key `"score"`
* ✅ Copies the value `95`
* ✅ Removes the old key `"marks"`

---

# Method 2: Step by Step

```python
student = {
    "marks": 95,
    "name": "Kiran"
}

student["score"] = student["marks"]

del student["marks"]

print(student)
```

**Output**

```python
{
    'score': 95,
    'name': 'Kiran'
}
```

---

# Visual Explanation

### Before

```text
marks ───► 95
name  ───► Kiran
```

↓

Rename

↓

### After

```text
score ───► 95
name  ───► Kiran
```

The **value stays the same**, only the **key changes**.

---

# ⚠️ What if the Old Key Doesn't Exist?

Using `pop()` without a default value:

```python
student.pop("age")
```

Output

```text
KeyError
```

Safer version:

```python
student["years"] = student.pop("age", None)
```

If `"age"` doesn't exist:

* No error
* `None` is returned

Or you can check first:

```python
if "age" in student:
    student["years"] = student.pop("age")
```

---

# ⭐ Interview Tip

There is **no built-in `rename_key()` method** in Python dictionaries.

The standard way to rename a key is:

```python
dictionary[new_key] = dictionary.pop(old_key)
```

or

```python
dictionary[new_key] = dictionary.pop(old_key, default_value)
```

---

# 🧠 Memory Trick

Think of a **dictionary** as a locker room.

Before:

```text
Locker 101 → Kiran's Bag
```

The locker number changes.

Instead of changing the locker number directly:

1. 📦 Move the bag to **Locker 201**
2. 🗑️ Remove **Locker 101**

That's exactly what `pop()` does.

---

# 🚀 Summary

| Task           | Code                                      |
| -------------- | ----------------------------------------- |
| Update a value | `student["marks"] = 99`                   |
| Add a new key  | `student["city"] = "Mumbai"`              |
| Rename a key   | `student["score"] = student.pop("marks")` |
| Delete a key   | `del student["marks"]`                    |

## 🎯 One-Line Rule

* **Update Value:** `dict[key] = new_value`
* **Rename Key:** `dict[new_key] = dict.pop(old_key)`
