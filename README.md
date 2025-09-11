<details>


   
   <summary><b> SQL INTRODUCTIONS </b></summary>
   
# <SUB>1. SQL: Structured Query Language, used to access and manipulate data.</SUB>
# <SUB>2. SQL used CRUD operations to communicate with DB.</SUB>
</br>1. CREATE - execute INSERT statements to insert new tuple into the relation.
</br>2. READ - Read data already in the relations.
</br>3. UPDATE - Modify already inserted data in the relation.
</br>4. DELETE - Delete specific data point/tuple/row or multiple rows.
# <sub>3. SQL is not DB, is a query language.</sub>
# <SUB>4. What is RDBMS? (Relational Database Management System)</SUB>
</br>1. Software that enable us to implement designed relational model.
</br>2. e.g., MySQL, MS SQL, Oracle, IBM etc.
</br>3. Table/Relation is the simplest form of data storage object in R-DB.
</br>4. MySQL is open-source RDBMS, and it uses SQL for all CRUD operations
# <sub>5. MySQL used client-server model, where client is CLI or frontend that used services provided by MySQL server.</sub>
# <sub>6. Difference between SQL and MySQL</sub>
</br>SQL is Structured Query language used to perform CRUD operations in R-DB, while MySQL is a RDBMS used to
store, manage and administrate DB (provided by itself) using SQL.
</details>

--------------------------------------------------------------------------------------------------------------------------------------
<details>




   
<summary><b> SQL DATATYPE </b></summary>

# <SUB>7. SQL DATA TYPES
## 🔹 String Data Types
- </br> **CHAR(n)** Fixed-length string (0–255), e.g., CHAR(251)
- </br> **VARCHAR(n)** Variable-length string (0–65535 depending on row size), e.g., VARCHAR(255)
- </br> **TINYTEXT** String up to 255 characters
- </br> **TEXT** String up to 65,535 characters (64 KB)
- </br> **MEDIUMTEXT** String up to 16,777,215 characters (16 MB)
- </br> **LONGTEXT** String up to 4,294,967,295 characters (4 GB)
- </br> **TINYBLOB** Binary string up to 255 bytes
- </br> **BLOB** Binary string up to 65,535 bytes (64 KB)
- </br> **MEDIUMBLOB** Binary string up to 16 MB
- </br> **LONGBLOB** Binary string up to 4 GB
- </br> **ENUM** One value from a preset list, e.g., ENUM('M','F','Other')
- </br> **SET** One or many values from a preset list, e.g., SET('a','b','c')
## 🔹 Numeric Data Types
- </br> **TINYINT** Integer (-128 to 127)
- </br> **SMALLINT** Integer (-32,768 to 32,767)
- </br> **MEDIUMINT** Integer (-8,388,608 to 8,388,607)
- </br> **INT** Integer (-2,147,483,648 to 2,147,483,647)
- </br> **BIGINT** Integer (-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807)
- </br> **FLOAT** Approx. decimal with precision up to 23 digits
- </br> **DOUBLE** Approx. decimal with precision 24 to 53 digits
- </br> **DECIMAL** Exact fixed-point decimal (stored as string internally)
## 🔹 Date & Time Data Types
- </br> **DATE** Format: `YYYY-MM-DD`
- </br> **DATETIME** Format: `YYYY-MM-DD HH:MM:SS`
- </br> **TIMESTAMP** Format: `YYYYMMDDHHMMSS`
- </br> **TIME** Format: `HH:MM:SS`
## 🔹 Boolean Data Type
- </br> **BOOLEAN** True/False (stored as 0 = False, 1 = True)

# <SUB>8. Size: TINY < SMALL < MEDIUM < INT < BIGINT.</SUB>
# <sub>9. Variable length Data types e.g., VARCHAR, are better to use as they occupy space equal to the actual data Size.</sub>
# <sub>10. Values can also be unsigned e.g., INT UNSIGNED. </sub>

</details>


--------------------------------------------------------------------------------------------------------------------------------------


<details>




   
<summary> <b>TYPES OF SQL commands:</b></summary>
<details>
   <summary> <b>DDL</b></summary>
   
