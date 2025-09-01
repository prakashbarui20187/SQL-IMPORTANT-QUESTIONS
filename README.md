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
# <sub>36. What is the SQL WHERE clause? </sub>
</br> The **WHERE** clause is used to **filter records**.  
</br> It extracts only those records that fulfill a specified condition.
# <sub>37. Syntax of WHERE clause </sub>
</br> **SELECT** column1, column2, ...  
**FROM** table_name  
**WHERE** condition;
# <sub> Example 1 </sub>
Select all customers from **Mexico**:
</br> **SELECT** *  
**FROM** Customers  
**WHERE** Country = 'Mexico';
# <sub> Example 2 </sub>
Select the customer with **CustomerID = 1**:
</br> **SELECT** *  
**FROM** Customers  
**WHERE** CustomerID = 1;
# <sub> Example 3 </sub>
Select all customers with **CustomerID > 80**:
</br> **SELECT** *  
**FROM** Customers  
**WHERE** CustomerID > 80;
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
