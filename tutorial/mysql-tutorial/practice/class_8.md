# class\_8

## SUM examples

{% code title="Sum total quantity" %}
```sql
SELECT SUM(Quantity)
FROM OrderDetails;
```
{% endcode %}

{% code title="Sum quantity for a specific product" %}
```sql
SELECT SUM(Quantity)
FROM OrderDetails
WHERE ProductId = 11;
```
{% endcode %}

{% code title="Sum with column alias" %}
```sql
SELECT SUM(Quantity) AS total
FROM OrderDetails;
```
{% endcode %}

{% code title="Sum grouped by OrderID" %}
```sql
SELECT OrderID, SUM(Quantity) AS Total_Quantity
FROM OrderDetails
GROUP BY OrderID;
```
{% endcode %}

{% code title="Sum of expression (quantity * 10)" %}
```sql
SELECT SUM(Quantity * 10)
FROM OrderDetails;
```
{% endcode %}

***

## AVG examples

{% code title="Average price (all products)" %}
```sql
SELECT AVG(Price)
FROM Products;
```
{% endcode %}

{% code title="Average price for a category" %}
```sql
SELECT AVG(Price)
FROM Products
WHERE CategoryID = 1;
```
{% endcode %}

{% code title="Average price with alias" %}
```sql
SELECT AVG(Price) AS [average price]
FROM Products;
```
{% endcode %}

{% code title="Products with price above overall average" %}
```sql
SELECT * FROM Products
WHERE price > (SELECT AVG(price) FROM Products);
```
{% endcode %}

{% code title="Average price grouped by category" %}
```sql
SELECT AVG(Price) AS AveragePrice, CategoryID
FROM Products
GROUP BY CategoryID;
```
{% endcode %}
