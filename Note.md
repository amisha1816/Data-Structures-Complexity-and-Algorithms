

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
squares = [i**2 for i in range(10)]
```

How does it work?
- A Square Bracket containing an expression that describes the list
- 1+ ```for clause``` to explain its items
- 0+ ```if clauses``` depending on the complexity of the list (e.g. for blank if x, y, z)

---

#### ✏️ map()

What does it do - Applys a function to iterable data

``` Format - map(function_name, sequence)```

- function_name: any function (built-in or selfmade) 
- sequence: any iterable data type

```python
square_array = list(map(square, array)
# square is the function, # array is the sequence
```
---

#### ✏️ filter()
  
What does it do - Filters out items from a data set that meets a certain condion (condition is True)

``` Format: filter(bool_returning_function, sequence)```

- function: The function name we provide for filter() must be return a boolean value ... should also be able handle the items inside the sequence as its arguments
- sequence: any iterable data type

```python

def isOdd(x)
    return x % 2 != 0 # will return either True or False

array = list(range(1, 10)
odds = list(filter(isOdd, array)
# in this case the function would return [1, 3, 5, 7, 9]
```
---

#### ✏️ Tuples

Tuple is a new data type! They're sliceable, indexable and iterable

``` Format: (item, item...) - because of this format tuple comprehension uses round brackets```

Examples:
```python
a = (1, 2, 3, 4, 5, 6)
d = (1, 2, 3, 4, 5, 6, 'Hi!')
```

Built in Functions with Tuple
- built in: max, min, len
- special: tuple (e.g ``` tuple(word) - ('H', 'e', 'l', 'l', 'o')```

Packing and Unpacking
Tuple allows us to easily collect variables and assign them to certain values. For instance:

```python

# Packing
var_1 = 2
var_2 = 3
var_3 = 5

prime = var_1, var_2, var_3
output - (2, 3, 5)

# Unpacking
fib = (0, 1, 1, 2, 3, 5, 8)

fib_0, fib_1, fib_n = fib[0], fib[1], fib[2:]
e.g. fib_0 = 0
e.g. fib_n = (1, 2, 3, 5, 8)
```

---

#### ✏️ Sets

Sets is a new data type. It's iterable, mutable, but not indexable or sliceable. Sets don't have an order (or an order of insertion), sets can't gurantee that their values will be in order. Due to all this, sets don't record a value's position.

What is it?
- an unordered collection with no duplicate elements
- a mathematical way to describe collection of different unique objects
- by following the operations and characteristics of the mathematical set, we can utilizie such data structure 

``` Format: {item, item...}```

Membership
- A set has no duplicates
- A set’s membership operation is one of the fastest operations compared to strings, lists, or tuples
- By using membership operator, we can be certain a target exists or does not exist in our data

Operators
```Union``` → joins two sets ```result = set1 | set2```
```Intersection``` → returns members that exist in both sets

```python
set1 = set('hello')
set2 = set('world')

result = set1 & set2
# uses '&' symbol
```

```Difference``` → members that only exist in the first set not the second

```python
set1 = set('hello')
set2 = set('world')

result = set1 - set2 

# uses - symbol
# output = {'e', 'h'}
```

```Symmetric Difference``` → members that exist in one or the other set, but not both

```python
set1 = set('hello')
set2 = set('world')

result = set1 ^ set2 

# uses ^ symbol
# output = {'e', 'h', 'w', 'd', 'r'}
```

```Proper Subset``` → a boolean operator that says A is proper subset of B if all members of A are found in B, but A cannot be exactly the same as B

```python
set1 = {1, 2, 3}
set2 = {1, 2, 3, 4)
set3 = {1, 2, 3}
set4 = set('hello')

print('Is set1 proper subset of set2?:', set1 < set2) # < is the proper subset operator
print('Is set1 proper subset of set3?:', set1 < set3)
print('Is set1 proper subset of set4?:', set1 < set4)

# Is set1 proper subset of set2?: True
# Is set1 proper subset of set3?: False
# Is set1 proper subset of set4?: False
# uses < symbol
```

```Subset``` → Same as proper subset except it can equal to B and uses <= symbol
``` Proper Superset``` → a boolean operator that says A is a proper superset of B if A has all the values of B and more, but they are not equal to each other

```python
# Superset Example:
set1 = {1,2,3,4}
set2 = {1,2,3,4}
set3 = {1,2,3}
set4 = set('hello')

print('Is set1 proper superset of set2?:', set1 > set2) # > is the proper superset operator
print('Is set1 proper superset of set3?:', set1 > set3)
print('Is set1 proper superset of set4?:', set1 > set4)

# Is set1 proper superset of set2?: False
# Is set1 proper superset of set3?: True
# Is set1 proper superset of set4?: False
```

```Superset``` → Same as proper superset except it can equal to B and uses >= symbol

*two sets are considered disjointed when they share no common value.

---

#### ✏️ Dictionary

A data type that stores a collection of (key, value) pairs, such that each possible key appears at most once in the collection.

```python
Format: {
    item: item,
    item: item,
 }
```

__Keys__
Are a unique address for a dictionary value’s location

Properties: 
- Must be immutable (strings, numbers, tuples, frozenset)
- Unique; therefore, two same key values cannot exist in a single dictionary - NEWEST CREATED ITEM with a duplicate KEY superceeds the previous declaration (replaces)

__Values__
A dictionary within a key can be any data type.

```python

sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

sammy['followers'] += 10 # We are adding 10 to the value located at key: 'followers'
sammy['verified'] = True # We added a new value at a new key: 'verified'
sammy['username'] = 'SammySammy'

print('Sammy Dict:', sammy)

# output - Sammy Dict: {'username': 'SammySammy', 'online': True, 'followers': 52, 'verified': True}
```

Dictionary Methods
- A.keys() → Returns a sequence of keys/addresses in A
- A.values() → Returns a sequence of item values in A
- A.items() → Returns a sequence of key,item pairs in A
- A.get(address) → Returns the item value at address
- A.update(B) → Extends A with the dictionary of key,value pairs of B
- dict() → allows us to turn other data ypes into dictionaries

__Iterating a Dictionary__
keys → ```for k in sammy.keys()```
values → ```for v in sammy.values():```
items → ```for k, v in sammy.items():```
