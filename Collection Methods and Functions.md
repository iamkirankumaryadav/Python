<table align="center">
  <tr>
    <th><h3>List Methods</h3></th>         
  </tr>
  <tr>
    <td><img src="Images/ListMethods.png" alt="List Methods"></td>   
  </tr>
</table>

<table align="center">
  <tr>
    <th><h3>Set Methods</h3></th>
    <th><h3>Set Functions</h3></th>           
  </tr>
  <tr>
    <td><img src="Images/SetMethods.png" alt="Set Methods"></td>   
    <td><img src="Images/SetFunctions.png" alt="Set Functions"></td>    
  </tr>
</table>

<table align="center">
  <tr>
    <th><h3>Dictionary Methods</h3></th>
    <th><h3>Dictionary Functions</h3></th>           
  </tr>
  <tr>
    <td><img src="Images/DictionaryMethods.png" alt="Dictionary Methods"></td>   
    <td><img src="Images/DictionaryFunction.png" alt="Dictionary Functions"></td>    
  </tr>
</table>

### `Set`

`issubset` : All the elements of set A is present in set B.

`isdisjoint` : No common element between both the sets.

`Difference` : Set of elements present in set A but not in set B

```python
A = {1, 2, 3, 4, 5}
B = {5, 6, 7, 8, 9}

A.difference(B) : {1, 2, 3, 4}
B.difference(A) : {6, 7, 8, 9}
```

`Intersection` : Elements common in both the sets 

```python
A = {1, 2, 3, 4, 5}
B = {5, 6, 7, 8, 9}

A.intersection(B) : {5}
```

`Symmetric Difference` : Set of `uncommon` elements in both set A and B

```python
A = {1, 2, 3, 4, 5}
B = {5, 6, 7, 8, 9}

A.symmetric_difference(B) : {1, 2, 3, 4, 6, 7, 8, 9}
```

### Data Type of an `empty set` is a dictionary `type({}) : dict`

### [Python Builtins](https://www.programiz.com/python-programming/methods/built-in)

### [Practical Business Python](https://pbpython.com/pandas_dtypes.html)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
