# SQL-basics
Basic-Functions are:

1.SELECT Statement
Used to retrieve data from a table.
SELECT name, age FROM students;

2.WHERE Clause
Filters rows based on a condition.
SELECT * FROM employees WHERE salary > 50000;

FROM Clause
Specifies the table name.
SELECT * FROM orders;

Aliasing (AS)
Gives temporary name to column/table.
SELECT salary AS employee_salary FROM workers;

DISTINCT
Removes duplicate values.
SELECT DISTINCT city FROM customers;

2. Aggregating Data
a. COUNT()
Counts number of rows.
SELECT COUNT(*) FROM students;

b. SUM()
Adds values of a column.
SELECT SUM(salary) FROM employees;

c. AVG()
Finds average.
SELECT AVG(marks) FROM exams;

d. MIN() / MAX()
Minimum / Maximum value.
SELECT MAX(price) FROM products;
SELECT MIN(price) FROM products;

e. GROUP BY
Groups rows based on column.
SELECT department, COUNT(*) 
FROM employees 
GROUP BY department;

f.HAVING
Filters groups (used after GROUP BY).
SELECT department, AVG(salary)
FROM employees
GROUP BY department
HAVING AVG(salary) > 40000;

3. Data Modification (DML)
* INSERT
Adds new row.
INSERT INTO students(name, age) VALUES ('Rahul', 20);

* UPDATE
Modifies existing data.
UPDATE employees SET salary = 60000 WHERE id = 3;

* DELETE
Removes rows.
DELETE FROM orders WHERE order_id = 10;
