## SQL

**DQL (Data Query Language)**

|Command|Description|Example|
|:---|:---|:---|
|`SELECT`|Retrieve data from a table|`SELECT * FROM customers;`|
|`FROM`|Specify the table to retrieve data from|`SELECT name, age FROM employees;`|
|`WHERE`|Filter data based on a condition|`SELECT * FROM products WHERE price > 100;`|
|`ORDER BY`|Sort data by one or more columns|`SELECT * FROM orders ORDER BY order_date DESC;`|
|`LIMIT`|Limit the number of rows returned (MySQL, PostgreSQL, SQLite)|`SELECT * FROM users LIMIT 10;`|
|`TOP`|Limit the number of rows returned (SQL Server)|`SELECT TOP 10 * FROM users;`|
|`DISTINCT`|Retrieve unique values|`SELECT DISTINCT city FROM customers;`|
|`GROUP BY`|Group rows based on a column|`SELECT city, COUNT(*) FROM customers GROUP BY city;`|
|`HAVING`|Filter grouped data|`SELECT city, COUNT(*) FROM customers GROUP BY city HAVING COUNT(*) > 10;`|

**DML (Data Manipulation Language)**

|Command|Description|Example|
|:---|:---|:---|
|`INSERT INTO`|Insert data into a table|`INSERT INTO customers (name, email) VALUES ('John Doe', 'john.doe@example.com');`|
|`UPDATE`|Update data in a table|`UPDATE products SET price = 120 WHERE id = 1;`|
|`DELETE`|Delete data from a table|`DELETE FROM orders WHERE order_date < '2023-01-01';`|
|`TRUNCATE`|Quickly remove all records from a table.| `TRUNCATE TABLE customers;` |

**DDL (Data Definition Language)**

|Command|Description|Example|
|:---|:---|:---|
|`CREATE TABLE`|Create a new table|`CREATE TABLE products (id INT PRIMARY KEY, name VARCHAR(255), price DECIMAL(10,2));`|
|`ALTER TABLE`|Modify an existing table|`ALTER TABLE customers ADD COLUMN phone VARCHAR(20);`|
|`DROP TABLE`|Delete a table|`DROP TABLE products;`|
|`CREATE INDEX`|Create an index on a table|`CREATE INDEX idx_customer_name ON customers (name);`|
|`CREATE DATABASE`|Create a new database|`CREATE DATABASE my_database;`|
|`DROP DATABASE`|Delete a database|`DROP DATABASE my_database;`|

**SQL Operators**
| Operator       | Description                                   | Example                               |
|----------------|-----------------------------------------------|----------------------------------------|
| `=`            | Equal to                                      | `SELECT * FROM users WHERE age = 30;` |
| `<>` or `!=`   | Not equal to                                  | `SELECT * FROM users WHERE age <> 30;` |
| `>`            | Greater than                                  | `SELECT * FROM products WHERE price > 100;` |
| `<`            | Less than                                     | `SELECT * FROM products WHERE price < 50;` |
| `>=`           | Greater than or equal to                      | `SELECT * FROM users WHERE age >= 18;` |
| `<=`           | Less than or equal to                         | `SELECT * FROM users WHERE age <= 65;` |
| `BETWEEN`      | Value within a range                          | `SELECT * FROM orders WHERE total BETWEEN 100 AND 500;` |
| `LIKE`         | Pattern matching using wildcards              | `SELECT * FROM customers WHERE name LIKE 'J%';` |
| `IN`           | Match any value in a list                     | `SELECT * FROM users WHERE country IN ('US', 'CA');` |
| `AND`          | Combine conditions (both must be true)        | `SELECT * FROM users WHERE age > 18 AND active = 1;` |
| `OR`           | Combine conditions (at least one true)        | `SELECT * FROM users WHERE age < 18 OR active = 0;` |
| `NOT`          | Negates a condition                           | `SELECT * FROM users WHERE NOT active = 1;` |
| `IS NULL`      | Check for NULL                                | `SELECT * FROM logs WHERE deleted_at IS NULL;` |
| `IS NOT NULL`  | Check for NOT NULL                            | `SELECT * FROM logs WHERE deleted_at IS NOT NULL;` |

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

**String Functions**

|Command|Description|Example|
|:---|:---|:---|
|`CONCAT`|Joins two or more strings together.|`SELECT CONCAT(first_name, ' ', last_name) AS full_name;`|
|`UPPER`|Converts a string to uppercase.|`SELECT UPPER(name) FROM customers;`|
|`LOWER`|Converts a string to lowercase.|`SELECT LOWER(email) FROM users;`|
|`TRIM`|Removes leading and trailing spaces from a string.|`SELECT TRIM('   hello   ');`|
|`REPLACE`|Replaces occurrences of a substring within a string.|`SELECT REPLACE('SQL Tutorial', 'Tutorial', 'Guide');`|
|`LEN`|Returns the number of characters in a string.|`SELECT LEN(name) FROM products;`|
|`LEFT`|Returns the leftmost characters from a string.|`SELECT LEFT('Database', 4); -- returns 'Data'`|
|`RIGHT`|Returns the rightmost characters from a string.|`SELECT RIGHT('Database', 4); -- returns 'base'`|
|`SUBSTRING`| Extracts part of a string starting at a position.|`SELECT SUBSTRING('Database', 5, 3); -- returns 'bas'`|

