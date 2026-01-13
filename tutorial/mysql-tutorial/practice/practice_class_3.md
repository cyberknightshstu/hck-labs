# practice\_class\_3

{% stepper %}
{% step %}
### Connect any databases from the server

Connect to the database server using your preferred client (CLI, GUI, or programmatic driver) and open the target database where you'll perform the following operations.
{% endstep %}

{% step %}
### Create a table named "student"

Create a table named `student` with columns `student_id`, `student_name`, `address`, `mobile_number`.

Example (SQL):

{% code title="create-student.sql" %}
```sql
CREATE TABLE student (
  student_id    INT,
  student_name  VARCHAR(255),
  address       VARCHAR(255),
  mobile_number VARCHAR(50)
);
```
{% endcode %}
{% endstep %}

{% step %}
### Change the datatype of student\_id column

Alter the `student_id` column datatype. SQL syntax differs between database engines; here are two common variants:

Example — MySQL:

{% code title="mysql-change-datatype.sql" %}
```sql
ALTER TABLE student
MODIFY COLUMN student_id BIGINT;
```
{% endcode %}

Example — PostgreSQL:

{% code title="postgres-change-datatype.sql" %}
```sql
ALTER TABLE student
ALTER COLUMN student_id TYPE BIGINT;
```
{% endcode %}
{% endstep %}

{% step %}
### Add new column named "CGPA" into the student table

Add a new column `CGPA` to the `student` table.

Example (SQL):

{% code title="add-cgpa.sql" %}
```sql
ALTER TABLE student
ADD COLUMN CGPA DECIMAL(3,2);
```
{% endcode %}
{% endstep %}

{% step %}
### Delete the column named "address"

Remove the `address` column from the `student` table.

Example — MySQL / PostgreSQL:

{% code title="drop-address.sql" %}
```sql
ALTER TABLE student
DROP COLUMN address;
```
{% endcode %}
{% endstep %}
{% endstepper %}
