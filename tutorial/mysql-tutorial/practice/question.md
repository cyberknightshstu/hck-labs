# question

{% stepper %}
{% step %}
### Create the table

Create a table named `gpa` with columns `serial_num`, `student_id`, `course_title`, `cgpa`, and make `student_id` the primary key.

{% code title="Create table" %}
```sql
CREATE TABLE gpa (
  serial_num   INTEGER,
  student_id   INTEGER PRIMARY KEY,
  course_title VARCHAR(255),
  cgpa         NUMERIC(3,2)
);
```
{% endcode %}
{% endstep %}

{% step %}
### Make `serial_num` unique (after table creation)

Add a uniqueness constraint on `serial_num` so only unique values are allowed.

{% code title="Add unique constraint" %}
```sql
ALTER TABLE gpa
ADD CONSTRAINT unique_serial_num UNIQUE (serial_num);
```
{% endcode %}
{% endstep %}

{% step %}
### Delete the primary key column

Remove the `student_id` column (the primary key column). Note: dropping the column will also remove any constraints tied to that column.

{% code title="Drop primary key column" %}
```sql
ALTER TABLE gpa
DROP COLUMN student_id;
```
{% endcode %}
{% endstep %}

{% step %}
### Insert rows and demonstrate `serial_num` uniqueness

Insert some rows with unique `serial_num` values, then attempt to insert a duplicate `serial_num` to show the uniqueness enforcement.

Insert unique rows:

{% code title="Insert unique rows" %}
```sql
INSERT INTO gpa (serial_num, course_title, cgpa) VALUES (1, 'Calculus', 3.50);
INSERT INTO gpa (serial_num, course_title, cgpa) VALUES (2, 'Physics', 3.75);
INSERT INTO gpa (serial_num, course_title, cgpa) VALUES (3, 'Chemistry', 3.20);
```
{% endcode %}

Verify the data:

{% code title="Select rows" %}
```sql
SELECT * FROM gpa;
```
{% endcode %}

Attempt to insert a duplicate `serial_num`:

{% code title="Insert duplicate serial_num (will fail)" %}
```sql
INSERT INTO gpa (serial_num, course_title, cgpa) VALUES (2, 'Biology', 3.60);
```
{% endcode %}

Expected result: the last INSERT will fail with a uniqueness/constraint violation error such as:

* PostgreSQL: ERROR: duplicate key value violates unique constraint "unique\_serial\_num"
* MySQL: ERROR 1062 (23000): Duplicate entry '2' for key 'unique\_serial\_num'
{% endstep %}
{% endstepper %}
