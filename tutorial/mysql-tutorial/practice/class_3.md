# class\_3

## Select statements

{% code title="select_lastname.sql" %}
```sql
select LastName from Persons;
select distinct address from Persons;
select count(distinct address) from Persons;
```
{% endcode %}

## Add Email column, query, then drop Email column

{% code title="alter_add_email.sql" %}
```sql
ALTER TABLE persons
ADD Email varchar(255);
select * from Persons;
```
{% endcode %}

{% code title="alter_drop_email.sql" %}
```sql
ALTER TABLE persons
DROP COLUMN Email;
select * from Persons;
```
{% endcode %}

## Add DateOfBirth, modify its type, query, then drop it

{% code title="alter_dateofbirth.sql" %}
```sql
ALTER TABLE Persons
ADD DateOfBirth date;
ALTER TABLE Persons
modify COLUMN DateOfBirth year;
select * from Persons;
ALTER TABLE Persons
DROP Column DateOfBirth;
select * from Persons;
```
{% endcode %}

## Show tables

{% code title="show_tables.sql" %}
```sql
show tables;
```
{% endcode %}