</br>**DDL (data definition language): defining relation schema.**
</br>1. **CREATE**: create table, DB, view.
</br>2 .**ALTER TABLE**: modification in table structure. e.g, change column datatype or add/remove columns.
</br>3. **DROP**: delete table, DB, view.
</br>4. **TRUNCATE**: remove all the tuples from the table.
</br>5. **RENAME**: rename DB name, table name, column name etc
# <sub>12. How to create a database?</SUB>
</br> **CREATE DATABASE** database_name;
</br> **Example** - CREATE DATABASE ORG; { HERE ORG IS A DATABASES NAME. }
# <sub>13. How to show all existing databases? </sub>
</br> **SHOW DATABASES;**
# <sub>14. How to use/select a database? </sub>
</br> **USE** database_name;  
</br> **Example** – USE ORG;
# <sub>15. How to create a table inside a database? </sub>
</br> **CREATE TABLE** table_name (  
column1 datatype,  
column2 datatype,  
column3 datatype,    
);  
</br> **Example** – CREATE TABLE STUDENT (ID INT, NAME VARCHAR(100), AGE INT)
# <sub>16. How to show all tables in the selected database? </sub>
</br> **SHOW TABLES;**
# <sub>17. How to describe the structure of a table? </sub>
</br> **DESCRIBE** table_name;  
</br> **Example** – DESCRIBE STUDENT;
# <sub>18. How to drop (delete) a database? </sub>
</br> **DROP DATABASE** database_name;  
</br> **Example** – DROP DATABASE ORG;
# <sub>19. How to drop (delete) a table? </sub>
</br> **DROP TABLE** table_name;  
</br> **Example** – DROP TABLE STUDENT;
# <sub>20. What is the SQL `ALTER TABLE` statement used for? </sub>
</br> **ALTER TABLE** is used to add, delete, or modify columns in an existing table. It can also add or drop constraints.
# <sub>21. How to add a column to a table? </sub>
</br> **ALTER TABLE** table_name **ADD** column_name datatype;  
</br> **Example** – CREATE TABLE Customers ADD Email VARCHAR(255); { Adds “Email” column to Customers table }
# <sub>22. How to drop (delete) a column from a table? </sub>
</br> **ALTER TABLE** table_name **DROP COLUMN** column_name;  
</br> **Example** – ALTER TABLE Customers DROP COLUMN Email; { Deletes “Email” column }
# <sub>23. How to modify a column's data type? </sub> 
</br> **ALTER TABLE** table_name **MODIFY COLUMN** column_name datatype;  
</br> **Example** – ALTER TABLE Persons MODIFY COLUMN DateOfBirth YEAR; { Changes column type to YEAR }
# <sub>24. How to rename a column? </sub> 
</br> **ALTER TABLE** table_name **RENAME COLUMN** old_name **TO** new_name;  
</br> **Example** – ALTER TABLE Persons RENAME COLUMN Address TO City; { Renames column Address → City }
# <sub>25. How to rename a table? </sub>
</br> **ALTER TABLE** old_table_name **RENAME TO** new_table_name;  
</br> **Example** – ALTER TABLE Customers RENAME TO Clients; { Renames table Customers → Clients }
# <sub>26. How to rename a database? </sub> 
</br> MySQL does **not** support `RENAME DATABASE` directly.  
</br> Instead, you must **create a new database**, then **move (or import/export) the tables** into it.
1. **CREATE DATABASE** new_database;  
2. **RENAME TABLE** old_database.table_name **TO** new_database.table_name;  
   (Repeat for each table)  
3. **DROP DATABASE** old_database; (after confirming data is moved)
Example:  
</br> **CREATE** DATABASE new_org;  
</br> **RENAME TABLE** org.students *TO** new_org.students;  
</br> **DROP DATABASE** org;
# <sub>27. How to add a column after a specific column? </sub>

</br> In MySQL, you can use the ALTER TABLE ... ADD COLUMN ... AFTER ... syntax to place the new column at a specific location.
</br> If you don’t specify AFTER, the new column will be added at the end of the table.
```
ALTER TABLE table_name
ADD COLUMN new_column_name datatype AFTER existing_column_name;

Example: Suppose you have an Employees table with columns:
EmployeeID, FirstName, LastName, BirthDate, Photo, Notes
To add a Gender column after BirthDate:
ALTER TABLE Employees
ADD COLUMN Gender TEXT AFTER BirthDate
```




