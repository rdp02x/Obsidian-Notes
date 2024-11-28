### 1. Explain Linux Architecture in Detail

The Linux architecture is composed of several layers that work together to run programs and manage system resources efficiently. The major components include:

1. Hardware Layer:
   - The lowest layer, consisting of physical components like the CPU, memory, storage, and input/output devices. This layer interacts directly with the kernel.

2. Kernel Layer:
   - The core of the operating system, responsible for managing hardware resources and abstracting them for higher layers.
   - Functions of the kernel include:
     - Process Management
     - Memory Management
     - Device Drivers
     - File System Management

3. Shell:
   - An interface between the user and the kernel. It allows users to execute commands by typing them.
   - Different types of shells include bash, zsh, csh, etc.

4. System Libraries:
   - Libraries that provide functions and tools for the application software to interact with the kernel.

5. User Applications:
   - The top layer, consisting of user programs and utilities such as text editors, browsers, and file managers.

---

### 2. Explain Following Linux Commands

1. `pwd`: Prints the current working directory.
2. `cat`: Concatenates and displays the content of files.
3. `wc`: Counts the number of words, lines, and characters in a file.
4. `chmod`: Changes file permissions.
5. `comm`: Compares two sorted files line by line.
6. `head`: Displays the first few lines of a file (default is 10).
7. `grep`: Searches for a pattern in a file.
8. `sort`: Sorts the content of a file alphabetically or numerically.
9. `cmp`: Compares two files byte by byte.
10. `ls`: Lists files and directories.
11. `date`: Displays the current date and time.
12. `who`: Shows who is logged into the system.
13. `cp`: Copies a file or directory.
14. `mkdir`: Creates a new directory.

---

### 3. Explain Branching Statement if…else and if…elseif… ladder

- `if…else` Statement:
   The `if` statement checks a condition, and if the condition is true, a block of code is executed. If false, the `else` block is executed.
   
   Example:
   ```bash
   if [ $a -gt $b ]; then
       echo "a is greater"
   else
       echo "b is greater"
   fi
   ```

- `if…elseif` Ladder:
   Used when multiple conditions are evaluated. It checks each `if` condition in sequence until one evaluates to true.
   
   Example:
   ```bash
   if [ $a -gt $b ]; then
       echo "a is greater"
   elif [ $a -eq $b ]; then
       echo "a and b are equal"
   else
       echo "b is greater"
   fi
   ```

---

### 4. What is File Permission in Linux? Explain Using `chmod` Command

File permissions in Linux determine who can read, write, or execute a file or directory. Each file has three types of permissions:
1. Read (r): Permission to read the file or list a directory.
2. Write (w): Permission to modify a file or write inside a directory.
3. Execute (x): Permission to run the file as a program or traverse the directory.

There are three categories of users for file permissions:
- Owner: The user who owns the file.
- Group: The group of users who share access to the file.
- Others: All other users.

Using `chmod`:
- `chmod` changes file permissions. It can be used with symbolic or numeric representations.

Numeric Representation:
- r = 4, w = 2, x = 1
- Combine values for different permissions (e.g., 7 = rwx, 5 = r-x).

---

### 5. Write a Shell Script to Sum of 1 to 10 Using While Loop

```bash
sum=0
i=1
while [ $i -le 10 ]; do
    sum=$((sum + i))
    i=$((i + 1))
done
echo "Sum of numbers from 1 to 10 is: $sum"
```

---

### 6. Write a Shell Script to Find Minimum from Three Numbers

```bash
echo "Enter three numbers:"
read a
read b
read c

if [ $a -le $b ] && [ $a -le $c ]; then
    echo "$a is the smallest"
elif [ $b -le $a ] && [ $b -le $c ]; then
    echo "$b is the smallest"
else
    echo "$c is the smallest"
fi
```

---

### 7. Write a Shell Script to Make Arithmetic Calculator

```bash
echo "Enter two numbers:"
read a
read b
echo "Enter operation (+, -, *, /):"
read op

case $op in
    +) result=$((a + b)) ;;
    -) result=$((a - b)) ;;
    \*) result=$((a * b)) ;;
    /) result=$((a / b)) ;;
    *) echo "Invalid operation" ;;
esac

echo "Result: $result"
```

---

### 8. Write a Shell Script to Find Greater Number Between Two Numbers

```bash

echo "Enter two numbers:"
read a
read b

if [ $a -gt $b ]; then
    echo "$a is greater"
else
    echo "$b is greater"
fi
```

---

### 9. Write a Shell Script to Check Given Number is Odd or Even

```bash
echo "Enter a number:"
read num

if [ $((num % 2)) -eq 0 ]; then
    echo "$num is even"
else
    echo "$num is odd"
fi
```

---

### 10. Write a Shell Script to Count Number of Words, Characters, and Lines from a Given File

```bash
echo "Enter filename:"
read filename

if [ -f "$filename" ]; then
    echo "Lines: $(wc -l < $filename)"
    echo "Words: $(wc -w < $filename)"
    echo "Characters: $(wc -c < $filename)"
else
    echo "File does not exist"
fi
```

---

### 11. Write a Shell Script to Find Maximum Out of Three Numbers

```bash
echo "Enter three numbers:"
read a
read b
read c

if [ $a -ge $b ] && [ $a -ge $c ]; then
    echo "$a is the largest"
elif [ $b -ge $a ] && [ $b -ge $c ]; then


    echo "$b is the largest"
else
    echo "$c is the largest"
fi
```

---

### 12. Write a Shell Script that Accepts a String in Lowercase and Converts It into Uppercase

```bash
echo "Enter a string in lowercase:"
read str
echo "Uppercase: $(echo $str | tr 'a-z' 'A-Z')"
```

---

### 13. Write a Shell Script to Find Factorial of a Given Number

```bash
echo "Enter a number:"
read num
factorial=1

for ((i=1; i<=num; i++)); do
    factorial=$((factorial * i))
done

echo "Factorial of $num is $factorial"
```

---

### 14. Write a Shell Script to Find Whether the Given String is Palindrome or Not

```bash
echo "Enter a string:"
read str

reverse=$(echo $str | rev)

if [ "$str" == "$reverse" ]; then
    echo "$str is a palindrome"
else
    echo "$str is not a palindrome"
fi
```