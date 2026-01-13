# class\_21

## Single line comments

```sql
-- Select all:
SELECT * FROM Customers;

SELECT * FROM Customers -- WHERE City='Berlin';
```

## Multiple line comments

```sql
/*Select all the columns
of all the records
in the Customers table:*/
SELECT * FROM Customers;
```

## Backup database

```sql
BACKUP DATABASE testDB
TO DISK = 'D:\backups\testDB.bak';
```

```sql
BACKUP DATABASE testDB
TO DISK = 'D:\backups\testDB.bak'
WITH DIFFERENTIAL;
```

## Index

```sql
CREATE INDEX idx_lastname
ON Persons (LastName);
```

```sql
CREATE INDEX idx_pname
ON Persons (LastName, FirstName);
```

```sql
ALTER TABLE table_name
DROP INDEX index_name;
```
