# class\_2

```sql
CREATE DATABASE testDB;
```

```sql
show databases;
```

```sql
DROP DATABASE testDB;
```

```sql
show databases;
```

```sql
CREATE DATABASE testDB;
```

```sql
use sys;
```

```sql
show tables;
```

```sql
use mysql;
```

```sql
show tables;
```

```sql
select * from Persons;
```

```sql
TRUNCATE TABLE persons;
```

```sql
select * from Persons;
```

```sql
insert into Persons
values(1, 'Sultana', 'Tangina', 'HSTU', 'Dinajpur');
```

```sql
select * from Persons;
```

```sql
DROP TABLE persons;
```

```sql
show tables;
```

***

```sql
CREATE TABLE Persons (
    PersonID INT,
    LastName VARCHAR(255),
    FirstName VARCHAR(255),
    Address VARCHAR(255),
    City VARCHAR(255)
);
```

```sql
select * from Persons;
```

```sql
insert into Persons
values(1, 'Sultana', 'Tangina', 'HSTU', 'Dinajpur');
```

```sql
select * from Persons;
```

```sql
insert into Persons
values(2, 'Tubba', 'Diyana', 'Balubari', 'Dinajpur');
```

```sql
insert into Persons
values(3, 'Mueed', 'Dihyat Al', 'Balubari', 'Dinajpur');
```

```sql
ALTER TABLE persons
ADD Email varchar(255);
```

```sql
select * from Persons;
```

```sql
ALTER TABLE persons
DROP COLUMN Email;
```

```sql
select * from Persons;
```

```sql
ALTER TABLE Persons
ADD DateOfBirth date;
```

```sql
ALTER TABLE Persons
modify COLUMN DateOfBirth year;
```

```sql
select * from Persons;
```

```sql
ALTER TABLE Persons
DROP Column DateOfBirth;
```

```sql
select * from Persons;
```
