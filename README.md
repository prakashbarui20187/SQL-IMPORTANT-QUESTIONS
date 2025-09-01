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

<details>




   
<summary> <b>TYPES OF SQL commands:</b></summary>

# <sub>11.Types of SQL commands: <sub>
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
      
</details>






      
</details>




















