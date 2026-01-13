# class\_1\_script

{% stepper %}
{% step %}
### show databases;

```sql
show databases;
```
{% endstep %}

{% step %}
### use mysql;

```sql
use mysql;
```
{% endstep %}

{% step %}
### show tables;

```sql
show tables;
```
{% endstep %}

{% step %}
### select \* from component;

```sql
select * from component;
```
{% endstep %}

{% step %}
### CREATE TABLE Persons

```sql
CREATE TABLE Persons (
    PersonID INT,
    LastName VARCHAR(255),
    FirstName VARCHAR(255),
    Address VARCHAR(255),
    City VARCHAR(255)
);
```
{% endstep %}

{% step %}
### select \* from Persons;

```sql
select * from Persons;
```
{% endstep %}

{% step %}
### insert into Persons

```sql
insert into Persons
values(1, 'Sultana', 'Tangina', 'HSTU', 'Dinajpur');
```
{% endstep %}

{% step %}
### select \* from Persons;

```sql
select * from Persons;
```
{% endstep %}
{% endstepper %}