# <sub>27. What is the SQL `TRUNCATE` statement used for? </sub>
</br> **TRUNCATE TABLE** is used to delete all rows from a table, but it keeps the table structure for future use.
# <sub>28. How to truncate a table? </sub>
</br> **TRUNCATE TABLE** table_name;  
</br> **Example** – TRUNCATE TABLE Students; { Removes all records from Students table, but keeps the table }
# <sub>29. What is the difference between `TRUNCATE` and `DELETE`? </sub>
</br> **DELETE** – removes rows one by one and can use a **WHERE** condition.  
</br> **TRUNCATE** – removes all rows instantly, does not support **WHERE**, and resets AUTO_INCREMENT counters (in MySQL).
**Example:**  
</br> DELETE FROM Students **WHERE** Age > 20; { Deletes only matching rows }  
</br> **TRUNCATE TABLE** Students; { Deletes all rows }
# <sub>30. What is DRL / DQL (Data Retrieval / Data Query Language)? </sub>
</br> DRL / DQL is used to retrieve data from the database.  
</br> The main keyword is **SELECT**.
# <sub>31. How to select all columns from a table? </sub>
</br> **SELECT * FROM** table_name;  
</br> **Example** – SELECT * FROM Students; { Fetches all columns and all rows from Students }
# <sub>32. How to select specific columns from a table? </sub>
</br> **SELECT** column1, column2 **FROM** table_name;  
</br> **Example** – SELECT Name, Age FROM Students; { Fetches only Name and Age columns }
# <sub>33. What is the order of execution in SELECT? </sub>
</br> The order of execution is **from RIGHT to LEFT**.  
</br> First, the **FROM** clause is executed, then the **SELECT** clause.
# <sub>34. Can we use SELECT keyword without using FROM clause? </sub>
</br> ✅ Yes, using **DUAL tables**.
# <sub> What are DUAL tables? </sub>
</br> DUAL tables are **dummy tables** created by MySQL (and Oracle).  
</br> They help users to perform calculations or functions without referring to user-defined tables.
# <sub>35. Example of SELECT without FROM (using DUAL) </sub>
</br> SELECT 55 + 11; { Returns 66 }  
</br> SELECT NOW(); { Returns current date & time }  
</br> SELECT UCASE('hello'); { Returns HELLO }
</details>

------------------------------------------------------------------------------------------------------------------------------------------


<details>
   <summary> <b>DML</b></summary>

   # <sub> What is DML in SQL? </sub>
</br> **DML (Data Manipulation Language)** is used to **manipulate data** in existing tables.  
</br> It includes **INSERT, UPDATE, DELETE, REPLACE** statements.
# <sub> How to insert data into a table? </sub>
```
sql
INSERT INTO table_name (col1, col2, col3)
VALUES (v1, v2, v3), (val1, val2, val3);
</br> ✅ You can insert single or multiple rows in one statement.
```
# <sub> What is the purpose of the SQL UPDATE statement? </sub>
</br> The **UPDATE** statement is used to **modify existing data** in a table.
# <sub> How do you update a single column value in a table? </sub>
</br> Use the **SET** keyword with a **WHERE clause** to update a specific row:

```
sql
UPDATE table_name
SET column_name = value
WHERE condition;
```
# <sub> How do you update multiple columns in a single query? </sub>
 ✅ Multiple columns can be updated at once using commas:
```
UPDATE table_name
SET col1 = value1, col2 = value2
WHERE condition;
```
# <sub> What is ON DELETE CASCADE and ON UPDATE CASCADE? </sub>
</br> - ON DELETE CASCADE: If a referenced row is deleted in the parent table, all corresponding rows in the child table are also deleted.
</br> - ON UPDATE CASCADE: If a referenced primary key is updated in the parent table, the foreign key values in the child table are automatically updated.
```
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
    ON DELETE CASCADE
    ON UPDATE CASCADE
);
IF YOU ARE NOT WRITE ON DELETE CASCADE OR ON UPDATE CASCADE YOU CANNOT UPDATE OR DELETE DATA FROM PARENT TABLE
```
# <sub> What is ON DELETE SET NULL? </sub>
</br> - **ON DELETE SET NULL:** If a referenced row is deleted in the parent table,
</br>the foreign key value in the child table is automatically set to **NULL** instead of being deleted.
```
sql
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
    ON DELETE SET NULL
);
```
</br>IF YOU ARE NOT WRITE **ON DELETE SET NULL**,
</br> YOU CANNOT **DELETE DATA** FROM THE PARENT TABLE IF CHILD
</br>ROWS EXIST, BECAUSE IT WILL BREAK THE **FOREIGN KEY CONSTRAINT**.
# <sub> What is REPLACE in SQL? </sub>

</br>**Primarily used for already present tuples (rows) in a table.**  
</br>Works like an **UPDATE** if the row with the same **PRIMARY KEY** or **UNIQUE KEY** already exists
</br>the old row will be deleted and replaced with the new one.  
</br> - Works like an **INSERT** if there is no duplicate data — a new row will be inserted.  
**Syntax Examples:**
```
sql
-- Insert or replace a row into student table
REPLACE INTO student (id, class) VALUES (4, 3);

-- Alternative syntax using SET
REPLACE INTO student 
SET id = 4, class = 3;
```
# <sub>Difference Between UPDATE and DELETE in SQL? </sub>
### 1.Basic Definition
- **UPDATE** → Modifies existing records in a table.  
- **DELETE** → Removes existing records from a table.  

