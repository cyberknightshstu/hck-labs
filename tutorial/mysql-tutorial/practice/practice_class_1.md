# practice\_class\_1

{% stepper %}
{% step %}
### Connect any databases from the server

Use your database client/CLI to connect to the database server. Example connection commands:

{% code title="MySQL / MariaDB" %}
```bash
# connect to MySQL/MariaDB
mysql -u username -p -h your_db_host -P 3306
```
{% endcode %}

{% code title="PostgreSQL (psql)" %}
```bash
# connect to PostgreSQL
psql -h your_db_host -U username -d your_database
```
{% endcode %}

Connect using the appropriate client for your database, then run the SQL statements in the following steps.
{% endstep %}

{% step %}
### Create a table named "student"

Run this SQL to create the table with the specified columns:

{% code title="Create student table (SQL)" %}
```sql
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(255),
    address VARCHAR(255),
    mobile_number VARCHAR(20)
);
```
{% endcode %}

If your database uses different types or requires AUTO\_INCREMENT / SERIAL for the primary key, adapt the column definition accordingly.
{% endstep %}

{% step %}
### Insert the values in the "student" table

Example INSERT statements to add rows to the student table:

{% code title="Insert sample rows (SQL)" %}
```sql
INSERT INTO student (student_id, student_name, address, mobile_number)
VALUES
  (1, 'Alice Johnson', '123 Maple St', '555-0101'),
  (2, 'Bob Smith',     '456 Oak Ave',  '555-0202'),
  (3, 'Carol Lee',     '789 Pine Rd',  '555-0303');
```
{% endcode %}

You can modify the values or add more INSERT statements as needed.
{% endstep %}
{% endstepper %}
