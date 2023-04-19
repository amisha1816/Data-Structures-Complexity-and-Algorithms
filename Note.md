

#### ✏️ Matrix

A representations of numbers, symbols, or expressions in a 2-Dimensional Array. In Computer Science we can start to create a data structure that has values in rows and columns, much like a table, by utilizing a list within a list. There are external libraries/modules that can be imported into replit to help this process as well.

```python
matrix_A = [
    [1, 2, 3, 4],
    {5, 6, 7, 8}
]
```

Rules for Matrix's in python:
- All rows must have the same number of values
- All columns must have the same number of values
- All items in the 2D List must have the same data types
- Since indexing always starts at 0 ... row 1 is technically located at matrix_A[0]

---

#### ✏️ List Comprehension

Is a concise method to create a list in Python. Commonly used when the list is made from another sequence, a member of another list/sequence or is a result of some operations applied to all it's item.

```python
squares = [i**2 for i in ranhe(10)]
```


How does it work?
- A Square Bracket containing an expression that describes the list
- 1+ ```for clause``` to explain its items
- 0+ ```if clauses``` depending on the complexity of the list (e.g. for blank if x, y, z)

---

#### ✏️ map()

What does it do - Applys a function to iterable data

```Format - map(function_name, sequence)```

- function_name: any function (built-in or selfmade) 
- sequence: any iterable data type

```python
square_array = list(map(square, array)
# square is the function, # array is the sequence

---

#### ✏️ map()
  
