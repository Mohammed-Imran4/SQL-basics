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

