# 🐍 Python `float` (Floating-Point Number) — Explained in the Simplest Way

Think of a **Float** as a **number with a decimal point**.

A float is used whenever you need **precision**.

Examples:

* 💰 Bank balance → `₹1250.75`
* 🌡️ Temperature → `36.8`
* 📏 Height → `5.9`
* ⛽ Fuel → `12.5` liters

---

# 🧠 Real-Life Analogy

Imagine buying apples.

You buy:

```text
🍎 2.5 kg
```

Not:

```text
🍎 2 kg
```

because the weight has a decimal.

That's a **Float**.

---

# Creating a Float

```python
price = 99.99

print(price)
```

Output

```text
99.99
```

---

# More Examples

```python
height = 5.9

temperature = 36.5

pi = 3.14159

balance = 12500.75
```

All of these are floats.

---

# Checking the Data Type

```python
price = 99.99

print(type(price))
```

Output

```python
<class 'float'>
```

---

# Float Arithmetic

Suppose

```python
a = 10.5
b = 2.5
```

---

## Addition

```python
print(a + b)
```

Output

```text
13.0
```

---

## Subtraction

```python
print(a - b)
```

Output

```text
8.0
```

---

## Multiplication

```python
print(a * b)
```

Output

```text
26.25
```

---

## Division

```python
print(a / b)
```

Output

```text
4.2
```

---

## Exponent

```python
print(2.5 ** 2)
```

Output

```text
6.25
```

---

# Converting to Float

From an integer:

```python
age = 30

print(float(age))
```

Output

```text
30.0
```

---

From a string:

```python
price = float("99.99")

print(price)
```

Output

```text
99.99
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

⚠️ **Important:**

`int()` **does not round** the number.

It simply removes the decimal part.

---

# Scientific Notation

Python also understands very large and very small numbers.

```python
number = 3e2

print(number)
```

Output

```text
300.0
```

Because

```text
3 × 10² = 300
```

---

```python
number = 5e-2

print(number)
```

Output

```text
0.05
```

Because

```text
5 × 10⁻² = 0.05
```

---

# Rounding Numbers

```python
price = 99.9876

print(round(price, 2))
```

Output

```text
99.99
```

Meaning:

Keep **2 digits after the decimal point**.

---

# Absolute Value

```python
print(abs(-5.75))
```

Output

```text
5.75
```

---

# Maximum and Minimum

```python
print(max(2.5, 8.7, 1.2))
```

Output

```text
8.7
```

---

```python
print(min(2.5, 8.7, 1.2))
```

Output

```text
1.2
```

---

# Where Are Floats Used?

Floats are used whenever decimals matter.

Examples:

* 💰 Price → `₹99.99`
* 🌡️ Temperature → `36.8`
* 📏 Height → `5.9`
* ⚖️ Weight → `72.5`
* 🚗 Fuel → `12.3`
* 📈 Stock Price → `1543.75`

---

# ⚠️ Floating-Point Precision (Interview Favorite)

Sometimes, Python gives surprising results.

```python
print(0.1 + 0.2)
```

Output

```text
0.30000000000000004
```

You might expect:

```text
0.3
```

### 🤔 Why does this happen?

Computers store decimal numbers in **binary (0s and 1s)**.

Some decimal numbers, like `0.1`, **cannot be represented exactly in binary**, just like **1/3 cannot be represented exactly in decimal**.

For example:

```text
1 ÷ 3 = 0.333333333...
```

It goes on forever.

Similarly, `0.1` in binary becomes an infinitely repeating value, so Python stores the closest possible approximation.

---

# Comparing Floats Safely

Instead of:

```python
0.1 + 0.2 == 0.3
```

Use:

```python
import math

print(math.isclose(0.1 + 0.2, 0.3))
```

Output

```text
True
```

This is the recommended way to compare floating-point numbers.

---

# Time Complexity 🚀

| Operation      | Time |
| -------------- | ---- |
| Addition       | O(1) |
| Subtraction    | O(1) |
| Multiplication | O(1) |
| Division       | O(1) |
| Comparison     | O(1) |
| `round()`      | O(1) |

---

# `int` vs `float`

| Feature       | `int`               | `float`              |
| ------------- | ------------------- | -------------------- |
| Decimal Point | ❌ No                | ✅ Yes                |
| Example       | `25`                | `25.5`               |
| Used For      | Counting            | Measurements         |
| Memory        | Less                | More                 |
| Precision     | Exact whole numbers | Approximate decimals |

---

# Interview Tips ⭐

1. ✅ `float` represents **decimal numbers**.
2. ✅ Floats can be **positive, negative, or zero**.
3. ✅ Use `float()` to convert compatible values.
4. ✅ `int()` removes the decimal part; it does **not** round.
5. ✅ Floating-point arithmetic may have **small precision errors** because of binary representation.
6. ✅ Use `round()` for display formatting and `math.isclose()` for reliable comparisons.

---

# 🧠 Memory Trick

Think of a **Float** as a **measuring tape 📏**.

When measuring a table:

```text
Length = 5 meters ❌ (not precise)
Length = 5.75 meters ✅
```

Whenever **precision** matters, use a **Float**.

---

# 🎯 Formula to Remember

> **`float` = Decimal Numbers + Precision + Positive/Negative/Zero**

---

# 📊 Comparison of Numeric Data Types

| Data Type | Example | Used For                              |
| --------- | ------- | ------------------------------------- |
| `int`     | `25`    | Counting                              |
| `float`   | `25.75` | Measurements                          |
| `bool`    | `True`  | Decisions                             |
| `complex` | `3+4j`  | Scientific & engineering calculations |

---

## 💡 Interview Question

### Q: When should you use `int` and when should you use `float`?

✅ **Use `int`** when counting whole things:

* 👥 Number of students
* 📦 Number of boxes
* 📅 Year
* 🎯 Score

✅ **Use `float`** when measurements or precision are needed:

* 🌡️ Temperature
* 📏 Height
* ⚖️ Weight
* 💰 Price
* ⛽ Fuel
