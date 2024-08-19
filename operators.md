# **Operators**

### **Arithmetic Operators**

**Expression** | **Meaning** 
:--- | :---
`a + b` | Addition
`a - b` | Subtraction
`a * b` | Multiplication
`a / b` | Division (Float Quotient)
`a // b` | Floor Division (Integer Quotient)
`a % b` | Modulo (Remainder)
`a ** b` | Power (Exponent)
`+a` | Unary Positive
`-a` | Unary Negative

### **Compound Arithmetic Operators**
Expression | Meaning | Similar
:--- | :--- | :---
`a += b` | Addition | `a = a + b`
`a -= b` | Subtraction | `a = a - b`
`a *= b` | Multiplication | `a = a * b`
`a /= b` | Division (Float Quotient) | `a = a / b`
`a //= b` | Floor Division (Integer Quotient) | `a = a // b`
`a %= b` | Modulo (Remainder) | `a = a % b`
`a **= b` | Power (Exponent) | `a = a ** b`

### **Comparison | Relational Operators**
**Expression** | **Meaning** 
:--- | :---
`a == b` | Equal
`a != b` | Not equal
`a < b` | Less than
`a > b` | Greater than
`a <= b` | Less than or equal
`a >= b` | Greater than or equal

### **Logical Operators** 
**Expression** | **Meaning** 
:--- | :---
`x and y` | True if both x and y are true
`x or y` | True if x or y is true
`not x` | Invert of x

### **Identity Operators**
**Expression** | **Meaning** 
:--- | :---
`x is y` | True if the objects x and y are same
`x is not y` | True if the objects x and y are different

### **Membership Operators** 
**Expression** | **Meaning** 
:--- | :---
`x in [x, y, z]` | True if x is a member of collection 
`x not in [a, b, c]` | True if x is not a member of collection

### **Bitwise Operators**
**Expression** | **Meaning** 
:--- | :---
`a & b` | And
`a \| b` | Or
`a ^ b` | Xor
`a << b` | Shift left
`a >> b` | Shift right

### **Value Operators**
**Expression** | **Meaning** 
:--- | :---
`a and b` | And
`a or b` | Or
`not a` | Not
`a in b` | Value in the collection (Membership)
`a not in b` | Value not in the collection (Membership)
`a is b` | Same object (Identity)
`a is not b` | Not same object (Identity)

### **Operator Precedence**
**Operators** | **Description**
:--- | :---
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
