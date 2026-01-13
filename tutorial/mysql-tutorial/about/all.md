# all

{% stepper %}
{% step %}
### Student database — setup and attendance table

1. Create a database named `student` and connect to it.

{% code title="Create DB & use it" %}
```
```
{% endcode %}

```sql
CREATE DATABASE student;
USE student;
```

2. Create a table named `attendance` with columns `serial_no`, `student_id`, `course_code`, `course_title`, `class_time`, `gpa`, and insert 10 rows.

{% code title="Create attendance table" %}
```sql
CREATE TABLE attendance (
  serial_no    INT PRIMARY KEY,
  student_id   INT,
  course_code  VARCHAR(20),
  course_title VARCHAR(100),
  class_time   INT,        -- initial datatype (can be changed later)
  gpa          DECIMAL(3,2)
);
```
{% endcode %}

{% code title="Insert 10 rows" %}
```sql
INSERT INTO attendance VALUES
(1,  10210, 'C101', 'Intro to C',        45, 3.10),
(2,  10211, 'C102', 'Advanced C',        60, 3.40),
(3,  10212, 'M201', 'Calculus I',        50, 2.95),
(4,  10213, 'P301', 'Physics I',         55, 3.20),
(5,  10214, 'C101', 'Intro to C',        45, 3.25),
(6,  10215, 'E101', 'English Basics',    40, 2.80),
(7,  10216, 'C202', 'C Programming II',  70, 3.60),
(8,  10217, 'H101', 'History',           35, 3.00),
(9,  10218, 'C103', 'C Data Structures', 65, 3.45),
(10, 10219, 'M202', 'Calculus II',       55, 3.05);
```
{% endcode %}

3. Delete all the rows that you have created in the `attendance` table.

{% code title="Delete rows" %}
```sql
DELETE FROM attendance;
-- or to remove only those 10 rows if table may contain others:
-- DELETE FROM attendance WHERE serial_no BETWEEN 1 AND 10;
```
{% endcode %}

4. Change the datatype of the `class_time` column.

Note: adjust the target datatype to the type you need (example below changes it to TIME or VARCHAR).

{% code title="Change datatype (examples)" %}
```sql
-- MySQL example: change to TIME
ALTER TABLE attendance MODIFY class_time TIME;

-- Or change to VARCHAR
ALTER TABLE attendance MODIFY class_time VARCHAR(50);
```
{% endcode %}

5. Create new column named `class_room` and drop it.

{% code title="Add and drop column" %}
```sql
ALTER TABLE attendance ADD COLUMN class_room VARCHAR(50);
ALTER TABLE attendance DROP COLUMN class_room;
```
{% endcode %}

6. Find average `class_time` for each course and order it in descending order.

Assuming `class_time` is numeric (if converted to TIME, use appropriate functions).

{% code title="Average class_time per course" %}
```sql
SELECT course_code, AVG(class_time) AS avg_class_time
FROM attendance
GROUP BY course_code
ORDER BY avg_class_time DESC;
```
{% endcode %}

7. How many courses are present in the student database?

Count distinct course codes from `attendance`:

{% code title="Count distinct courses" %}
```sql
SELECT COUNT(DISTINCT course_code) AS total_courses
FROM attendance;
```
{% endcode %}

8. Find the `student_id` from the attendance table whose `gpa` is greater than 3.15.

{% code title="Student IDs with gpa > 3.15" %}
```sql
SELECT student_id
FROM attendance
WHERE gpa > 3.15;
```
{% endcode %}

9. Find the `course_code` and `class_time` of `student_id = 10214`.

{% code title="Course_code and class_time for student_id=10214" %}
```sql
SELECT course_code, class_time
FROM attendance
WHERE student_id = 10214;
```
{% endcode %}

10. Select all the `course_code` started by `C`.

{% code title="Course codes starting with C" %}
```sql
SELECT DISTINCT course_code
FROM attendance
WHERE course_code LIKE 'C%';
```
{% endcode %}
{% endstep %}

{% step %}
### Student table — connect, create, insert

1. Connect any database from the server (example: connect to previously created `student` database).

{% code title="Use database" %}
```sql
USE student;
```
{% endcode %}