### 2. Effect on Data
- **UPDATE** → Changes values of one or more columns for selected rows, but the rows remain in the table.  
- **DELETE** → Removes the entire row(s) from the table.  
### 3. Syntax
```
sql
-- UPDATE Example
UPDATE employees
SET salary = 50000
WHERE emp_id = 101;

-- DELETE Example
DELETE FROM employees
WHERE emp_id = 101;
```










   </details>

   
-----------------------------------------------------------------------------------------------------------------------------------------




   
   <details>
   <summary> <b>DCL</b></summary>

   </details>



------------------------------------------------------------------------------------------------------------------------------------------


   
   <details>
   <summary> <b>TCL</b></summary>

   </details>
 </details>


--------------------------------------------------------------------------------------------------------------------------------------



 
 <details>
    
   <summary><b> SQL CLAUSE & OPERATORS: </b></summary>
   
<details>
<summary><b>SQL CLAUSE</b></summary>
   
# <sub>36. What is the SQL WHERE clause? </sub>
</br> The **WHERE** clause is used to **filter records**.  
</br> It extracts only those records that fulfill a specified condition.
# <sub>37. Syntax of WHERE clause </sub>
</br> **SELECT** column1, column2, ...  
**FROM** table_name  
**WHERE** condition;
```
Example 1 :
Select from customer where country="mexico";
Example 2:
Select from customer where CustomerID = 1;
Example 3 :
Select from customers where CustomerID > 80;
 
```
# <sub>38. Can the WHERE clause be used only in SELECT? </sub>
</br> ❌ No.  
</br> The WHERE clause can also be used in **UPDATE, DELETE,** and other SQL statements.
# <sub>39. What is the SQL BETWEEN operator? </sub>  
</br> The **BETWEEN** operator is used to filter the result set within a certain **range of values**.  
</br> The values can be numbers, text, or dates.  
# <sub>40. Syntax of BETWEEN </sub>  
</br> **SELECT** column1, column2, ...  
**FROM** table_name  
**WHERE** column_name **BETWEEN** value1 **AND** value2;  
# <sub>41. How to select students with Marks between 70 and 90? </sub>  
</br> **SELECT** *  
**FROM** Students  
**WHERE** Marks BETWEEN 70 AND 90;  
# <sub>42. How to select employees with Salary between 30,000 and 50,000? </sub>  
</br> **SELECT** *  
**FROM** Employees  
**WHERE** Salary BETWEEN 30000 AND 50000;  
# <sub>43. How to select customers whose Age is between 25 and 35? </sub>  
</br> **SELECT** *  
**FROM** Customers  
**WHERE** Age BETWEEN 25 AND 35;  
# <sub>44. How to select products where Price is NOT between 500 and 1000? </sub>  
</br> **SELECT** *  
**FROM** Products  
**WHERE** Price NOT BETWEEN 500 AND 1000;  
# <sub>45. How to select orders placed between '2025-01-01' and '2025-06-30'? </sub>  
</br> **SELECT** *  
**FROM** Orders  
**WHERE** OrderDate BETWEEN '2025-01-01' AND '2025-06-30';  
# <sub>46. Can BETWEEN be used with text values? </sub>  
</br> ✅ Yes. For example:  
```sql
SELECT *  
FROM Customers  
WHERE CustomerName BETWEEN 'A' AND 'M';
```
# <sub> What is the SQL ORDER BY keyword? </sub>
</br> The **ORDER BY** keyword is used to **sort the result-set** in ascending or descending order.
# <sub> What is the default sorting order in ORDER BY? </sub>
</br> By default, **ORDER BY** sorts records in **ascending order (ASC)**.
```sql
SELECT * FROM Products ORDER BY Price;
```
# <sub> How do you sort records in descending order? </sub>
</br> Use the DESC keyword to sort records from highest to lowest or Z to A:
```
SELECT * FROM Products ORDER BY Price DESC;
SELECT * FROM Products ORDER BY ProductName DESC;
```
# <sub> How do you sort records by multiple columns? </sub>
</br> List multiple columns separated by commas. Records are sorted by the first column, then by the next if there are duplicates:
```
SELECT * FROM Customers ORDER BY Country, CustomerName;
```
# <sub> How do you use both ASC and DESC in one query? </sub>
</br> Specify the order for each column individually:
```
SELECT * FROM Customers ORDER BY Country ASC, CustomerName DESC;
```
# <sub> What is the SQL SELECT DISTINCT statement? </sub>
</br> The **SELECT DISTINCT** statement is used to return **only distinct (different) values** from a column.
# <sub> Why do we use SELECT DISTINCT? </sub>
</br> To avoid duplicate values in the result set and **list only unique entries**.
# <sub> Syntax of SELECT DISTINCT</sub>
```
sql
SELECT DISTINCT column1, column2, ...
FROM table_name;

```
# <sub> Can SELECT DISTINCT be used on multiple columns?</sub>

