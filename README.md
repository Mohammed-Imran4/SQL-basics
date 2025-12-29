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

* TRUNCATE
Deletes all rows (faster than DELETE).
TRUNCATE TABLE logs;

4. Indexing
*. Create Index
Speeds up search.
CREATE INDEX idx_name ON students(name);

*. Drop Index
DROP INDEX idx_name;

*. Composite Index
Multiple columns.
CREATE INDEX idx_stu ON students(name, age);

*. Unique Index
Values cannot repeat.
CREATE UNIQUE INDEX idx_email ON users(email);

5. Conversion Functions
a. CAST
Converts datatype.
SELECT CAST(price AS INT) FROM products;

b.TO_NUMBER / TO_CHAR
Oracle/MySQL string conversions.
SELECT TO_CHAR(salary) FROM employees;

c. COALESCE
Returns first non-null value.
SELECT COALESCE(middle_name, 'Not Available') FROM users;

6. Filtering Data
*. BETWEEN
Range filter.
SELECT * FROM items WHERE price BETWEEN 100 AND 500;

*. LIKE
Pattern matching.
SELECT * FROM students WHERE name LIKE 'A%';

. IN
Multiple values.
SELECT * FROM employees WHERE department IN ('HR', 'Sales');

*. AND / OR / NOT
SELECT * FROM products 
WHERE price < 500 AND category = 'Mobile';

7. Sorting and Limiting
a. ORDER BY
SELECT * FROM students ORDER BY marks DESC;

b. LIMIT (MySQL)
SELECT * FROM books LIMIT 5;

c.OFFSET
SELECT * FROM books LIMIT 5 OFFSET 10;

8. Set Operations
*. UNION
Merge results – removes duplicates.

SELECT city FROM customers
UNION
SELECT city FROM suppliers;

*. UNION ALL
Includes duplicates.

SELECT city FROM customers
UNION ALL
SELECT city FROM suppliers;

*. INTERSECT
Common rows.

SELECT id FROM table1
INTERSECT
SELECT id FROM table2;

*. EXCEPT / MINUS
Returns rows in first table but not second.

9. Joins
a. INNER JOIN
Matching rows only.

SELECT students.name, marks.score
FROM students
INNER JOIN marks ON students.id = marks.student_id;
