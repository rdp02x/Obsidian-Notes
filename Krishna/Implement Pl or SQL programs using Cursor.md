1. Create Table `employees`
```sql
CREATE TABLE employees (
    employee_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    salary DECIMAL(10, 2),
    department_id INT
);
```

 2. Insert Data into `employees`
```sql
INSERT INTO employees (name, salary, department_id) 
VALUES ('John Doe', 5500, 2);

INSERT INTO employees (name, salary, department_id) 
VALUES ('Jane Smith', 4500, 3);

INSERT INTO employees (name, salary, department_id) 
VALUES ('Alice Johnson', 7000, 1);
```

 3. Cursor Declaration and Insertion into `high_salar_employees`
```sql
DELIMITER //

DECLARE
    CURSOR emp_cursor IS
        SELECT employee_id, name, salary
        FROM employees
        WHERE salary > 5000;

    v_emp_id employeesemployee_id%TYPE;
    v_emp_name employeesname%TYPE;
    v_salary employeessalary%TYPE;

BEGIN
    OPEN emp_cursor;

    LOOP
        FETCH emp_cursor INTO v_emp_id, v_emp_name, v_salary;
        EXIT WHEN emp_cursor%NOTFOUND;
        
        INSERT INTO high_salar_employees (emp_id, emp_name, salary)
        VALUES (v_emp_id, v_emp_name, v_salary);
    END LOOP;

    CLOSE emp_cursor;
    COMMIT;

    DBMS_OUTPUTPUT_LINE('Insert into high_salary_employees table completed successfully');
END;
//

DELIMITER ;
```

 4. Display Data from `employees`
```sql
SELECT * FROM employees;
```

 - Output
```
+-------------+--------------+---------+---------------+
| employee_id | name        | salary  | department_id |
+-------------+--------------+---------+---------------+
| 1           | John Doe    | 550000 | 2             |
| 2           | Jane Smith  | 450000 | 3             |
| 3           | Alice Johnson| 700000| 1             |
+-------------+--------------+---------+---------------+
```