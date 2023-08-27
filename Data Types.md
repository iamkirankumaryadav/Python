# Python Data Types

<table>
  <tr>
    <th colspan=4><h3>Primitive Data Types</h3></th>
  </tr>
  <tr>
    <th><h3>Numeric</h3></th>
    <th><h3>Boolean</h3></th>
    <th><h3>String</h3></th>
    <th><h3>None</h3></th>
  </tr>
  <tr>
    <td>
      <ol type="A">
        <li><strong>int</strong>: Integer | Whole No.</li>
        <li><strong>float</strong>: Floating Point | Decimal No.</li>
        <li><strong>complex(7 + j)</strong> | Complex No.</li>
        <li><strong>bin(2)</strong>: Binary</li>
        <li><strong>oct(8)</strong>: Octal</li>
        <li><strong>hex(16)</strong>: Hexadecimal</li>
      </ol>
    </td>
    <td>
      <ol type="A">
        <li>True</li>
        <li>False</li>
      </ol>
    </td>
    <td>Sequence of <strong>characters</strong>:<br>"Hello", "123", <br>"!@#$%^&*()_+{}[]:;<>?"</td>
    <td>
      <strong>Absence of a value:<br>NoneType</strong>      
    </td>
  </tr>

  <tr>
    <th colspan=4><h3>Collections | Arrays</h3></th>
  </tr>
  <tr>
    <th><h3>List</h3></th>
    <th><h3>Tuple</h3></th>
    <th><h3>Set</h3></th>
    <th><h3>Dictionary</h3></th>
  </tr>
  <tr>
    <td colspan=2>Represents sequence of values</td>
    <td>Represents a collection of unique values</td>
    <td>Maps keys to the values for efficient information retrieval</td>
  </tr>
  <tr>
    <td colspan=2>Ordered and Allow Duplicates</td>    
    <td>Unordered and Unique</td>
    <td>Ordered unique keys</td>
  </tr>
  <tr>
    <td>Subscriptable</td>
    <td>Subscriptable</td>
    <td>Not subscriptable</td>
    <td>Subscriptable (Access by key)</td>
  </tr>
  <tr>
    <td>Mutable</td>
    <td>Immutable</td>
    <td>Mutable (Only add and remove)</td>
    <td>Mutable</td>
  </tr>
  <tr>
    <td>Heterogeneous</td>
    <td>Heterogeneous</td>
    <td>Heterogeneous<br>Only lists and Dictionaries are unhashable</td>
    <td>Heterogeneous</td>
  </tr>
  <tr>
    <td>list([1, 2, 3])</td>
    <td>tuple([1, 2, 3])</td>
    <td>set([1, 2, 3])</td>
    <td>dict({key : value})</td>
  </tr>
  <tr>
    <td>Add 
      <ol type="i">
        <li>append(1)</li>
        <li>extend([1,2,3])</li>
        <li>insert(index , 1)</li>
      </ol>
     </td>
    <td>Immutable</td>
    <td>Add  
      <ol type="i">
        <li>add(1)</li>
        <li>update([2, 3, 4, 5])</li>
      </ol>
     </td>
    <td>Add  
      <ol type="i">
        <li>setdefault(k, v)</li>
        <li>update(k = v)</li>
      </ol>
     </td>
  </tr>
  <tr>
    <td>Remove 
      <ol type="i">
        <li>pop( ): Pop right</li>
        <li>pop(i): Pop at index</li>
        <li>remove(1)</li>
      </ol>
     </td>
    <td>Immutable</td>
    <td>Remove  
      <ol type="i">
        <li>pop( ): Pop arbitrary</li>
        <li>remove(1)</li>
        <li>discard(1)</li>
      </ol>
     </td>
    <td>Remove  
      <ol type="i">
        <li>pop(k): Pop item</li>
        <li>popitem( ): Pop arbitrary</li>
      </ol>
     </td>
  </tr>
</table>

```Python
# Empty set is considered as dictionary:
type({}) : dict

# We can declare empty set by using set() function:
type(set()) : set

type({1}) : set
```

### Collections are used to store multiple items in single variable.

### `Ordered`
- Order of the items remains same as passed at the time of defining collection (List, Tuple)

### `Subscriptable`
- Elements inside the collections can be `accessed` and `modified` with the help of index positions.

### `Indexing`
- Allows user to `access` a specific element at specific index position `x[i]` in an array or collection.

### `Slicing`
- Allows user to access a sequence of elements `x[start: end: step]` in an array or collection.

### `Mutable`
- We can `change` the value at a particular index.
- We can also `add` or `remove` the elements. 
- The `memory address` remains same after changes.
- `List`, `Sets` (Only add and remove) and `Dictionaries` are mutable.
- `Mutable` objects are `unhashable`
- `Integers`, `Floats`, `Strings`, `Booleans`, `Frozenset`, and `Tuples` are `immutable` (Cannot change, add or remove elements)

### `Constructor`
- `list()`, `tuple()`, `set()` and `dict()`

### `Iterable`
- Object is capable of returning it's each elements one at a time (Loops and statements can be applied on them)
- `Strings`, `Lists`, `Tuples`, `Sets` and `Dictionaries` are iterable.

### `Hashable`
- `Immutable` objects are hashable.
- `Sets` can have only hashable objects as it's `value`
- `Dictionaries` also have only hashable objects as it's `key`
- Each and every elements of an immutable object have a hash value and they are able to return a hash value.
- An object is `hashable` if it has a hash value that does not change during its entire lifetime.
- `Strings`, `Integers`, `Booleans`, `Tuples` and `Frozen Sets` are `immutable`

<table>
  <tr>
    <th>Sequence</th>
    <th>Class</th>
    <th>Definition</th>
  </tr>
  <tr>
    <td>String</td>
    <td><code>str</code></td>
    <td><strong>Immutable characters</strong></td>
  </tr>
  <tr>
    <td>List</td>
    <td><code>list</code></td>
    <td><strong>Heterogeneous mutable elements</strong></td>
  </tr>
  <tr>
    <td>Tuple</td>
    <td><code>tuple</code></td>
    <td><strong>Heterogeneous immutable elements</strong></td>
  </tr>
  <tr>
    <td>Dictionary</td>
    <td><code>dict</code></td>
    <td><strong>Key value pairs</strong></td>
  </tr>
</table>

- `List` is `ordered` and `changeable`, allows duplicate items.
- `Tuple` is `ordered` and `unchangeable`, allows duplicate items.
- `Set` is `unordered`, `unchangeable`, and `unindexed`, no duplicate items.
- `Dictionary` is `ordered` and `changeable`, no duplicate items.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
