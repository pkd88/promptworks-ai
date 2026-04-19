Advanced SQL Engineering & Database Architecture Guide
1. Database Normalization (The Rules of Design)
Normalization is the process of organizing data to minimize redundancy (duplicate data) and avoid "Update Anomalies."
First Normal Form (1NF): Atomicity
A table is in 1NF if every column contains only atomic (indivisible) values, and there are no repeating groups.

Rule: No "comma-separated" lists in a single cell.
Rule: Every row must have a unique identifier (Primary Key).
Second Normal Form (2NF): Full Functional Dependency
A table is in 2NF if it is in 1NF and all non-key columns are fully dependent on the Primary Key.

Rule: If you have a composite key (two columns making a PK), every other column must relate to BOTH parts of that key.
Goal: Move partial dependencies to a separate table.
Third Normal Form (3NF): No Transitive Dependency
A table is in 3NF if it is in 2NF and non-key columns do not depend on other non-key columns.

Rule: If Column A depends on Column B, and Column B depends on the PK, Column A should be moved to its own table.
Simplified: "The key, the whole key, and nothing but the key, so help me Codd."
Boyce-Codd Normal Form (BCNF)
A stronger version of 3NF used when a table has multiple overlapping candidate keys. It ensures that for every dependency X -> Y, X must be a superkey.


2. Advanced SQL Query Techniques
A. Common Table Expressions (CTEs)
CTEs create a temporary result set that you can reference within a SELECT, INSERT, UPDATE, or DELETE statement. They make complex queries readable.

WITH RegionalSales AS ( SELECT region, SUM(amount) as total_sales FROM orders GROUP BY region ) SELECT region, total_sales FROM RegionalSales WHERE total_sales > 10000;
B. Recursive CTEs
Used for querying hierarchical data, such as organizational charts or file systems.

WITH RECURSIVE OrgChart AS ( SELECT emp_id, manager_id, name FROM employees WHERE manager_id IS NULL -- The Boss UNION ALL SELECT e.emp_id, e.manager_id, e.name FROM employees e INNER JOIN OrgChart o ON o.emp_id = e.manager_id ) SELECT * FROM OrgChart;
C. Window Functions
Window functions perform calculations across a set of table rows that are related to the current row. Unlike aggregate functions, they do not group the rows into a single output row.

OVER / PARTITION BY: Divides the data into "windows."
RANK() / DENSE_RANK(): Assigns a number to each row based on a value.
ROW_NUMBER(): Gives a unique number to every row in the partition.

SELECT employee_name, department, salary, AVG(salary) OVER(PARTITION BY department) as dept_avg_salary, salary - AVG(salary) OVER(PARTITION BY department) as diff_from_avg FROM employees;


3. Performance Tuning and Indexing
A. B-Tree Indexes
The default index type. It works like a library card catalog, allowing the database to find a specific row without reading the entire table (Full Table Scan).

CREATE INDEX idx_order_date ON orders(order_date);
B. Composite Indexes
An index on multiple columns. The order of columns matters (Leading Column). An index on (LastName, FirstName) is useless for a search on just FirstName.
C. Execution Plans (EXPLAIN)
Professionals use the EXPLAIN command to see how the database engine intends to run a query.

Index Scan: Good (Uses the index).
Seq Scan (Sequential Scan): Bad for large tables (Reads every row).

EXPLAIN ANALYZE SELECT * FROM users WHERE email = 'phil@example.com';


4. Advanced Constraints and Triggers
A. Check Constraints
Ensures that data entered into a column meets a specific requirement. ALTER TABLE Employees ADD CONSTRAINT check_salary CHECK (salary > 0);
B. Database Triggers
Automated scripts that run when a specific event (Insert, Update, Delete) occurs.

Example: Automatically updating a "last_modified" timestamp whenever a row is changed.

CREATE TRIGGER update_timestamp BEFORE UPDATE ON users FOR EACH ROW EXECUTE PROCEDURE refresh_timestamp_func();


5. ACID Properties (The Gold Standard of Transactions)
To ensure data integrity, every transaction must follow ACID rules:

Atomicity: The whole transaction succeeds or the whole thing is rolled back. No "half-finished" saves.
Consistency: The database moves from one valid state to another.
Isolation: Transactions happening at the same time do not interfere with each other.
Durability: Once a transaction is committed, it stays saved even if the power goes out.
