# class\_5

{% code title="setup.sql" %}
```sql
se mysql;
CREATE TABLE CUSTOMERS(
   ID   INT              ,
   NAME VARCHAR (20)     ,
   AGE  INT              ,
   ADDRESS  CHAR (25) ,
   SALARY   DECIMAL (18, 2)
);
```
{% endcode %}

{% code title="inserts.sql" %}
```sql
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (1, 'Ramesh', 32, 'Ahmedabad', 2000.00 );

INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (2, 'Khilan', 25, 'Delhi', 1500.00 );

INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (3, 'Kaushik', 23, 'Kota', 2000.00 );

INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY) VALUES
(4, 'Chaitali', 25, 'Mumbai', 6500.00 ),
(5, 'Hardik', 27, 'Bhopal', 8500.00 ),
(6, 'Komal', 22, 'Hyderabad', 4500.00 );
```
{% endcode %}

{% code title="queries.sql" %}
```sql
select * from customers;

SELECT *
FROM Customers
WHERE age >25 and salary>1500;

SELECT * FROM Customers
WHERE address= 'bhopal' AND (Name LIKE 'R%' OR Name LIKE 'H%');

SELECT * FROM Customers
WHERE NOT address = 'bhopal';

SELECT * FROM Customers
WHERE Name NOT LIKE 'K%';

SELECT * FROM Customers
WHERE address NOT IN ('delhi', 'Kota');

SELECT * FROM Customers
WHERE NOT ID > 2;

SELECT * FROM Customers
WHERE NOT Id < 3;
```
{% endcode %}