**Numeric Functions**

|Command|Description|Example|
|:---|:---|:---|
|`COUNT`|Count the number of rows|`SELECT COUNT(*) FROM orders;`|
|`SUM`|Calculate the sum of a column|`SELECT SUM(price) FROM products;`|
|`AVG`|Calculate the average of a column|`SELECT AVG(age) FROM employees;`|
|`MAX`|Find the maximum value in a column|`SELECT MAX(salary) FROM employees;`|
|`MIN`|Find the minimum value in a column|`SELECT MIN(price) FROM products;`|
|`ROUND`|Round a number to a specified number of decimals|`SELECT ROUND(price, 2) FROM products;`|
|`ABS`|Return the absolute (positive) value of a number|`SELECT ABS(balance) FROM accounts;`|

**SQL Joins**

|Command|Description|Example|
|:---|:---|:---|
|`INNER JOIN`|Combine data from multiple tables|`SELECT o.order_id, c.name FROM orders o INNER JOIN customers c ON o.customer_id = c.customer_id;`|
|`LEFT JOIN`| Return all rows from the left table, even if there is no match in the right table|`SELECT c.name, o.order_id FROM customers c LEFT JOIN orders o ON c.customer_id = o.customer_id;`|
|`RIGHT JOIN`|Return all rows from the right table, even if there is no match in the left table|`SELECT c.name, o.order_id FROM customers c RIGHT JOIN orders o ON c.customer_id = o.customer_id;`|
|`FULL JOIN`|Return all rows when there is a match in either table; missing matches are filled with NULLs|`SELECT c.name, o.order_id FROM customers c FULL JOIN orders o ON c.customer_id = o.customer_id;`|
|`LEFT ANTI JOIN`|Return rows from the left table that **do not** have a match in the right table|`SELECT c.* FROM customers c LEFT JOIN orders o ON c.customer_id = o.customer_id WHERE o.customer_id IS NULL;`|
|`RIGHT ANTI JOIN`|Return rows from the right table that **do not** have a match in the left table|`SELECT o.* FROM orders o RIGHT JOIN customers c ON c.customer_id = o.customer_id WHERE c.customer_id IS NULL;`|
|`FULL ANTI JOIN`|Return rows from both tables that **do not** match each other|`SELECT * FROM customers c FULL JOIN orders o ON c.customer_id = o.customer_id WHERE c.customer_id IS NULL OR o.customer_id IS NULL;`|
|`CROSS JOIN`|Return the Cartesian product of both tables (all combinations of rows)|`SELECT c.name, o.order_id FROM customers c CROSS JOIN orders o;`|

**SET Operators**

|Command|Description|Example|
|:---|:---|:---|
|`UNION`|Combine the result sets of two or more `SELECT` statements, **removing duplicates**|`SELECT name FROM customers UNION SELECT name FROM employees;`|
|`UNION ALL`| Combine the result sets of two or more `SELECT` statements, **including duplicates**|`SELECT name FROM customers UNION ALL SELECT name FROM employees;`|
|`INTERSECT`|Return the common rows from two or more `SELECT` statements|`SELECT name FROM customers INTERSECT SELECT name FROM employees;`|
|`EXCEPT`|Return the rows from the first `SELECT` statement that are not present in the second `SELECT` statement|`SELECT name FROM customers EXCEPT SELECT name FROM employees;`|

**Other Commands**

|Command|Description|Example|
|:---|:---|:---|
|`SUBQUERY`|A query nested inside another query|`SELECT * FROM products WHERE price > (SELECT AVG(price) FROM products);`|
|`CASE`|Perform conditional logic|`SELECT name, CASE WHEN age >= 18 THEN 'Adult' ELSE 'Minor' END AS age_group FROM users;`|
|`COALESCE`|Returns the first non-NULL value from a list of expressions| `SELECT name, COALESCE(nickname, 'No nickname') AS display_name FROM users;`|
|`ISNULL`|Replaces NULL with a specified value (SQL Server specific)|`SELECT price, ISNULL(discount, 0) AS final_discount FROM products;`|
| |Cartesian product is a cross-join which returns all the rows in all the tables listed in a query.|`SELECT c.id, c.nome, c.data_nascimento, c.telefone, p.cargo	FROM clientes AS c, profissoes AS p WHERE c.id_profissao = p.id;`|

**Date functions**

