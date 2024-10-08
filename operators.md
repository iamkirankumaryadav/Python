# **Operators**

### **Assignment Operator**
`x = 5` (Here `x` is an operand, `=` is an operator, and `5` is a value)

### **Arithmetic Operators**
**Expression** | **Meaning** | **Example** 
:--- | :--- | :---
`a + b` | Addition | `5 + 2 = 7`
`a - b` | Subtraction | `4 - 2 = 2`
`a * b` | Multiplication | `2 * 3 = 6`
`a / b` | Division (Float Quotient) | `4 / 2 = 2`
`a // b` | Floor Division (Integer Quotient) | `10 // 3 = 3`
`a % b` | Modulo (Remainder) | `5 % 2 = 1`
`a ** b` | Power (Exponent) | `4 ** 2 = 16`

### **Compound Arithmetic | Assignment Operators**
**Expression** | **Meaning** | **Example**
:--- | :--- | :---
`a = b` | Assignment | `a = 5`
`a += b` | Addition | `a = a + b`
`a -= b` | Subtraction | `a = a - b`
`a *= b` | Multiplication | `a = a * b`
`a /= b` | Division (Float Quotient) | `a = a / b`
`a //= b` | Floor Division (Integer Quotient) | `a = a // b`
`a %= b` | Modulo (Remainder) | `a = a % b`
`a **= b` | Power (Exponent) | `a = a ** b`

### **Comparison | Relational Operators**
**Expression** | **Meaning** | **Example**
:--- | :--- | :---
`a == b` | Is Equal To | `3 == 5` gives us `False`
`a != b` | Not Equal To | `3 != 5` gives us `True`
`a < b` | Less Than | `3 < 5` gives us `True`
`a > b` | Greater Than | `3 > 5` gives us `False`
`a <= b` | Less Than or Equal To | `3 <= 5` gives us `True`
`a >= b` | Greater Than or Equal To | `3 >= 5` gives us `False`

### **Logical Operators** 
**Expression** | **Meaning** 
:--- | :---
`x and y` | Logical `AND`: `True` if both x and y are `True`
`x or y` | Logical `OR`: `True` if atleast x or y is `True`
`not x` | Logical `NOT`: Invert of x

### **Identity Operators**
**Expression** | **Meaning** 
:--- | :---
`x is y` | `True` if the operands x and y are the same object
`x is not y` | `True` if the operands x and y are not identical object

### **Membership Operators** 
**Expression** | **Meaning** 
:--- | :---
`x in [x, y, z]` | `True` if the value/variable is found in the collection 
`x not in [a, b, c]` | `True` if the value/variable is not found in the collection

### **Bitwise Operators**
**Expression** | **Meaning** 
:--- | :---
`a & b` | AND
`a \| b` | OR
`a ^ b` | XOR
`~ a` | NOT
`a << b` | Left Shift
`a >> b` | Right Shift

### **Operator Precedence**
**Operators** | **Description**
:--- | :---
`=` | Assignment 
`**` | Exponent
`+x`, `-x` | Unary Positive and Negative
`*`, `/`, `//`, `%` | Multiplication, Division and Remainder
`+`, `-` | Addition and Subtraction
`<<`, `>>` | Bitwise shifts
`&` | Bitwise AND 
`^` | Bitwise XOR
`in`, `not in`, `is`, `is not`, `<`, `<=`, `>`, `>=`, `!=`, `==` | Comparisons, Membership and Identity tests
`not x` | Boolean NOT
`and` | Boolean AND
`or` | Boolean OR
