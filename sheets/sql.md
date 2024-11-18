## SQL

**DQL (Data Query Language)**

|Command|Description|Example|
|:---|:---|:---|
|`SELECT`|Retrieve data from a table|`SELECT * FROM customers;`|
|`FROM`|Specify the table to retrieve data from|`SELECT name, age FROM employees;`|
|`WHERE`|Filter data based on a condition|`SELECT * FROM products WHERE price > 100;`|
|`ORDER BY`|Sort data by one or more columns|`SELECT * FROM orders ORDER BY order_date DESC;`|
|`LIMIT`|Limit the number of rows returned|`SELECT * FROM users LIMIT 10;`|
|`DISTINCT`|Retrieve unique values|`SELECT DISTINCT city FROM customers;`|

**DML (Data Manipulation Language)**

|Command|Description|Example|
|:---|:---|:---|
|`INSERT INTO`|Insert data into a table|`INSERT INTO customers (name, email) VALUES ('John Doe', 'john.doe@example.com');`|
|`UPDATE`|Update data in a table|`UPDATE products SET price = 120 WHERE id = 1;`|
|`DELETE`|Delete data from a table|`DELETE FROM orders WHERE order_date < '2023-01-01';`|

**DDL (Data Definition Language)**

|Command|Description|Example|
|:---|:---|:---|
|`CREATE TABLE`|Create a new table|`CREATE TABLE products (id INT PRIMARY KEY, name VARCHAR(255), price DECIMAL(10,2));`|
|`ALTER TABLE`|Modify an existing table|`ALTER TABLE customers ADD COLUMN phone VARCHAR(20);`|
|`DROP TABLE`|Delete a table|`DROP TABLE products;`|
|`CREATE INDEX`|Create an index on a table|`CREATE INDEX idx_customer_name ON customers (name);`|
|`CREATE DATABASE`|Create a new database|`CREATE DATABASE my_database;`|
|`DROP DATABASE`|Delete a database|`DROP DATABASE my_database;`|

**DCL (Data Control Language)**

|Command|Description|Example|
|:---|:---|:---|
|`GRANT`|Grant privileges to a user|`GRANT SELECT, INSERT ON customers TO user1;`|
|`REVOKE`|Revoke privileges from a user|`REVOKE DROP TABLE ON my_database FROM user2;`|

**DTL (Data Transaction Language)**

|Command|Description|Example|
|:---|:---|:---|
|`BEGIN`|Start a transaction block.|`BEGIN TRANSACTION;`|
|`COMMIT`|Commit the changes made within a transaction.|`COMMIT;`|
|`ROLLBACK`|Rollback the changes made within a transaction.|`ROLLBACK;`|
|`TRANSACTION`|Group multiple statements into a single unit of work|`BEGIN TRANSACTION; UPDATE accounts SET balance = balance - 100 WHERE id = 1; UPDATE accounts SET balance = balance + 100 WHERE id = 2; COMMIT;`|

**Aggregate Functions**

|Command|Description|Example|
|:---|:---|:---|
|`COUNT`|Count the number of rows|`SELECT COUNT(*) FROM orders;`|
|`SUM`|Calculate the sum of a column|`SELECT SUM(price) FROM products;`|
|`AVG`|Calculate the average of a column|`SELECT AVG(age) FROM employees;`|
|`MAX`|Find the maximum value in a column|`SELECT MAX(salary) FROM employees;`|
|`MIN`|Find the minimum value in a column|`SELECT MIN(price) FROM products;`|

**Other Commands**

|Command|Description|Example|
|:---|:---|:---|
|`GROUP BY`|Group rows based on a column|`SELECT city, COUNT(*) FROM customers GROUP BY city;`|
|`HAVING`|Filter grouped data|`SELECT city, COUNT(*) FROM customers GROUP BY city HAVING COUNT(*) > 10;`|
|`JOIN`|Combine data from multiple tables|`SELECT o.order_id, c.name FROM orders o JOIN customers c ON o.customer_id = c.customer_id;`|
|`LEFT JOIN`|Return all rows from the left table, even if there is no match in the right table|`SELECT c.name, o.order_id FROM customers c LEFT JOIN orders o ON c.customer_id = o.customer_id;`|
|`RIGHT JOIN`|Return all rows from the right table, even if there is no match in the left table|`SELECT c.name, o.order_id FROM customers c RIGHT JOIN orders o ON c.customer_id = o.customer_id;`|
|`UNION`|Combine the result sets of two or more `SELECT` statements|`SELECT name FROM customers UNION SELECT name FROM employees;`|
|`INTERSECT`|Return the common rows from two or more `SELECT` statements|`SELECT name FROM customers INTERSECT SELECT name FROM employees;`|
|`EXCEPT`|Return the rows from the first `SELECT` statement that are not present in the second `SELECT` statement|`SELECT name FROM customers EXCEPT SELECT name FROM employees;`|
|`SUBQUERY`|A query nested inside another query|`SELECT * FROM products WHERE price > (SELECT AVG(price) FROM products);`|
|`CASE`|Perform conditional logic|`SELECT name, CASE WHEN age >= 18 THEN 'Adult' ELSE 'Minor' END AS age_group FROM users;`|
|---|Cartesian product is a cross-join which returns all the rows in all the tables listed in a query.|`SELECT c.id, c.nome, c.data_nascimento, c.telefone, p.cargo	FROM clientes AS c, profissoes AS p WHERE c.id_profissao = p.id;`|

**Date functions**
|Command|Description|Example|
|:---|:---|:---|
| `GETDATE()` | Returns the current date and time. | `SELECT GETDATE();` |
| `CURRENT_TIMESTAMP` or `CURTIME` | Returns the current date and time. | `SELECT CURRENT_TIMESTAMP;` |
| `DATEADD(datepart, number, date)` | Adds a specified number of units to a date. | `SELECT DATEADD(day, 7, '2023-12-25');` |
| `DATEDIFF(datepart, startdate, enddate)` | Returns the difference between two dates. | `SELECT DATEDIFF(day, '2023-12-25', '2024-01-01');` |
| `DATEPART(datepart, date)` | Returns a specific part of a date. | `SELECT DATEPART(month, '2023-12-25');` |
| `DAY(date)` | Returns the day of the month. | `SELECT DAY('2023-12-25');` |
| `MONTH(date)` | Returns the month of the year. | `SELECT MONTH('2023-12-25');` |
| `YEAR(date)` | Returns the year. | `SELECT YEAR('2023-12-25');` |

**Tips and Tricks:**

  * Use uppercase for SQL keywords and lowercase for table and column names.
  * Use aliases to make your queries more readable.
  * Use comments to explain your code.
  * Use a database management tool to visualize your data and write queries.

**Resources:**

  * **W3Schools SQL Tutorial:** [https://www.w3schools.com/sql/](https://www.google.com/url?sa=E&source=gmail&q=https://www.w3schools.com/sql/)
  * **SQLBolt:** [https://sqlbolt.com/](https://www.google.com/url?sa=E&source=gmail&q=https://sqlbolt.com/)
  * **Khan Academy SQL Course:** [https://www.khanacademy.org/computing/computer-programming/sql](https://www.google.com/url?sa=E&source=gmail&q=https://www.khanacademy.org/computing/computer-programming/sql)
