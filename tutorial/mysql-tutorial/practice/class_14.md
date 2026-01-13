# class\_14

### Foreign Keys

{% tabs %}
{% tab title="For all" %}
{% code title="Create table with named FK" %}
```sql
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    CONSTRAINT FK_PersonOrder FOREIGN KEY (PersonID)
    REFERENCES Persons(PersonID)
);
```
{% endcode %}

{% code title="Add FK via ALTER" %}
```sql
ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);

ALTER TABLE Orders
ADD CONSTRAINT FK_PersonOrder
FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);

ALTER TABLE Orders
DROP FOREIGN KEY FK_PersonOrder;

ALTER TABLE Orders
DROP CONSTRAINT FK_PersonOrder;
```
{% endcode %}
{% endtab %}

{% tab title="MySQL" %}
{% code title="Create table with FK (MySQL)" %}
```sql
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
```
{% endcode %}

{% code title="Alter table FK (MySQL)" %}
```sql
ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);

ALTER TABLE Orders
ADD CONSTRAINT FK_PersonOrder
FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);

ALTER TABLE Orders
DROP FOREIGN KEY FK_PersonOrder;

ALTER TABLE Orders
DROP CONSTRAINT FK_PersonOrder;
```
{% endcode %}
{% endtab %}
{% endtabs %}

***

### CHECK Constraints

{% tabs %}
{% tab title="For all" %}
{% code title="Create table with named CHECK" %}
```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255),
    CONSTRAINT CHK_Person CHECK (Age>=18 AND City='Sandnes')
);
```
{% endcode %}
{% endtab %}

{% tab title="MySQL" %}
{% code title="Create table with CHECK (MySQL)" %}
```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
);
```
{% endcode %}

{% code title="Alter table CHECK (MySQL)" %}
```sql
ALTER TABLE Persons
ADD CHECK (Age>=18);

ALTER TABLE Persons
ADD CONSTRAINT CHK_PersonAge CHECK (Age>=18 AND City='Sandnes');

ALTER TABLE Persons
DROP CHECK CHK_PersonAge;
```
{% endcode %}
{% endtab %}
{% endtabs %}
