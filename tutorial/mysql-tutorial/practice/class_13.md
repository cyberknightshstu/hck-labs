# class\_13

## UNIQUE constraints

Creating a UNIQUE constraint inline:

{% code title="CREATE TABLE (UNIQUE column)" %}
```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    UNIQUE (ID)
);
```
{% endcode %}

Creating a named UNIQUE constraint:

{% code title="CREATE TABLE (named UNIQUE)" %}
```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT UC_Person UNIQUE (ID,LastName)
);
```
{% endcode %}

Add a UNIQUE constraint with ALTER TABLE:

{% code title="ALTER TABLE ADD UNIQUE" %}
```sql
ALTER TABLE Persons
ADD UNIQUE (ID);
```
{% endcode %}

Add a named UNIQUE constraint with ALTER TABLE:

{% code title="ALTER TABLE ADD CONSTRAINT UNIQUE" %}
```sql
ALTER TABLE Persons
ADD CONSTRAINT UC_Person UNIQUE (ID,LastName);
```
{% endcode %}

Dropping a UNIQUE constraint

{% hint style="info" %}
Syntax differs by RDBMS.
{% endhint %}

MySQL:

{% code title="MySQL: DROP INDEX (unique constraint)" %}
```sql
ALTER TABLE Persons
DROP INDEX UC_Person;
```
{% endcode %}

SQL (generic SQL Server / other dialects that use DROP CONSTRAINT):

{% code title="SQL: DROP CONSTRAINT (unique constraint)" %}
```sql
ALTER TABLE Persons
DROP CONSTRAINT UC_Person;
```
{% endcode %}

***

## PRIMARY KEY

Create a table with PRIMARY KEY using PRIMARY KEY clause:

{% code title="CREATE TABLE (PRIMARY KEY clause)" %}
```sql
MySQL:
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);
```
{% endcode %}

Create a table with PRIMARY KEY inline (column-level):

{% code title="CREATE TABLE (column-level PRIMARY KEY)" %}
```sql
SQL:
CREATE TABLE Persons (
    ID int NOT NULL PRIMARY KEY,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);
```
{% endcode %}

Create a named PRIMARY KEY constraint:

{% code title="CREATE TABLE (named PRIMARY KEY)" %}
```sql
All:
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT PK_Person PRIMARY KEY (ID)
);
```
{% endcode %}

Add a PRIMARY KEY with ALTER TABLE:

{% code title="ALTER TABLE ADD PRIMARY KEY" %}
```sql
ALTER TABLE Persons
ADD PRIMARY KEY (ID);
```
{% endcode %}

Add a named PRIMARY KEY constraint with ALTER TABLE:

{% code title="ALTER TABLE ADD CONSTRAINT PRIMARY KEY" %}
```sql
ALTER TABLE Persons
ADD CONSTRAINT PK_Person PRIMARY KEY (ID);
```
{% endcode %}

Dropping a PRIMARY KEY

{% hint style="info" %}
Syntax differs by RDBMS.
{% endhint %}

MySQL:

{% code title="MySQL: DROP PRIMARY KEY" %}
```sql
ALTER TABLE Persons
DROP PRIMARY KEY;
```
{% endcode %}

SQL (dialects using DROP CONSTRAINT):

{% code title="SQL: DROP CONSTRAINT (primary key)" %}
```sql
ALTER TABLE Persons
DROP CONSTRAINT PK_Person;
```
{% endcode %}
