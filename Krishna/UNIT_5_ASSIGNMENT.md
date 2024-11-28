### 1. Define String. How to Create a List of Strings

A string is a sequence of characters enclosed within single (`' '`) or double (`" "`) quotes in Python.

To create a list of strings:
```python
string_list = ["apple", "banana", "cherry"]
print(string_list)
```

---

### 2. How to Use Slicing Operator for String. Explain with Example

Slicing allows you to access a portion of a string. The syntax for slicing is `string[start:end:step]`.

Example:
```python
text = "Hello, World!"
print(text[0:5])
print(text[7:12])
print(text[::2])
```

- `text[0:5]` slices from index 0 to 4.
- `text[7:12]` slices from index 7 to 11.
- `text[::2]` slices the entire string but takes every second character.

---

### 3. Explain Following Functions with Example

- `isalnum()`: Returns `True` if all characters are alphanumeric (letters and numbers).
    ```python
    print("abc123".isalnum())
    ```

- `isalpha()`: Returns `True` if all characters are alphabetic.
    ```python
    print("hello".isalpha())
    ```

- `isdigit()`: Returns `True` if all characters are digits.
    ```python
    print("123".isdigit())
    ```

- `isidentifier()`: Returns `True` if the string is a valid identifier in Python.
    ```python
    print("variable1".isidentifier())    
    ```

- `islower()`: Returns `True` if all alphabetic characters are in lowercase.
    ```python
    print("hello".islower())
    ```

- `isupper()`: Returns `True` if all alphabetic characters are in uppercase.
    ```python
    print("HELLO".isupper())
    ```

- `isspace()`: Returns `True` if all characters are whitespace.
    ```python
    print("   ".isspace())
    ```

---

### 4. Explain Following Functions with Example

- `endswith()`: Checks if the string ends with a specified suffix.
    ```python
    print("hello.py".endswith(".py"))  # Output: True
    ```

- `startswith()`: Checks if the string starts with a specified prefix.
    ```python
    print("hello.py".startswith("hello"))
    ```

- `find()`: Returns the first occurrence index of a substring. Returns `-1` if not found.
    ```python
    print("hello world".find("world"))
    ```

- `rfind()`: Returns the last occurrence index of a substring. Returns `-1` if not found.
    ```python
    print("hello world world".rfind("world"))
    ```

- `count()`: Returns the number of occurrences of a substring.
    ```python
    print("banana".count("a"))
    ```

---

### 5. List Out Formatting Functions and Explain Any Two

Common string formatting functions:
- `format()`
- `join()`
- `ljust()`
- `rjust()`
- `center()`

Example:

- `format()`: Used to insert values into a string using placeholders `{}`.
    ```python
    print("My name is {}".format("Alice"))
    ```

- `join()`: Joins elements of a list into a single string, with a specified separator.
    ```python
    words = ["apple", "banana", "cherry"]
    print(", ".join(words))
    ```

---

### 6. Difference Between Text Files and Binary Files

| Text Files                               | Binary Files                                |
|----------------------------------------------|-------------------------------------------------|
| Store data in a human-readable format.       | Store data in a machine-readable format.        |
| Characters are encoded using a character set (e.g., ASCII). | Data is stored as raw bytes.                    |
| Example: `.txt`, `.csv`                      | Example: `.bin`, `.exe`                         |

---

### 7. Explain `open()` and `close()` for File with Example

- `open()`: Opens a file and returns a file object. Requires file mode (`'r'`, `'w'`, `'a'`, etc.).
- `close()`: Closes the file and frees up the system resources.

Example:
```python
file = open("example.txt", "r")
print(file.read())
file.close()
```

---

### 8. Explain `read()`, `readline()`, and `readlines()` for File with Example

- `read()`: Reads the entire file content as a single string.
    ```python
    file = open("example.txt", "r")
    print(file.read())
    file.close()
    ```

- `readline()`: Reads one line at a time.
    ```python
    file = open("example.txt", "r")
    print(file.readline())
    file.close()
    ```

- `readlines()`: Reads all lines as a list of strings.
    ```python
    file = open("example.txt", "r")
    print(file.readlines())
    file.close()
    ```

---

### 9. Explain `write()`, `append()`, and `writelines()` for File with Example

- `write()`: Writes a string to the file.
    ```python
    file = open("example.txt", "w")
    file.write("Hello, World!")
    file.close()
    ```

- `append()`: Appends content to the end of the file.
    ```python
    file = open("example.txt", "a")
    file.write("\nNew Line")
    file.close()
    ```

- `writelines()`: Writes a list of strings to the file.
    ```python
    file = open("example.txt", "w")
    file.writelines(["Line 1\n", "Line 2\n", "Line 3\n"])
    file.close()
    ```