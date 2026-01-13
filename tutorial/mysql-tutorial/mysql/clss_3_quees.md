# clss\_3\_quees

{% stepper %}
{% step %}
### Create a database named `student` and connect to that database

{% code title="SQL" %}
```sql
CREATE DATABASE student;
USE student;
```
{% endcode %}
{% endstep %}

{% step %}
### Create a table named `attendance` with columns and insert 5 rows

Columns: `serial_no`, `course_code`, `course_title`, `class_time`

{% code title="SQL" %}
```sql
CREATE TABLE attendance (
  serial_no INT PRIMARY KEY,
  course_code VARCHAR(50),
  course_title VARCHAR(255),
  class_time VARCHAR(50)
);

INSERT INTO attendance (serial_no, course_code, course_title, class_time) VALUES
  (1, 'CS101', 'Introduction to Computer Science', '09:00'),
  (2, 'MATH201', 'Calculus II', '10:30'),
  (3, 'PHY150', 'General Physics', '13:00'),
  (4, 'ENG101', 'English Composition', '14:30'),
  (5, 'HIS210', 'World History', '16:00');
```
{% endcode %}
{% endstep %}

{% step %}
### Delete all the rows you created in the `attendance` table

{% code title="SQL" %}
```sql
DELETE FROM attendance;
```
{% endcode %}
{% endstep %}

{% step %}
### Change the datatype of `class_time` column

(Example: change `class_time` from VARCHAR to DATETIME)

{% code title="SQL" %}
```sql
ALTER TABLE attendance
MODIFY class_time DATETIME;
```
{% endcode %}
{% endstep %}

{% step %}
### Create new column named `class_room` and then drop it

{% code title="SQL" %}
```sql
ALTER TABLE attendance
ADD class_room VARCHAR(50);

ALTER TABLE attendance
DROP COLUMN class_room;
```
{% endcode %}
{% endstep %}
{% endstepper %}
