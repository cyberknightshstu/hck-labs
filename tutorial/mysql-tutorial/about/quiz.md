# quiz

{% stepper %}
{% step %}
### Create the database and connect to it

SQL (MySQL / MariaDB / compatible):

```sql
-- Create database
CREATE DATABASE student;

-- Connect to the database
USE student;
```
{% endstep %}

{% step %}
### Create the tables

Create two tables: attendance and faculty\_member with the requested columns.

```sql
-- attendance table
CREATE TABLE attendance (
  serial_no INT PRIMARY KEY,
  course_code VARCHAR(20),
  course_title VARCHAR(255),
  class_time VARCHAR(50)
);

-- faculty_member table
CREATE TABLE faculty_member (
  serial_no INT PRIMARY KEY,
  name VARCHAR(255),
  dept VARCHAR(100),
  room_number VARCHAR(50)
);
```
{% endstep %}

{% step %}
### Insert 10 rows into each table

Example data (10 rows per table). Adjust values as needed.

```sql
-- Insert 10 rows into attendance
INSERT INTO attendance (serial_no, course_code, course_title, class_time) VALUES
(1,  'CS101', 'Intro to Computer Science', '09:00 AM'),
(2,  'MA101', 'Calculus I', '10:00 AM'),
(3,  'PH101', 'Physics I', '11:00 AM'),
(4,  'CS102', 'Data Structures', '12:00 PM'),
(5,  'EN101', 'English Literature', '01:00 PM'),
(6,  'CH101', 'Chemistry I', '02:00 PM'),
(7,  'CS201', 'Algorithms', '03:00 PM'),
(8,  'MA201', 'Linear Algebra', '04:00 PM'),
(9,  'EE101', 'Basic Electronics', '05:00 PM'),
(10, 'CS301', 'Operating Systems', '06:00 PM');

-- Insert 10 rows into faculty_member
INSERT INTO faculty_member (serial_no, name, dept, room_number) VALUES
(1,  'Dr. Alice Smith',   'Computer Science', 'R101'),
(2,  'Dr. Bob Johnson',   'Mathematics',      'R102'),
(3,  'Dr. Carol Davis',   'Physics',          'R103'),
(4,  'Dr. David Lee',     'Computer Science', 'R104'),
(5,  'Dr. Eva Martinez',  'English',          'R105'),
(6,  'Dr. Frank Brown',   'Chemistry',        'R106'),
(7,  'Dr. Grace Wilson',  'Computer Science', 'R107'),
(8,  'Dr. Henry Clark',   'Mathematics',      'R108'),
(9,  'Dr. Ivy Young',     'Electronics',      'R109'),
(10, 'Dr. John King',     'Computer Science', 'R110');
```
{% endstep %}

{% step %}
### Display all values of the attendance table

```sql
SELECT * FROM attendance;
```

This returns all rows and columns from attendance.
{% endstep %}

{% step %}
### Find "common" (duplicate) values in faculty\_member

If by "common values" you mean rows or values that repeat (duplicates) within faculty\_member, here are a few useful queries:

* To find duplicate names (names that appear more than once):

```sql
SELECT name, COUNT(*) AS occurrences
FROM faculty_member
GROUP BY name
HAVING COUNT(*) > 1;
```

* To find duplicate rows across all columns (exact duplicate rows):

```sql
SELECT serial_no, name, dept, room_number, COUNT(*) AS occurrences
FROM faculty_member
GROUP BY serial_no, name, dept, room_number
HAVING COUNT(*) > 1;
```

Note: In the provided sample data primary key serial\_no is unique, so these queries will return no duplicates. If you meant "common values" between the two tables (values that appear in both tables), see the next step.
{% endstep %}

{% step %}
### Show values of the two tables with distinct rows / columns

Here are several interpretations and corresponding queries:

* Select distinct rows from each table individually:

```sql
SELECT DISTINCT * FROM attendance;
SELECT DISTINCT * FROM faculty_member;
```

* Select distinct values of a specific column (example: distinct course\_code and distinct dept):

```sql
SELECT DISTINCT course_code FROM attendance;
SELECT DISTINCT dept FROM faculty_member;
```

* Show combined distinct rows from both tables for comparable columns (for example, if you want a list of distinct identifiers/shared values). Since tables have different schemas, you can UNION comparable columns. Example: distinct serial\_no values present in either table:

```sql
SELECT serial_no FROM attendance
UNION
SELECT serial_no FROM faculty_member;
```

* If you want to find distinct values that are common to both tables for a comparable column (e.g., serial\_no present in both):

```sql
SELECT a.serial_no
FROM attendance a
INNER JOIN faculty_member f ON a.serial_no = f.serial_no;
```

* To show distinct combinations across some columns from both tables, you can UNION matching columns. Example: combine course\_code from attendance and dept from faculty\_member (only meaningful if you want to treat them as a single column):

```sql
SELECT DISTINCT course_code AS value FROM attendance
UNION
SELECT DISTINCT dept AS value FROM faculty_member;
```

Choose the query that matches the exact "distinct" result you need.
{% endstep %}
{% endstepper %}
