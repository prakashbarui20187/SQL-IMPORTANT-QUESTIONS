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
# <sub>Types of SQL commands: <sub>
</br>**DDL (data definition language): defining relation schema.**
1.**CREATE**: create table, DB, view.
2.**ALTER TABLE**: modification in table structure. e.g, change column datatype or add/remove columns.
3.**DROP**: delete table, DB, view.
4.**TRUNCATE**: remove all the tuples from the table.
5.**RENAME**: rename DB name, table name, column name etc
