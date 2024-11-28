### 1. Define String with its Declaration
- **Definition:** A string is a sequence of characters, often used to represent words, sentences, or any text data in programming. Strings are usually stored as arrays of characters, ending with a null character (`'\0'`) in languages like C/C++.
  
- **Declaration:**
    ```c
    char str[50];  // Declares a string that can hold up to 49 characters (1 reserved for '\0')
    ```

### 2. Write an Algorithm to Find the Length of a Given String
**Algorithm:**
1. **Start**
2. Initialize a counter variable `length` to 0.
3. Loop through each character of the string until you encounter the null character (`'\0'` in C/C++).
    - For each character, increment `length` by 1.
4. End loop when the null character is encountered.
5. The value of `length` now holds the length of the string.
6. **End**

### 3. Write an Algorithm to Copy a String
**Algorithm:**
1. **Start**
2. Declare a destination string array `dest[]` of appropriate size.
3. Initialize an index variable `i` to 0.
4. Loop through each character of the source string `src[]`:
    - Copy each character from `src[i]` to `dest[i]`.
    - Increment `i` by 1.
5. After the loop, assign the null character `'\0'` to `dest[i]`.
6. **End**

### 4. Write an Algorithm for Comparing Two Strings
**Algorithm:**
1. **Start**
2. Initialize an index variable `i` to 0.
3. Loop through each character of both strings `str1[]` and `str2[]`:
    - If `str1[i]` is not equal to `str2[i]`, then:
      - If `str1[i] > str2[i]`, return 1.
      - If `str1[i] < str2[i]`, return -1.
    - Increment `i` by 1.
4. If the loop ends, return 0, indicating that both strings are equal.
5. **End**

### 5. Write an Algorithm to Concatenate Two Strings
**Algorithm:**
1. **Start**
2. Declare a destination string array `dest[]` of appropriate size to hold the concatenated result.
3. Copy all characters from the first string `str1[]` to `dest[]`.
4. Append all characters from the second string `str2[]` to `dest[]`, starting from where `str1[]` ended.
5. Null-terminate the resulting string with `'\0'`.
6. **End**

### 6. Write an Algorithm to Create a Substring from a Given String
**Algorithm:**
1. **Start**
2. Declare a substring array `sub[]` of appropriate size.
3. Initialize two index variables `start` and `end` to define the substring range.
4. Initialize `i` to `start` and `j` to 0.
5. Loop from `start` to `end`:
    - Copy `str[i]` to `sub[j]`.
    - Increment both `i` and `j`.
6. Null-terminate `sub[]` with `'\0'`.
7. **End**

### 7. Write an Algorithm to Insert and Delete a String into a Given String

**Insertion Algorithm:**
1. **Start**
2. Declare a destination array `result[]` to hold the resulting string.
3. Initialize `i` to 0 and loop through the original string `str[]` until you reach the desired insertion point.
4. Copy characters from `str[]` to `result[]`.
5. Insert the new string `insert[]` at the desired point in `result[]`.
6. Continue copying the remaining characters of `str[]` to `result[]`.
7. Null-terminate `result[]` with `'\0'`.
8. **End**

**Deletion Algorithm:**
1. **Start**
2. Declare a destination array `result[]` to hold the resulting string.
3. Initialize `i` to 0 and loop through `str[]` until you reach the start of the deletion range.
4. Skip the characters in the deletion range and continue copying the rest of the string into `result[]`.
5. Null-terminate `result[]` with `'\0'`.
6. **End**