</br> ✅ Yes. It considers the combination of values across the listed columns as unique.
```
SELECT DISTINCT Country, City FROM Customers;
```
</br> Returns unique combinations of Country and City.

# <sub> What is the SQL GROUP BY statement? </sub>
</br> The **GROUP BY** statement groups rows that have the same values into **summary rows**.  
</br> Often used with aggregate functions like **COUNT(), SUM(), AVG(), MIN(), MAX()**.
# <sub> Syntax of GROUP BY</sub>
```
sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```
# <sub> What is the SQL HAVING clause? </sub>
</br> The **HAVING** clause is used to **filter groups** created by the **GROUP BY** statement.  
</br> It is used because the **WHERE** clause **cannot filter aggregate results**.
# <sub> Syntax of HAVING clause</sub>
```
sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

# <sub> Example: Filter groups using HAVING</sub>
```
SELECT Country, COUNT(CustomerID) AS NumberOfCustomers
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5;
```   
</br> This returns countries with more than 5 customers.
# <sub> Can multiple conditions be used in HAVING?</sub>
</br> ✅ Yes, multiple conditions can be combined using AND/OR:
```
SELECT Country, COUNT(CustomerID) AS NumberOfCustomers
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5 AND COUNT(CustomerID) < 20;
```
</details>

--------------------------------------------------------------------------------------------------------------------------------------


<details>
<summary><b>SQL OPERATOR</b></summary>


# <sub>47. What is the SQL IN operator? </sub>  
</br> The **IN** operator allows you to specify multiple values in a **WHERE** clause.  
</br> It is a shorthand for writing multiple **OR** conditions.  
# <sub>48. What is the syntax of IN? </sub>  
</br> **SELECT** column_name(s)  
**FROM** table_name  
**WHERE** column_name **IN** (value1, value2, ...);  
# <sub>49. How to return all customers from 'Germany', 'France', or 'UK'? </sub>
```
</br> **SELECT** *  
**FROM** Customers  
**WHERE** Country IN ('Germany', 'France', 'UK');
```
# <sub>50. How to return all customers that are NOT from 'Germany', 'France', or 'UK'? </sub>  
```
</br> **SELECT** *  
**FROM** Customers  
**WHERE** Country NOT IN ('Germany', 'France', 'UK');  
```
# <sub>51. What is the SQL AND operator? </sub>
</br> The **AND** operator is used to filter records only when **all conditions** are true.  
</br> **Syntax:**  
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2;
```
</br> **Example:**
```
SELECT * 
FROM Customers
WHERE Country = 'Germany' AND City = 'Berlin';
```
# <sub>52. What is the SQL OR operator? </sub>
</br> The OR operator is used to filter records when at least one condition is true.
</br> **Syntax:**
```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2;
```
</br> **Example:**
```
SELECT * 
FROM Customers
WHERE Country = 'Germany' OR Country = 'France';
```
# <sub>53. What is the SQL NOT operator? </sub>
</br> The NOT operator is used to display records when the condition is not true.
</br> **Syntax:**
```
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```
</br> **Example:**
```
SELECT * 
FROM Customers
WHERE Country NOT IN ('Germany', 'France', 'UK');
```
# <sub>54. What is the SQL IS NULL operator? </sub>
</br> The IS NULL operator is used to test for empty (NULL) values in a column.
</br> **Syntax:**
```
SELECT column1, column2, ...
FROM table_name
WHERE column_name IS NULL;
```
</br> **Example:**
```
SELECT * 
FROM Customers
WHERE Address IS NULL;

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------



<details>
<summary><b>SQL WILDCARDS</b></summary>
   
# <sub>55. What are SQL Wildcards? </sub>
</br> SQL Wildcards are special symbols used with the **LIKE** operator to search for specific patterns in a column.  
</br>They allow you to substitute one or more characters in string matching.  
# <sub>56. Why are SQL Wildcards used? </sub>
</br> Wildcards are used in the **WHERE** clause to perform flexible searches when you don’t know the exact value.  
</br>They help find partial matches instead of exact matches.  
# <sub>57. What does the % wildcard represent? </sub>
</br> The **%** wildcard matches **zero or more characters**.  
**Examples:**  
```sql
-- Names ending with 'es'
SELECT * FROM Customers WHERE CustomerName LIKE '%es';

