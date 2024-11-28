### 1. Explain PUSH and POP Algorithm of Stack
- **PUSH Algorithm:**
  1. **Start**
  2. Check if the stack is full.
     - If full, print "Stack Overflow" and exit.
  3. If not full, increment the `top` pointer by 1.
  4. Add the new element at the position pointed by `top`.
  5. **End**

- **POP Algorithm:**
  1. **Start**
  2. Check if the stack is empty.
     - If empty, print "Stack Underflow" and exit.
  3. If not empty, access the element pointed by `top`.
  4. Decrement the `top` pointer by 1.
  5. Return the accessed element.
  6. **End**

### 2. Write Applications of Stack
- **Function Call Management:** Used in handling function calls and recursion in programming.
- **Expression Evaluation:** Conversion between infix, prefix, and postfix notations, as well as evaluation of expressions.
- **Backtracking Algorithms:** Helps in solving problems like maze traversal, pathfinding, etc.
- **Undo Mechanism:** In text editors or other applications where you can undo the last operation.
- **Syntax Parsing:** Used in compilers to check matching parentheses and other symbols.

### 3. Explain Infix, Prefix, and Postfix Form Expressions
- **Infix:** The operator is between the operands. Example: `A + B`.
- **Prefix:** The operator precedes the operands. Example: `+AB`.
- **Postfix:** The operator follows the operands. Example: `AB+`.

### 4. 'A / B ^ C + D * E - A * C' convert infix form to Postfix form.
1. **Infix:** `A / B ^ C + D * E - A * C`
2. **Postfix Conversion:**
   - Step 1: Identify operators and operands.
   - Step 2: Apply operator precedence and associativity rules.
   - **Result:** `ABC^/DE*+AC*-`

### 5. 'A * (B + C) * D' convert infix to Prefix.
1. **Infix:** `A * (B + C) * D`
2. **Prefix Conversion:**
   - Step 1: Identify operators and operands.
   - Step 2: Apply operator precedence and associativity rules.
   - **Result:** `*A*+BCD`

### 6. Convert a given Infix expression 'a * b $ c / d – e + f – g' into prefix Form.
1. **Infix:** `a * b $ c / d – e + f – g`
2. **Prefix Conversion:**
   - Step 1: Identify operators and operands.
   - Step 2: Apply operator precedence and associativity rules.
   - **Result:** `- + - * a $ b c / d e f g`

### 7. Write an Algorithm for Delete Operation in a Circular Queue
**Algorithm:**
1. **Start**
2. Check if the queue is empty.
   - If empty, print "Queue Underflow" and exit.
3. If not empty, access the element at `front`.
4. Increment `front` by 1 (mod `max_size`).
   - If `front == rear`, reset both `front` and `rear` to -1 (queue becomes empty).
5. Return the accessed element.
6. **End**

### 8. Write an Algorithm for Delete Operation in a Queue
**Algorithm:**
1. **Start**
2. Check if the queue is empty.
   - If empty, print "Queue Underflow" and exit.
3. If not empty, access the element at `front`.
4. Increment `front` by 1.
   - If `front` exceeds `rear`, reset both `front` and `rear` to -1 (queue becomes empty).
5. Return the accessed element.
6. **End**

### 9. Define circular queue. Explain INSERT and DELETE operations of circular queue with diagrams.
- **Definition:** A circular queue is a linear data structure that follows the FIFO principle but connects the end of the queue back to the front, forming a circle. It efficiently uses space by recycling empty positions.

- **INSERT Operation:**
  - Check if the queue is full. If full, print "Queue Overflow".
  - Increment `rear` by 1 (mod `max_size`) and add the new element.
  - If the queue was empty (`front == -1`), set `front = 0`.

- **DELETE Operation:**
  - Check if the queue is empty. If empty, print "Queue Underflow".
  - Access and remove the element at `front`.
  - Increment `front` by 1 (mod `max_size`).
  - If `front` equals `rear`, reset both `front` and `rear` to -1.

### 10. Convert following infix expression into postfix expression. 'a + b * ( c / d ) – e'
1. **Infix:** `a + b * ( c / d ) – e`
2. **Postfix Conversion:**
   - Step 1: Identify operators and operands.
   - Step 2: Apply operator precedence and associativity rules.
   - **Result:** `abcd/*+e-`

### 11. Differentiate Between Stack and Queue

| **Stack**                 | **Queue**                  |
| ------------------------- | -------------------------- |
| LIFO (Last In, First Out) | FIFO (First In, First Out) |
| PUSH (Add)                | ENQUEUE (Add)              |
| POP (Remove)              | DEQUEUE (Remove)           |
| Access from the top       | Access from the front      |
| Example: Undo button      | Example: Waiting in line   |
### 12. Consider size of stack as 6. Perform following operation on stack and show the status of stack and top pointer after each operation.
-  **Push a, b:**
    ```
    Stack: [a, b, - , - , - , -]
    Top: 1
    ```
  - **Pop:**
    ```
    Stack: [a, - , - , - , - , -]
    Top: 0
    ```
  - **Push c:**
    ```
    Stack: [a, c, - , - , - , -]
    Top: 1
    ```
  - **Pop:**
    ```
    Stack: [a, - , - , - , - , -]
    Top: 0
    ```
  - **Pop:**
    ```
    Stack: [- , - , - , - , - , -]
    Top: -1 (empty stack)
    ```

