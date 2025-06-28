# README: Data Structures in Python

This document provides an overview of the main data structures in Python, their properties, and commonly used methods with examples.

---

## 1. List

- **Mutable**
- **Ordered**
- **Allows duplicates**
- **Syntax:** `[]`

### Common Methods

| Method         | Description                                  | Example                        |
|----------------|----------------------------------------------|--------------------------------|
| `append(x)`    | Adds item `x` to the end                     | `lst.append(10)`               |
| `extend(iter)` | Adds all items from iterable                 | `lst.extend([20, 30])`         |
| `insert(i, x)` | Inserts `x` at position `i`                  | `lst.insert(1, 15)`            |
| `remove(x)`    | Removes first occurrence of `x`              | `lst.remove(10)`               |
| `pop([i])`     | Removes and returns item at index `i`        | `lst.pop()`                    |
| `index(x)`     | Returns index of first occurrence of `x`     | `lst.index(20)`                |
| `count(x)`     | Counts occurrences of `x`                    | `lst.count(20)`                |
| `sort()`       | Sorts the list in place                      | `lst.sort()`                   |
| `reverse()`    | Reverses the list in place                   | `lst.reverse()`                |
| `copy()`       | Returns a shallow copy                       | `lst2 = lst.copy()`            |
| `clear()`      | Removes all items                            | `lst.clear()`                  |

**Example:**
```python
lst = [1, 2, 3]
lst.append(4)
lst.remove(2)
print(lst)  # [1, 3, 4]
```

---

## 2. Tuple

- **Immutable**
- **Ordered**
- **Allows duplicates**
- **Syntax:** `()`

### Common Methods

| Method         | Description                                  | Example                        |
|----------------|----------------------------------------------|--------------------------------|
| `count(x)`     | Counts occurrences of `x`                    | `tup.count(2)`                 |
| `index(x)`     | Returns index of first occurrence of `x`     | `tup.index(3)`                 |

**Example:**
```python
tup = (1, 2, 3, 2)
print(tup.count(2))  # 2
print(tup.index(3))  # 2
```

---

## 3. Set

- **Mutable**
- **Unordered**
- **No duplicates**
- **Syntax:** `{}` or `set()`

### Common Methods

| Method         | Description                                  | Example                        |
|----------------|----------------------------------------------|--------------------------------|
| `add(x)`       | Adds item `x`                                | `s.add(5)`                     |
| `remove(x)`    | Removes `x`, raises error if not found       | `s.remove(3)`                  |
| `discard(x)`   | Removes `x` if present                       | `s.discard(3)`                 |
| `pop()`        | Removes and returns an arbitrary element     | `s.pop()`                      |
| `clear()`      | Removes all items                            | `s.clear()`                    |
| `union(s2)`    | Returns union of sets                        | `s.union(s2)`                  |
| `intersection(s2)` | Returns intersection                     | `s.intersection(s2)`           |
| `difference(s2)`   | Returns difference                       | `s.difference(s2)`             |
| `issubset(s2)`     | Checks if set is subset                  | `s.issubset(s2)`               |
| `issuperset(s2)`   | Checks if set is superset                | `s.issuperset(s2)`             |

**Example:**
```python
s = {1, 2, 3}
s.add(4)
s.remove(2)
print(s)  # {1, 3, 4}
```

---

## 4. Frozenset

- **Immutable set**
- **Unordered**
- **No duplicates**
- **Syntax:** `frozenset(iterable)`

### Methods

Supports all set operations except those that modify the set (`add`, `remove`, etc.).

**Example:**
```python
fs = frozenset([1, 2, 3])
print(fs)
```

---

## 5. Dictionary

- **Mutable**
- **Ordered (Python 3.7+)**
- **Keys must be unique**
- **Syntax:** `{key: value}`

### Common Methods

| Method             | Description                                  | Example                        |
|--------------------|----------------------------------------------|--------------------------------|
| `get(key)`         | Returns value for key, or None               | `d.get('a')`                   |
| `keys()`           | Returns all keys                             | `d.keys()`                     |
| `values()`         | Returns all values                           | `d.values()`                   |
| `items()`          | Returns all key-value pairs                  | `d.items()`                    |
| `update(d2)`       | Updates with another dict                    | `d.update({'b': 2})`           |
| `pop(key)`         | Removes and returns value for key            | `d.pop('a')`                   |
| `popitem()`        | Removes and returns last key-value pair      | `d.popitem()`                  |
| `clear()`          | Removes all items                            | `d.clear()`                    |
| `setdefault(k, v)` | Returns value if key exists, else sets it    | `d.setdefault('c', 3)`         |
| `copy()`           | Returns a shallow copy                       | `d2 = d.copy()`                |

**Example:**
```python
d = {'a': 1, 'b': 2}
d['c'] = 3
print(d.get('a'))  # 1
print(d.keys())    # dict_keys(['a', 'b', 'c'])
```

---

## 6. String

- **Immutable**
- **Ordered**
- **Allows duplicates**
- **Syntax:** `'text'` or `"text"`

### Common Methods

| Method             | Description                                  | Example                        |
|--------------------|----------------------------------------------|--------------------------------|
| `upper()`          | Converts to uppercase                        | `"abc".upper()`                |
| `lower()`          | Converts to lowercase                        | `"ABC".lower()`                |
| `find(sub)`        | Finds substring, returns index or -1         | `"abc".find("b")`              |
| `replace(a, b)`    | Replaces substring                           | `"abc".replace("a", "x")`      |
| `split(sep)`       | Splits string into list                      | `"a,b,c".split(",")`           |
| `join(list)`       | Joins list into string                       | `",".join(['a','b','c'])`      |
| `strip()`          | Removes whitespace from ends                 | `" abc ".strip()`              |

**Example:**
```python
s = "hello world"
print(s.upper())  # "HELLO WORLD"
```

---

## 7. Useful Concepts

- **List Comprehension:**  
  `[x*2 for x in range(5)]  # [0, 2, 4, 6, 8]`

- **Slicing:**  
  `lst[1:4]  # Elements from index 1 to 3`

- **Unpacking:**  
  `a, b = (1, 2)`

- **Membership:**  
  `if 3 in lst: ...`

- **Copying:**  
  `lst2 = lst.copy()`

---