-- Names containing 'mer'
SELECT * FROM Customers WHERE CustomerName LIKE '%mer%';
```
# <sub>57. What does the _ wildcard represent? </sub>
</br> The _ wildcard matches exactly one character.
```
-- Any city ending with 'ondon'
SELECT * FROM Customers WHERE City LIKE '_ondon';
-- City starting with 'L' and ending with 'on'
SELECT * FROM Customers WHERE City LIKE 'L___on';
```
# <sub>58. How is the [] wildcard used in SQL? </sub>
</br> The [] wildcard matches any one character from inside the brackets.
**Example:**
```
-- Names starting with b, s, or p
SELECT * FROM Customers WHERE CustomerName LIKE '[bsp]%';
```
# <sub> 57. What does the - wildcard do? </sub>
</br> The - wildcard specifies a range of characters inside brackets.
**Example:**
```
-- Names starting with a–f
SELECT * FROM Customers WHERE CustomerName LIKE '[a-f]%';
```
# <sub>59. Can SQL wildcards be combined? </sub>
</br> ✅ Yes. Wildcards can be combined for more complex patterns.
**Examples:**
```
-- Names starting with 'a' and at least 3 characters long
SELECT * FROM Customers WHERE CustomerName LIKE 'a__%';

-- Names having 'r' in the second position
SELECT * FROM Customers WHERE CustomerName LIKE '_r%';
```
# <sub>60. What happens if no wildcard is used with LIKE? </sub>
</br> Without wildcards, the LIKE operator behaves like the = operator (exact match).
```
***Example:**

SELECT * FROM Customers WHERE Country LIKE 'Spain';
```
# <sub>61. Are all wildcards supported in every SQL database? </sub>
</br> ❌ No. Some wildcards are not supported in MySQL and PostgreSQL.
```
% and _ → Supported everywhere

[], -, ^ → Not supported in MySQL/PostgreSQL

{} → Only supported in Oracle
```


</details>

--------------------------------------------------------------------------------------------------------------------------------------


<details>
<summary><b>SQL ALISE</b></summary>
   
# <sub>62. What is a SQL Alias? </sub>
</br> A SQL Alias is a **temporary name** given to a table or column to make it more readable.  
</br> It exists only for the duration of the query.

# <sub>63. How do you create a column alias in MySQL? </sub>
</br> Use the **AS** keyword (optional in MySQL):  
```sql
SELECT CustomerID AS ID FROM Customers;
-- Or without AS
SELECT CustomerID ID FROM Customers;
```
# <sub>64. How do you give an alias with spaces in MySQL? </sub>
</br> Surround the alias with **backticks (`)** in MySQL:
```
SELECT ProductName AS `My Great Products` FROM Products;
```
# <sub> Why are table aliases useful? </sub>
</br> Table aliases are useful when:
</br>Using more than one table in a query,
</br>Making long column or table names shorter,
</br>Improving query readability,
```
Example:

SELECT o.OrderID, o.OrderDate, c.CustomerName
FROM Customers AS c, Orders AS o
WHERE c.CustomerName='Around the Horn' AND c.CustomerID=o.CustomerID;
```

</details>
</details>



---------------------------------------------------------------------------------------------------



<details>
   
   <summary> <b>SQL KEY </b></summary> 

<details>
   
   <summary> <b>PRIMARY KEY </b></summary> 
   
   # <sub> What is a PRIMARY KEY in SQL? </sub>
</br> A **PRIMARY KEY** is a column (or a set of columns) that **uniquely identifies each row** in a table.  
</br> Each table can have **only one primary key.**
# <sub> Can a PRIMARY KEY column accept NULL values? </sub>
</br> ❌ No. A **PRIMARY KEY column cannot contain NULL** values because it must uniquely identify every row.
# <sub> Can a table have more than one PRIMARY KEY? </sub>
</br> ❌ No. A table can have **only one PRIMARY KEY**, but it can consist of **multiple columns (composite primary key).**
# <sub> What is a composite PRIMARY KEY? </sub>
</br> A **composite primary key** is a primary key made up of **two or more columns** that together uniquely identify a row.

```sql
CREATE TABLE Orders (
    OrderID INT,
    ProductID INT,
    Quantity INT,
    PRIMARY KEY (OrderID, ProductID)
);
```

# <sub> Can PRIMARY KEY be added after table creation? </sub>
</br> ✅ Yes, using ALTER TABLE:
```
ALTER TABLE Students
ADD PRIMARY KEY (StudentID);
```
# <sub> Can a PRIMARY KEY be dropped? </sub>
</br> ✅ Yes, using ALTER TABLE:
```
ALTER TABLE Students
DROP PRIMARY KEY;
 ```
