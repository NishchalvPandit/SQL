# Databases and SQL

This is my whole summary of learning SQL.


A database is an organized collection of data stored and accessed electronically. It is designed to efficiently manage, store, retrieve, and update large amounts of structured information.

Databases are used in various applications and industries to store and manipulate data in a structured manner, allowing for easy access, retrieval, and analysis of information.

A relational database is a type of database that organizes data into tables with rows and columns, and establishes relationships between the tables.

In a relational database, data is stored in tables, which are structured as two-dimensional grids.


## SQL
SQL (Structured Query Language) is a standardized programming language used for managing and manipulating relational databases. It provides a set of commands and syntax for querying, updating, and managing the data stored in a relational database.
| Command  | Description                                           | Syntax                                                                                 | Example                                                                                  |
|----------|-------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| SELECT   | Retrieve data from a table                            | `SELECT column1, column2, ... FROM table_name;`                                         | `SELECT * FROM employees;`                                                              |
| WHERE    | Filter data based on conditions                        | `SELECT column1, column2, ... FROM table_name WHERE condition;`                         | `SELECT * FROM employees WHERE salary > 50000;`                                          |
| COUNT    | Count the number of rows or occurrences                | `SELECT COUNT(column_name) FROM table_name;`                                            | `SELECT COUNT(*) FROM employees;`                                                       |
| DISTINCT | Retrieve unique values from a column                   | `SELECT DISTINCT column_name FROM table_name;`                                           | `SELECT DISTINCT department FROM employees;`                                             |
| LIMIT    | Limit the number of rows returned                      | `SELECT column1, column2, ... FROM table_name LIMIT number_of_rows;`                    | `SELECT * FROM employees LIMIT 10;`                                                      |
| INSERT   | Insert new data into a table                           | `INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);`          | `INSERT INTO employees (name, age, salary) VALUES ('John', 30, 60000);`                   |
| UPDATE   | Modify existing data in a table                        | `UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;`        | `UPDATE employees SET salary = 65000 WHERE employee_id = 101;`                            |
| DELETE   | Remove data from a table                               | `DELETE FROM table_name WHERE condition;`                                                | `DELETE FROM employees WHERE employee_id = 101;`                                         |
