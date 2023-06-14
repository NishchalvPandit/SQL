# Databases and SQL

A database is an organized collection of data stored and accessed electronically. It is designed to efficiently manage, store, retrieve, and update large amounts of structured information.

Databases are used in various applications and industries to store and manipulate data in a structured manner, allowing for easy access, retrieval, and analysis of information.

A relational database is a type of database that organizes data into tables with rows and columns, and establishes relationships between the tables.

In a relational database, data is stored in tables, which are structured as two-dimensional grids.


## SQL
SQL (Structured Query Language) is a standardized programming language used for managing and manipulating relational databases. It provides a set of commands and syntax for querying, updating, and managing the data stored in a relational database.
## DML
DML (Data Manipulation Language): It is used to manipulate the data stored in the database.

| Command  | Description                                           | Syntax                                                                                 | Example                                                                                  |
|----------|-------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| SELECT   | Retrieve data from a table                            | `SELECT column1, column2, ... FROM table_name;`                                         | `SELECT * FROM employees;`                                                              |
| WHERE    | Filter data based on conditions                        | `SELECT column1, column2, ... FROM table_name WHERE condition;`                         | `SELECT * FROM employees WHERE salary > 50000;`                                          |
| COUNT    | Count the number of rows or occurrences                | `SELECT COUNT(column_name) FROM table_name;`                                            | `SELECT COUNT(*) FROM employees;`                                                       |
| DISTINCT | Retrieve unique values from a column                   | `SELECT DISTINCT column_name FROM table_name;`                                           | `SELECT DISTINCT department FROM employees;`                                             |
| LIMIT    | Limit the number of rows returned                      | `SELECT column1, column2, ... FROM table_name LIMIT number_of_rows;`                    | `SELECT * FROM employees LIMIT 10;`                                                      |
| INSERT   | Insert new data into a table                           | `INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);`          | `INSERT INTO employees (name, age, salary) VALUES ('John', 30, 60000);`                   |
| UPDATE   | Modify existing data in a table                        | `UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;`        | `UPDATE employees SET salary = 65000 WHERE employee_id = 101;`                            |
| DELETE   | Remove data from a table                               | `DELETE FROM table_name WHERE condition;`                                                | `DELETE FROM employees WHERE employee_id = 101;`  \


## DDL
DDL (Data Definition Language): It is used to define and manage the structure of database objects.

| Operation   | Syntax                                     | Example                                 | Use                                      |
|-------------|--------------------------------------------|-----------------------------------------|------------------------------------------|
| Create      | `CREATE TABLE table_name ( ... );`          | `CREATE TABLE employees ( ... );`       | Create a new table with specified columns |
| Alter       | `ALTER TABLE table_name ADD COLUMN ... ;`   | `ALTER TABLE employees ADD COLUMN ... ;`| Add a new column to an existing table     |
| Truncate    | `TRUNCATE TABLE table_name;`                | `TRUNCATE TABLE employees;`             | Remove all rows from a table              |

## Refining the results

| Command    | Syntax                                                      | Description                                                                                                                                                   | Example                                                                                                                      |
|------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| LIKE       | `SELECT column1, column2, ... FROM table_name WHERE columnN LIKE pattern;` | The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.                                                                   | `SELECT f_name, l_name FROM employees WHERE address LIKE '%Elgin,IL%';`                                                      |
| BETWEEN    | `SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value1 AND value2;` | The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates. The BETWEEN operator is inclusive: begin and end values are included. | `SELECT * FROM employees WHERE salary BETWEEN 40000 AND 80000;`                                                             |
| ORDER BY   | `SELECT column1, column2, ... FROM table_name ORDER BY column1, column2, ... ASC/DESC;` | The ORDER BY keyword is used to sort the result-set in ascending or descending order. The default is ascending.                                               | `SELECT f_name, l_name, dep_id FROM employees ORDER BY dep_id DESC, l_name;`                                                 |
| GROUP BY   | `SELECT column_name(s) FROM table_name WHERE condition GROUP BY column_name(s) ORDER BY column_name(s);` | The GROUP BY clause is used in collaboration with the SELECT statement to arrange identical data into groups.                                               | `SELECT dep_id, COUNT(*) FROM employees GROUP BY dep_id;`                                                                    |