# <sub> Why is PRIMARY KEY important? </sub>
</br> - Ensures data integrity by uniquely identifying each row
</br> - Used to create relationships between tables with foreign keys
</br> - Helps in indexing and faster query performance



</details>

--------------------------------------------------------------------------------------------------------------------------------------

<details>
   
   <summary> <b>FOREGIN KEY </b></summary> 
   
  # <sub> What is a FOREIGN KEY in SQL? </sub>
</br> A **FOREIGN KEY** is a column (or set of columns) in one table that **references the PRIMARY KEY of another table**.  
</br> It is used to maintain **referential integrity** between two tables.
# <sub> Can a table have multiple FOREIGN KEYS? </sub>
</br> ✅ Yes. A table can have **multiple foreign keys**, each referencing different tables.
# <sub> Can a FOREIGN KEY accept NULL values? </sub>
</br> ✅ Yes. A FOREIGN KEY column can contain **NULL** unless specified otherwise.
# <sub> How to create a FOREIGN KEY while creating a table? </sub>
```
sql
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    OrderDate DATE,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
);
  ```
# <sub> How to add a FOREIGN KEY to an existing table? </sub>
```
ALTER TABLE Orders
ADD CONSTRAINT FK_Customer
FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID);
```
# <sub> How to delete a FOREIGN KEY? </sub>
```
ALTER TABLE Orders
DROP FOREIGN KEY FK_Customer;
```
# <sub> What is ON DELETE CASCADE and ON UPDATE CASCADE? </sub>
</br> - ON **DELETE CASCADE:** If a referenced row is deleted in the parent table, all corresponding rows in the child table are also deleted.
</br> - ON **UPDATE CASCADE:** If a referenced primary key is updated in the parent table, the foreign key values in the child table are automatically updated.
```
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
    ON DELETE CASCADE
    ON UPDATE CASCADE
);
```
</details>
</details>

--------------------------------------------------------------------------------------------------------------------------------------
<details>
   
   <summary> <b>SQL JOIN </b></summary> 
   
   # <sub>MySQL Joining Tables</sub>

</br>A **JOIN** clause is used to combine rows from two or more tables, based on a related column between them.  
</br>It helps in retrieving meaningful data from multiple tables by establishing relationships us
# <sub>Types of JOINs in MySQL</sub>
</br>**1.INNER JOIN.**
</br>**2.LEFT JOIN.**
</br>**3.RIGHT JOIN.**
</br>**4.FULL JOIN.**
</br>**5.CROSS JOIN.**
</br>**6.SELF JOIN.**

<details>
   
   <summary> <b>INNER JOIN </b></summary> 
   
   # <sub>1. What is INNER JOIN in MySQL?</sub>  
   </br>In MySQL, INNER JOIN returns rows that have matching values in both tables.
   </br>If there is no match, that row will not be included in the result set.
   # <sub>2. What is the syntax of INNER JOIN?</sub>  
