### 1. Define VIEW, Types, Creation, and Advantages
- A view in SQL is a virtual table based on the result of a SQL query. It does not store data physically but displays data stored in tables.
- **Types of Views:**
  - **Simple View:** Based on a single table, does not contain functions, groups, or subqueries.
  - **Complex View:** Based on multiple tables and can include functions, joins, groupings, etc.
- **How to Create a View:**
  ```sql
  CREATE VIEW view_name AS
  SELECT column1, column2, ...
  FROM table_name
  WHERE condition;
  ```
- **Advantages of Views:**
  - Simplifies complex queries.
  - Allows for a customized presentation of data.
  - Can help in preserving backward compatibility.

### 2. Explain Synonyms, Creation, and Destruction
- **Definition:** A synonym in SQL is an alias or alternative name for a database object such as a table, view, sequence, or stored procedure.
- **Syntax for Creation:** `CREATE SYNONYM synonym_name FOR object_name;`
- **Syntax for Destruction:** `DROP SYNONYM synonym_name;`

### 3. What is a Sequence? Creation and Destruction
- **Definition:** A sequence in SQL is a database object that generates a sequence of unique numbers. It's commonly used to auto-generate primary key values.
- **How to Create a Sequence:**
  ```sql
  CREATE SEQUENCE sequence_name
  START WITH initial_value
  INCREMENT BY increment_value
  [MAXVALUE max_value]
  [MINVALUE min_value]
  [CYCLE | NOCYCLE];
  ```
- **How to Destroy a Sequence:**
  ```sql
  DROP SEQUENCE sequence_name;
  ```

### 4. What is an Index? Types with Example
- **Definition:** An index in SQL is used to speed up the retrieval of rows by using a pointer. It's a performance enhancement technique.
- **Types of Indexes:**
  - **Unique Index:** Ensures that the indexed column has unique values.
  - **Non-Unique Index:** Allows duplicate values in the indexed column.
  - **Composite Index:** An index on two or more columns.
  - **Clustered Index:** Alters the physical order of the data in the table.
  - **Non-Clustered Index:** Does not alter the physical order of the data.
- **Example of Creating an Index:**
  ```sql
  CREATE INDEX idx_employee_name
  ON Employees (LastName);
  ```

### 5. Explain Foreign Key
- **Definition:** A foreign key in SQL is a field (or collection of fields) in one table that uniquely identifies a row in another table. It creates a link between two tables.
- **Example:**
  ```sql
  CREATE TABLE Orders (
    OrderID int PRIMARY KEY,
    CustomerID int,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
  );
  ```

### 6. Explain UNIQUE Key
- **Definition:** A UNIQUE key in SQL ensures that all values in a column or a set of columns are unique across all rows in a table.
- **Example:**
  ```sql
  CREATE TABLE Employees (
    EmployeeID int UNIQUE,
    Email varchar(255) UNIQUE
  );
  ```

### 7. Explain Primary Key
- **Definition:** A primary key is a field in a table that uniquely identifies each row/record in that table. It must contain unique values and cannot contain NULLs.
- **Example:**
  ```sql
  CREATE TABLE Employees (
    EmployeeID int PRIMARY KEY,
    LastName varchar(255),
    FirstName varchar(255)
  );
  ```

### 8. Explain `NOT NULL` and `CHECK` Constraints
- **NOT NULL Constraint:**
  - **Definition:** Ensures that a column cannot have a NULL value.
  - **Example:**
    ```sql
    CREATE TABLE Employees (
      EmployeeID int NOT NULL,
      LastName varchar(255) NOT NULL
    );
    ```

- **CHECK Constraint:**
  - **Definition:** Ensures that all values in a column satisfy a specific condition.
  - **Example:**
    ```sql
    CREATE TABLE Employees (
      EmployeeID int NOT NULL,
      Age int CHECK (Age >= 18)
    );
    ```
