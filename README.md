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
</br>-In SQL DB, data is stored in the form of tables.
</br>-Data can be of different types, like INT, CHAR etc
</br>CHAR - string(0-255), string with size = (0, 255], e.g., CHAR(251)
</br>VARCHAR- string(0-255)
</br>TINYTEXT-String(0-255)
</br>TEXT-string(0-65535)
</br>BLOB-string(0-65535)
</br>MEDIUMTEXT-string(0-16777215)
</br>MEDIUMBLOB-string(0-16777215)
</br>LONGTEXT- string(0-4294967295)
</br>LONGBLOB- string(0-4294967295)
</br>TINYINT- integer(-128 to 127)
</br>SMALLINT- integer(-32768 to 32767)
</br>MEDIUMINT- integer(-8388608 to 8388607)
</br>INT- integer(-2147483648 to 2147483647)
</br>BIGINT- integer (-9223372036854775808 to
</br>9223372036854775807)
</br>FLOAT- Decimal with precision to 23 digits
</br>DOUBLE- Decimal with 24 to 53 digits
</br>DECIMAL- Double stored as string
</br>DATE- YYYY-MM-DD
</br>DATETIME- YYYY-MM-DD HH:MM:SS
</br>TIMESTAMP- YYYYMMDDHHMMSS
</br>TIME- HH:MM:SS
</br>ENUM- One of the preset values
</br>SET- One or many of the preset values
</br>BOOLEAN - 0/1
# <SUB>8. Size: TINY < SMALL < MEDIUM < INT < BIGINT.</SUB>
# <sub>9. Variable length Data types e.g., VARCHAR, are better to use as they occupy space equal to the actual data Size.</sub>
# <sub>10. Values can also be unsigned e.g., INT UNSIGNED. </sub>
# <sub>Types of SQL commands: <sub>
</br>* DDL (data definition language): defining relation schema.
1. CREATE: create table, DB, view.
2. ALTER TABLE: modification in table structure. e.g, change column datatype or add/remove columns.
3. DROP: delete table, DB, view.
4. TRUNCATE: remove all the tuples from the table.
5. RENAME: rename DB name, table name, column name etc
