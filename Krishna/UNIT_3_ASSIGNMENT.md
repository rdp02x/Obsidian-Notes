### 1. Define List. Write Characteristics of List.

A list in Python is an ordered, mutable collection of items that can hold a variety of data types, including numbers, strings, and other objects. Lists are defined using square brackets (`[]`).

#### Characteristics of List:
1. Ordered: The items in a list maintain their order and can be accessed by their index.
2. Mutable: Lists can be changed (elements can be added, removed, or modified) after creation.
3. Heterogeneous: Lists can contain items of different data types.
4. Dynamic: Lists can grow and shrink in size as elements are added or removed.

---

### 2. How to Create a List. Explain `append()`, `extend()`, `insert()` and Delete Operations on List.

Creating a List:
```python
my_list = [1, 2, 3, 'apple', 'banana']
```

#### List Operations:
1. `append()`: Adds an element to the end of the list.
   ```python
   my_list.append('orange')  # my_list becomes [1, 2, 3, 'apple', 'banana', 'orange']
   ```

2. `extend()`: Adds elements from an iterable (like a list) to the end of the list.
   ```python
   my_list.extend([4, 5])  # my_list becomes [1, 2, 3, 'apple', 'banana', 'orange', 4, 5]
   ```

3. `insert()`: Inserts an element at a specified index.
   ```python
   my_list.insert(2, 'grape')  # my_list becomes [1, 2, 'grape', 3, 'apple', 'banana', 'orange', 4, 5]
   ```

4. Delete Operations:
   - `remove()`: Removes the first occurrence of a specified value.
     ```python
     my_list.remove('banana')  # my_list becomes [1, 2, 'grape', 3, 'apple', 'orange', 4, 5]
     ```
   - `pop()`: Removes an element at a specified index and returns it (default is the last item).
     ```python
     my_list.pop()  # removes '5' and returns it, my_list becomes [1, 2, 'grape', 3, 'apple', 'orange', 4]
     ```

---

### 3. Write Characteristics of Tuple. Explain Indexing and Slicing in Tuple.

A tuple in Python is an ordered, immutable collection of items. Tuples are defined using parentheses (`()`).

#### Characteristics of Tuple:
1. Ordered: The items maintain their order and can be accessed by their index.
2. Immutable: Once created, the items in a tuple cannot be changed, added, or removed.
3. Heterogeneous: Tuples can contain items of different data types.
4. Can Contain Duplicate Values: Like lists, tuples can have repeated elements.

#### Indexing and Slicing in Tuple:
- Indexing: Access elements using their index (starting from 0).
  ```python
  my_tuple = (1, 2, 3, 'apple', 'banana')
  print(my_tuple[1])  # Output: 2
  ```

- Slicing: Access a subset of elements using a colon (`:`).
  ```python
  print(my_tuple[1:4])  # Output: (2, 3, 'apple')
  ```

---

### 4. Write Characteristics of Set.

A set in Python is an unordered collection of unique items. Sets are defined using curly braces (`{}`) or the `set()` function.

#### Characteristics of Set:
1. Unordered: The elements do not maintain any specific order.
2. Mutable: Sets can be modified by adding or removing elements.
3. Unique Elements: A set cannot have duplicate items; if duplicates are added, they are ignored.
4. Dynamic: Sets can grow and shrink in size as elements are added or removed.

---

### 5. How Python Set is Modified? Explain `add()`, `update()`, `remove()` and `discard()` Method of Set.

Modifying a Set:
- You can add or remove elements from a set using various methods.

#### Set Methods:
1. `add()`: Adds a single element to the set.
   ```python
   my_set = {1, 2, 3}
   my_set.add(4)  # my_set becomes {1, 2, 3, 4}
   ```

2. `update()`: Adds multiple elements to the set from an iterable (e.g., list, tuple).
   ```python
   my_set.update([5, 6])  # my_set becomes {1, 2, 3, 4, 5, 6}
   ```

3. `remove()`: Removes a specified element from the set. Raises a KeyError if the element is not found.
   ```python
   my_set.remove(3)  # my_set becomes {1, 2, 4, 5, 6}
   ```

4. `discard()`: Removes a specified element from the set. Does not raise an error if the element is not found.
   ```python
   my_set.discard(2)  # my_set becomes {1, 4, 5, 6}
   ```

---

### 6. Explain Mathematical Operations on Set (Union, Intersection, Difference, and Symmetric Difference)

1. Union: Combines two sets and returns a new set containing all unique elements.
   ```python
   set_a = {1, 2, 3}
   set_b = {3, 4, 5}
   union_set = set_a | set_b  # {1, 2, 3, 4, 5}
   ```

2. Intersection: Returns a new set containing elements common to both sets.
   ```python
   intersection_set = set_a & set_b  # {3}
   ```

3. Difference: Returns a new set containing elements in the first set but not in the second.
   ```python
   difference_set = set_a - set_b  # {1, 2}
   ```

4. Symmetric Difference: Returns a new set containing elements in either set, but not in both.
   ```python
   symmetric_difference_set = set_a ^ set_b  # {1, 2, 4, 5}
   ```

---

### 7. Write Characteristics of Dictionary. Explain Operations on Dictionary (Accessing, Changing, Updating, and Removing)

A dictionary in Python is an unordered collection of key-value pairs. Dictionaries are defined using curly braces (`{}`) or the `dict()` function.

#### Characteristics of Dictionary:
1. Unordered: The items do not maintain any specific order.
2. Mutable: Dictionaries can be changed by adding or removing key-value pairs.
3. Key-Value Pairs: Each item is stored as a pair of keys and values.
4. Unique Keys: Each key must be unique within the dictionary.

#### Operations on Dictionary:

- Accessing: Access a value using its key.
  ```python
  my_dict = {'name': 'Alice', 'age': 25}
  print(my_dict['name'])  # Output: Alice
  ```

- Changing: Change the value associated with a key.
  ```python
  my_dict['age'] = 26  # my_dict becomes {'name': 'Alice', 'age': 26}
  ```

- Updating: Add new key-value pairs or update existing ones.
  ```python
  my_dict['city'] = 'New York'  # my_dict becomes {'name': 'Alice', 'age': 26, 'city': 'New York'}
  ```

- Removing: Remove a key-value pair.
  ```python
  del my_dict['age']  # my_dict becomes {'name': 'Alice', 'city': 'New York'}
  ```

---
