# 🐍 Python `int` (Integer) — Explained in the Simplest Way

Think of an **Integer (`int`)** as a **whole number**.

Whole numbers have:

* ✅ No decimal point
* ✅ Can be positive
* ✅ Can be negative
* ✅ Can be zero

---

# 🧠 Real-Life Analogy

Imagine you're counting apples 🍎.

```text
🍎 🍎 🍎 🍎 🍎
```

How many apples?

```text
5
```

Not:

```text
5.5
```

Because you can't have **half an apple** while counting whole apples.

This whole number is an **Integer**.

---

# Creating an Integer

```python
age = 30

print(age)
```

Output

```text
30
```

---

# More Examples

```python
temperature = -5

year = 2026

score = 100

zero = 0
```

All of these are integers.

---

# Positive Integers ➕

```python
x = 15
```

Output

```text
15
```

Examples:

```text
1
5
100
9999
```

---

# Negative Integers ➖

```python
x = -20
```

Output

```text
-20
```

Examples

```text
-1
-10
-500
```

---

# Zero is also an Integer

```python
x = 0
```

Output

```text
0
```

---

# Checking the Data Type

Use `type()`.

```python
age = 30

print(type(age))
```

Output

```python
<class 'int'>
```

---

# Integer Arithmetic

Suppose

```python
a = 10
b = 5
```

---

## Addition

```python
print(a + b)
```

Output

```text
15
```

---

## Subtraction

```python
print(a - b)
```

Output

```text
5
```

---

## Multiplication

```python
print(a * b)
```

Output

```text
50
```

---

## Division

```python
print(a / b)
```

Output

```text
2.0
```

⚠️ Notice:

Even though both numbers are integers, `/` returns a **float**.

---

## Floor Division

```python
print(a // b)
```

Output

```text
2
```

Returns an integer when dividing evenly.

Example:

```python
print(7 // 2)
```

Output

```text
3
```

It removes the decimal part.

---

## Modulus (Remainder)

```python
print(7 % 2)
```

Output

```text
1
```

Meaning:

```text
7 ÷ 2

Quotient = 3
Remainder = 1
```

---

## Exponent (Power)

```python
print(2 ** 3)
```

Output

```text
8
```

Meaning

```text
2 × 2 × 2
```

---

# Integer Conversion

Convert a string into an integer.

```python
age = int("30")

print(age)
```

Output

```text
30
```

Type

```python
print(type(age))
```

Output

```python
<class 'int'>
```

---

# Converting Float to Integer

```python
price = 99.99

print(int(price))
```

Output

```text
99
```

⚠️ `int()` **does not round** the number—it simply removes the decimal part (truncates toward zero).

---

# Boolean and Integer

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
print(int(True))
```

Output

```text
1
```

---

```python
print(int(False))
```

Output

```text
0
```

---

# Large Integers

Unlike many programming languages, Python can store **very large integers**.

```python
number = 999999999999999999999999999999

print(number)
```

Python handles it automatically.

---

# Common Integer Functions

```python
x = -25
```

Absolute value

```python
abs(x)
```

Output

```text
25
```

---

Power

```python
pow(2, 5)
```

Output

```text
32
```

---

Maximum

```python
max(5, 8, 2)
```

Output

```text
8
```

---

Minimum

```python
min(5, 8, 2)
```

Output

```text
2
```

---

# Where Are Integers Used?

Integers are everywhere.

Examples:

* 👤 Age → `30`
* 🎯 Game Score → `1500`
* 📚 Number of Books → `25`
* 👨‍🎓 Student Roll Number → `101`
* 📅 Year → `2026`
* 🏢 Employee ID → `10045`
* 🚗 Speed Limit → `80`

---

# Common Mistakes

### ❌ Confusing `10` and `"10"`

```python
x = 10
```

Integer

```python
type(x)
```

Output

```python
<class 'int'>
```

---

```python
x = "10"
```

String

```python
type(x)
```

Output

```python
<class 'str'>
```

Although they look similar, they are different data types.

---

### ❌ Expecting `int()` to Round

```python
print(int(9.99))
```

Output

```text
9
```

Not

```text
10
```

---

# Time Complexity 🚀

| Operation             | Time                              |
| --------------------- | --------------------------------- |
| Addition              | O(1) (for typical-sized integers) |
| Subtraction           | O(1)                              |
| Multiplication        | O(1) (for typical-sized integers) |
| Division              | O(1)                              |
| Comparison            | O(1)                              |
| Type Check (`type()`) | O(1)                              |

> ⚠️ For extremely large integers (hundreds or thousands of digits), operations become slower because Python has to process more digits.

---

# Interview Tips ⭐

1. ✅ `int` represents **whole numbers**.
2. ✅ Integers can be **positive, negative, or zero**.
3. ✅ Integers have **no decimal point**.
4. ✅ `/` always returns a **float**.
5. ✅ `//` performs **floor division**.
6. ✅ `%` returns the **remainder**.
7. ✅ `**` is used for **exponentiation**.
8. ✅ `int()` converts compatible values to integers by **truncating** decimal values toward zero.

---

# 🧠 Memory Trick

Think of an **Integer** as a **lift (elevator) floor number 🛗**.

You can be on:

* Basement 2 → `-2`
* Ground Floor → `0`
* 1st Floor → `1`
* 10th Floor → `10`

You **cannot** be on floor:

```text
10.5
```

because floors are counted as **whole numbers**.

**Formula to remember:**

> **`int` = Whole Numbers + No Decimal + Positive/Negative/Zero**

This one-line formula is enough to answer the common interview question:

> **"What is an integer in Python?"**

---

# 📊 Quick Comparison of Basic Data Types

| Data Type | Example | Description           |
| --------- | ------- | --------------------- |
| `int`     | `25`    | Whole numbers         |
| `float`   | `25.5`  | Numbers with decimals |
| `str`     | `"25"`  | Text                  |
| `bool`    | `True`  | True/False values     |