```
sql
-- INNER JOIN between two tables
SELECT column_list
FROM table1
INNER JOIN table2
ON table1.common_column = table2.common_column;

-- INNER JOIN with three tables
SELECT column_list
FROM table1
INNER JOIN table2 ON table1.col = table2.col
INNER JOIN table3 ON table2.col = table3.col;
```
   </details>
   <details>
   
   <summary> <b>OUTER  JOIN </b></summary> 

   # <sub>1. What is an OUTER JOIN in MySQL?</sub> 
   </br>OUTER JOIN is used to return all records from one table and the matched records from another table.
   </br>If no match is found, NULL values are returned for the missing side.
   </br> **THREE** types of OUTER JOINS : -
   </br>**1.LEFT JOIN.**
   </br>**2.RIGHT JOIN.**
   </br>**3.FULL JOIN.**
    <details>
   
   <summary> <b> LEFT JOIN </b></summary> 

   # <sub>3. What is LEFT JOIN in MySQL?</sub>  
   </br>LEFT JOIN returns all rows from the left table, and the matched rows from the right table.
   </br>If there is no match, NULL is returned from the right side.
   
    **Example:**  
      ```
      sql
      SELECT employees.emp_id, employees.name, departments.dept_name
      FROM employees
      LEFT JOIN departments
      ON employees.dept_id = departments.dept_id;
      ```
   </details>
   
   <details>
   
   <summary> <b> RIGHT JOIN </b></summary> 

   # <sub>What is RIGHT JOIN in MySQL?</sub>
   </br>RIGHT JOIN returns all rows from the right table, and the matched rows from the left table.  
   </br>If there is no match, NULL is returned from the left side.
   ```
SELECT employees.emp_id, employees.name, departments.dept_name
   FROM employees
   RIGHT JOIN departments
   ON employees.dept_id = departments.dept_id;
   ```

   </details>

   <details>
   
   <summary> <b> FULL JOIN </b></summary> 
   
   # <sub>What is FULL JOIN in MySQL?</sub>
   </br>MySQL does not support FULL OUTER JOIN directly.  
   </br>It can be simulated using a combination of LEFT JOIN and RIGHT JOIN with UNION.  
   ```
SELECT e.emp_id, e.name, d.dept_name
FROM employees e
LEFT JOIN departments d ON e.dept_id = d.dept_id
UNION
SELECT e.emp_id, e.name, d.dept_name
FROM employees e
RIGHT JOIN departments d ON e.dept_id = d.dept_id;
```
# <sub>What is the difference between UNION and UNION ALL in FULL JOIN?</sub>
```
- UNION → Removes duplicate rows (only unique rows are returned).  
- UNION ALL → Returns all rows including duplicates.  
```
# <sub>When should you use OUTER JOINS?</sub>
```
- Use LEFT JOIN → When you want all rows from the left table, even if no match exists.  
- Use RIGHT JOIN → When you want all rows from the right table, even if no match exists.  
- Use FULL JOIN → When you want all rows from both tables, with NULLs where no match exists.  
```

   </details>

   </details>
   <details>
   
   <summary> <b> CROSS JOIN </b></summary> 
   
   # <sub>1. What is CROSS JOIN in MySQL?</sub> 
   ```
   CROSS JOIN returns the Cartesian product of two tables.
It combines each row from the first table with all rows from the second table.
```
# <sub>2. What is the syntax of CROSS JOIN?</sub>  
```
sql
SELECT column_list
FROM table1
CROSS JOIN table2;
```
# <sub>4. How many rows does CROSS JOIN return?</sub>
```
If table1 has M rows and table2 has N rows,  
then CROSS JOIN returns M × N rows.  
Example:
Table1 → 10 rows
Table2 → 5 rows
Result → 10 × 5 = 50 rows
```
# <sub>Difference between CROSS JOIN and INNER JOIN?</sub>
```
- INNER JOIN → Returns only matching rows based on a condition.  
- CROSS JOIN → Returns all possible row combinations (Cartesian product), regardless of match.
```
   </details>
   <details>
   
   <summary> <b> SELF JOIN </b></summary> 

   # <sub>1. What is a SELF JOIN?</sub>  
</br>A SELF JOIN is a regular join but the table is joined with itself.
</br>It is used when we want to compare rows within the same table.

# <sub>2. When is SELF JOIN used?</sub> 
```
To find relationships among rows of the same table.
Example: finding employees and their managers in the same employee table.
Example: finding duplicate records in a table.
```
# <sub>3. Syntax of SELF JOIN</sub>  
```
sql
SELECT column_list
FROM table_name t1
INNER JOIN table_name t2
ON t1.common_column = t2.common_column;

```
# <sub>Example of SELF JOIN</sub>
```
SELECT e1.emp_name AS Employee, e2.emp_name AS Manager
FROM employees e1
INNER JOIN employees e2
ON e1.manager_id = e2.emp_id;
```

# <sub>Join Without Using JOIN Keywords</sub>

We can combine rows from two or more tables without explicitly using the `JOIN` keyword.  
This method is called an **implicit join** (old-style join).
## 🔹 Syntax
```
sql
SELECT * 
FROM table1, table2 
WHERE condition;
```


   </details>
   
   
</details>


--------------------------------------------------------------------------------------------------------------------------------------


  <details>
   <summary> <b>SQL STRING OPERATION</b></summary>
     
   # <sub> What is the LENGTH() function in SQL? </sub>
</br> - The **LENGTH()** function is used to determine the number of characters in a string.  
</br> - It is useful for data validation, checking empty values, and analyzing text length.
     
```
     sql
SELECT LENGTH(column_name) AS length_of_string
FROM table_name;
```

# <sub> What is the TRIM() function in SQL? </sub>
</br> - The **TRIM()** function removes leading and trailing spaces (or specified characters) from a string.  
</br> - It is commonly used for **data cleaning** to ensure values are stored without unwanted spaces.

```
sql
-- Syntax
TRIM([{BOTH | LEADING | TRAILING} [trim_character] FROM] string);

-- Example 1: Remove 'x' from both ends
SELECT TRIM(BOTH 'x' FROM 'xxxCodingNinjasxxx') AS trimmed_string;
-- Output: CodingNinjas

-- Example 2: Remove spaces from both ends
SELECT TRIM(' Hello ') AS trimmed_string;
-- Output: Hello
```


   </details>
      
</details>




