|Command|Description|Example|
|:---|:---|:---|
| `GETDATE()` | Returns the current date and time. | `SELECT GETDATE();` |
| `CURRENT_TIMESTAMP` or `NOW` | Returns the current date and time. | `SELECT CURRENT_TIMESTAMP;` |
| `DATEADD(datepart, number, date)` | Adds a specified number of units to a date. | `SELECT DATEADD(day, 7, '2023-12-25');` |
| `DATEDIFF(datepart, startdate, enddate)` | Returns the difference between two dates. | `SELECT DATEDIFF(day, '2023-12-25', '2024-01-01');` |
| `DATEPART(datepart, date)` | Returns a specific part of a date. | `SELECT DATEPART(month, '2023-12-25');` |
| `HOUR(time)` | Returns the hour from a time/datetime. | `SELECT HOUR('10:30:00');` |
| `MINUTE(time)` | Returns the minute from a time/datetime. | `SELECT MINUTE('10:30:00');` |
| `SECOND(time)` | Returns the second from a time/datetime. | `SELECT SECOND('10:30:00');` |
| `DAY(date)` | Returns the day of the month. | `SELECT DAY('2023-12-25');` |
| `WEEK(date)` | Returns the week number of the year. | `SELECT WEEK('2023-12-25');` |
| `MONTH(date)` | Returns the month of the year. | `SELECT MONTH('2023-12-25');` |
| `QUARTER(date)` | Returns the quarter of the year (1-4). | `SELECT QUARTER('2023-12-25');` |
| `YEAR(date)` | Returns the year. | `SELECT YEAR('2023-12-25');` |
| `WEEKDAY(date)` | Returns the weekday index (0-6, Monday=0). | `SELECT WEEKDAY('2023-12-25');` |
| `CURDATE()` | Returns the current date. | `SELECT CURDATE();` |
| `CURTIME()` | Returns the current time. | `SELECT CURTIME();` |
| `DATE_ADD(date, INTERVAL expr unit)` | Adds a time/date interval to a date. | `SELECT DATE_ADD('2023-12-25', INTERVAL 7 DAY);` |
| `DATE_SUB(date, INTERVAL expr unit)` | Subtracts a time/date interval from a date. | `SELECT DATE_SUB('2023-12-25', INTERVAL 1 MONTH);` |
| `DATE_FORMAT(date, format)` | Formats a date value according to a format string. | `SELECT DATE_FORMAT('2023-12-25', '%Y-%m-%d');` |
| `DAYNAME(date)` | Returns the name of the weekday for a given date. | `SELECT DAYNAME('2023-12-25');` | 
| `DAYOFMONTH(date)` | Returns the day of the month (1-31). | `SELECT DAYOFMONTH('2023-12-25');` |
| `DAYOFWEEK(date)` | Returns the weekday index (1-7, Sunday=1). | `SELECT DAYOFWEEK('2023-12-25');` |
| `DAYOFYEAR(date)` | Returns the day of the year (1-366). | `SELECT DAYOFYEAR('2023-12-25');` |
| `TIME(datetime)` | Extracts the time part of a datetime expression. | `SELECT TIME('2023-12-25 10:30:00');` |
| `SEC_TO_TIME(seconds)` | Converts seconds to a time value. | `SELECT SEC_TO_TIME(3600);` |
| `PERIOD_DIFF(period1, period2)` | Returns the number of months between periods. | `SELECT PERIOD_DIFF(202401, 202312);` |
| `TIME_DIFF(time1, time2)` | Returns the difference between two time values. | `SELECT TIME_DIFF('10:30:00', '09:00:00');` |
| `DATENAME`  | Returns a specific part of a date as text         | `SELECT DATENAME(month, '2024-05-15');` |
| `DATETRUNC` | Truncates a date to a specified precision         | `SELECT DATETRUNC(month, '2024-05-15');` |
| `EOMONTH`   | Returns the last day of the month                 | `SELECT EOMONTH('2024-05-15');` |
| `FORMAT`    | Formats a date value as a string                  | `SELECT FORMAT('2024-05-15', 'MMMM dd, yyyy');` |
| `CONVERT`   | Converts a date to a specific style or data type  | `SELECT CONVERT(VARCHAR, '2024-05-15', 103);` |
| `CAST`      | Casts a date expression to another data type      | `SELECT CAST('2024-05-15' AS DATETIME);` |
| `ISDATE`    | Checks whether a value is a valid date            | `SELECT ISDATE('2024-05-15');` |

**Tips and Tricks:**

  * Use uppercase for SQL keywords and lowercase for table and column names.
  * Use aliases to make your queries more readable.
  * Use comments to explain your code.
  * Use a database management tool to visualize your data and write queries.

**Resources:**

  * **W3Schools SQL Tutorial:** [https://www.w3schools.com/sql/](https://www.google.com/url?sa=E&source=gmail&q=https://www.w3schools.com/sql/)
  * **SQLBolt:** [https://sqlbolt.com/](https://www.google.com/url?sa=E&source=gmail&q=https://sqlbolt.com/)
  * **Khan Academy SQL Course:** [https://www.khanacademy.org/computing/computer-programming/sql](https://www.google.com/url?sa=E&source=gmail&q=https://www.khanacademy.org/computing/computer-programming/sql)
