## SQL

**Basic Commands:**

| Command | Description | Example |
|---|---|---|
| `SELECT` | Retrieve data from a table | `SELECT * FROM customers;` |
| `FROM` | Specify the table to retrieve data from | `SELECT name, age FROM employees;` |
| `WHERE` | Filter data based on a condition | `SELECT * FROM products WHERE price > 100;` |
| `ORDER BY` | Sort data by one or more columns | `SELECT * FROM orders ORDER BY order_date DESC;` |
| `LIMIT` | Limit the number of rows returned | `SELECT * FROM users LIMIT 10;` |
| `INSERT INTO` | Insert data into a table | `INSERT INTO customers (name, email) VALUES ('John Doe', 'john.doe@example.com');` |
| `UPDATE` | Update data in a table | `UPDATE products SET price = 120 WHERE id = 1;` |
| `DELETE` | Delete data from a table | `DELETE FROM orders WHERE order_date < '2023-01-01';` |

**Intermediate Commands:**

| Command | Description | Example |
|---|---|---|
| `DISTINCT` | Retrieve unique values | `SELECT DISTINCT city FROM customers;` |
| `COUNT` | Count the number of rows | `SELECT COUNT(*) FROM orders;` |
| `SUM` | Calculate the sum of a column | `SELECT SUM(price) FROM products;` |
| `AVG` | Calculate the average of a column | `SELECT AVG(age) FROM employees;` |
| `MAX` | Find the maximum value in a column | `SELECT MAX(salary) FROM employees;` |
| `MIN` | Find the minimum value in a column | `SELECT MIN(price) FROM products;` |
| `GROUP BY` | Group rows based on a column | `SELECT city, COUNT(*) FROM customers GROUP BY city;` |
| `HAVING` | Filter grouped data | `SELECT city, COUNT(*) FROM customers GROUP BY city HAVING COUNT(*) > 10;` |
| `JOIN` | Combine data from multiple tables | `SELECT o.order_id, c.name FROM orders o JOIN customers c ON o.customer_id = c.customer_id;` |
| `LEFT JOIN` | Return all rows from the left table, even if there is no match in the right table | `SELECT c.name, o.order_id FROM customers c LEFT JOIN orders o ON c.customer_id = o.customer_id;` |
| `RIGHT JOIN` | Return all rows from the right table, even if there is no match in the left table | `SELECT c.name, o.order_id FROM customers c RIGHT JOIN orders o ON c.customer_id = o.customer_id;` |

**Advanced Commands:**

| Command | Description | Example |
|---|---|---|
| `UNION` | Combine the result sets of two or more `SELECT` statements | `SELECT name FROM customers UNION SELECT name FROM employees;` |
| `INTERSECT` | Return the common rows from two or more `SELECT` statements | `SELECT name FROM customers INTERSECT SELECT name FROM employees;` |
| `EXCEPT` | Return the rows from the first `SELECT` statement that are not present in the second `SELECT` statement | `SELECT name FROM customers EXCEPT SELECT name FROM employees;` |
| `SUBQUERY` | A query nested inside another query | `SELECT * FROM products WHERE price > (SELECT AVG(price) FROM products);` |
| `CASE` | Perform conditional logic | `SELECT name, CASE WHEN age >= 18 THEN 'Adult' ELSE 'Minor' END AS age_group FROM users;` |
| `CREATE TABLE` | Create a new table | `CREATE TABLE products (id INT PRIMARY KEY, name VARCHAR(255), price DECIMAL(10,2));` |
| `ALTER TABLE` | Modify an existing table | `ALTER TABLE customers ADD COLUMN phone VARCHAR(20);` |
| `DROP TABLE` | Delete a table | `DROP TABLE products;` |
| `CREATE INDEX` | Create an index on a table | `CREATE INDEX idx_customer_name ON customers (name);` |
| `TRANSACTION` | Group multiple statements into a single unit of work | `BEGIN TRANSACTION; UPDATE accounts SET balance = balance - 100 WHERE id = 1; UPDATE accounts SET balance = balance + 100 WHERE id = 2; COMMIT;` |

**Tips and Tricks:**

* Use uppercase for SQL keywords and lowercase for table and column names.
* Use aliases to make your queries more readable.
* Use comments to explain your code.
* Use a database management tool to visualize your data and write queries.

**Resources:**

* **W3Schools SQL Tutorial:** https://www.w3schools.com/sql/
* **SQLBolt:** https://sqlbolt.com/
* **Khan Academy SQL Course:** https://www.khanacademy.org/computing/computer-programming/sql