2. Create a table named `student` having columns `student_id`, `student_name`, `address`, `mobile_number`.

{% code title="Create student table" %}
```sql
CREATE TABLE student (
  student_id     INT PRIMARY KEY,
  student_name   VARCHAR(100),
  address        VARCHAR(255),
  mobile_number  VARCHAR(20)
);
```
{% endcode %}

3. Insert the values in the `student` table.

{% code title="Insert sample students" %}
```sql
INSERT INTO student VALUES
(10210, 'Alice Khan',    'Dhaka',      '01710000001'),
(10211, 'Bilal Ahmed',   'Chittagong', '01710000002'),
(10212, 'Chitra Roy',    'Sylhet',     '01710000003'),
(10213, 'David Saha',    'Rajshahi',   '01710000004'),
(10214, 'Esha Begum',    'Khulna',     '01710000005');
```
{% endcode %}
{% endstep %}

{% step %}
### Hotel inventory — create and queries

1. Create a table named `hotel_inv` having `number_of_room`, `room_number`, `facilities`, `location` columns and insert 15 rows.

{% code title="Create hotel_inv table" %}
```sql
CREATE TABLE hotel_inv (
  number_of_room INT,
  room_number    VARCHAR(20),
  facilities     VARCHAR(255), -- e.g. 'AC,kitchen' or 'AC' etc.
  location       VARCHAR(100)
);
```
{% endcode %}

{% code title="Insert 15 sample rows" %}
```sql
INSERT INTO hotel_inv VALUES
(1, '101', 'AC,kitchen', 'Rangpur'),
(1, '102', 'AC',         'Rangpur'),
(1, '103', 'kitchen',    'Dhaka'),
(1, '104', 'AC,kitchen', 'Rangpur'),
(1, '105', 'AC',         'Sylhet'),
(1, '106', 'kitchen',    'Rangpur'),
(1, '107', 'AC,kitchen', 'Chittagong'),
(1, '108', 'AC',         'Rangpur'),
(1, '109', 'kitchen',    'Khulna'),
(1, '110', 'AC,kitchen', 'Rangpur'),
(1, '115', 'AC',         'Rangpur'),
(1, '205', 'kitchen',    'Rangpur'),
(1, '305', 'AC,kitchen', 'Dhaka'),
(1, '405', 'AC',         'Rangpur'),
(1, '505', 'kitchen',    'Rangpur');
```
{% endcode %}

2. Show the rows having `location = Rangpur`.

{% code title="Rows with location = Rangpur" %}
```sql
SELECT *
FROM hotel_inv
WHERE location = 'Rangpur';
```
{% endcode %}

3. Show all the `room_number` which has kitchen and AC facilities.

Assumes `facilities` stores comma-separated values.

{% code title="Rooms with both kitchen and AC" %}
```sql
SELECT room_number
FROM hotel_inv
WHERE facilities LIKE '%kitchen%' AND facilities LIKE '%AC%';
```
{% endcode %}

4. Order the room number in descending order.

{% code title="Room numbers descending" %}
```sql
SELECT room_number
FROM hotel_inv
ORDER BY room_number DESC;
```
{% endcode %}

5. Find the total number of room in that hotel.

If `number_of_room` is a per-row count, sum it; otherwise count rows.

{% code title="Total number of rooms (sum)" %}
```sql
SELECT SUM(number_of_room) AS total_rooms
FROM hotel_inv;
```
{% endcode %}

6. Select all the rooms which has the room number \_5% (i.e., pattern matching where room\_number contains '5' as first char followed by any characters).

If you meant room numbers that start with '5' or contain '5' at a specific position, adjust the pattern. Example: room\_number starting with '5':

{% code title="Rooms starting with " %}
```sql
SELECT *
FROM hotel_inv
WHERE room_number LIKE '5%';
```
{% endcode %}

If you intended a different pattern, replace the LIKE pattern accordingly (e.g., '\_5%' matches any single char then '5' then anything):

{% code title="Rooms with pattern _5%" %}
```sql
SELECT *
FROM hotel_inv
WHERE room_number LIKE '_5%';
```
{% endcode %}
{% endstep %}
{% endstepper %}
