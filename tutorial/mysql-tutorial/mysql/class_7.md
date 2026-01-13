# class\_7

## Use database

{% code title="use-database.sql" %}
```sql
use mysql;
```
{% endcode %}

## Select all from customers

{% code title="select-all-customers.sql" %}
```sql
select * from customers;
```
{% endcode %}

## Select with LIMIT

{% code title="select-limit.sql" %}
```sql
SELECT * FROM Customers
LIMIT 3;
```
{% endcode %}

## Select with WHERE and LIMIT

{% code title="select-where-limit.sql" %}
```sql
SELECT  * FROM Customers
WHERE name='Kaushik'
limit 1;
```
{% endcode %}

## MIN and MAX examples

{% code title="select-min.sql" %}
```sql
SELECT MIN(Price)
FROM Products;
```
{% endcode %}

{% code title="select-max.sql" %}
```sql
SELECT MAX(Price)
FROM Products;
```
{% endcode %}

## MIN with GROUP BY

{% code title="min-groupby.sql" %}
```sql
SELECT MIN(Price) AS SmallestPrice, CategoryID
FROM Products
GROUP BY CategoryID;
```
{% endcode %}

## COUNT examples

{% code title="count-all.sql" %}
```sql
SELECT COUNT(*)
FROM Products;
```
{% endcode %}

{% code title="count-productname.sql" %}
```sql
SELECT COUNT(ProductName)
FROM Products;
```
{% endcode %}

{% code title="count-where.sql" %}
```sql
SELECT COUNT(ProductID)
FROM Products
WHERE Price > 20;
```
{% endcode %}

{% code title="count-distinct.sql" %}
```sql
SELECT COUNT(DISTINCT Price)
FROM Products;
```
{% endcode %}

{% code title="count-as-alias.sql" %}
```sql
SELECT COUNT(*) AS NumberOfRecords
FROM Products;
```
{% endcode %}

{% code title="count-groupby.sql" %}
```sql
SELECT COUNT(*) AS "Number of records", CategoryID
FROM Products
GROUP BY CategoryID;
```
{% endcode %}
