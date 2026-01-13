# question\_class\_5

{% stepper %}
{% step %}
### Create table and insert rows

Create the table `hotel_inv` and insert 5 rows. Example SQL:

{% code title="create-and-insert.sql" %}
```sql
CREATE TABLE hotel_inv (
  number_of_room INT,
  room_number INT,
  facilities VARCHAR(255),
  location VARCHAR(100)
);

INSERT INTO hotel_inv (number_of_room, room_number, facilities, location) VALUES
(2, 101, 'AC, TV, kitchen', 'Dinajpur'),
(3, 102, 'AC, TV', 'Dhaka'),
(1, 201, 'kitchen, Fan', 'Dinajpur'),
(2, 202, 'AC, kitchen', 'Chittagong'),
(4, 301, 'AC, kitchen, TV', 'Dinajpur');
```
{% endcode %}

This creates the schema and populates the table with five sample rows.
{% endstep %}

{% step %}
### Show rows having location = Dinajpur

Query to retrieve all rows where location is "Dinajpur":

{% code title="select-dinajpur.sql" %}
```sql
SELECT *
FROM hotel_inv
WHERE location = 'Dinajpur';
```
{% endcode %}

This returns all columns for rows whose location equals 'Dinajpur'.
{% endstep %}

{% step %}
### Show room\_number which has both kitchen and AC facilities

If `facilities` is stored as a comma-separated string, use LIKE to match both terms:

{% code title="select-kitchen-ac.sql" %}
```sql
SELECT room_number
FROM hotel_inv
WHERE facilities LIKE '%kitchen%'
  AND facilities LIKE '%AC%';
```
{% endcode %}

This returns the room numbers whose facilities contain both "kitchen" and "AC".
{% endstep %}

{% step %}
### Order the room numbers in descending order

To get all room numbers ordered descending:

{% code title="select-room-desc.sql" %}
```sql
SELECT room_number
FROM hotel_inv
ORDER BY room_number DESC;
```
{% endcode %}

If you want both filtering (e.g., those with kitchen and AC) and ordering descending:

{% code title="select-kitchen-ac-desc.sql" %}
```sql
SELECT room_number
FROM hotel_inv
WHERE facilities LIKE '%kitchen%'
  AND facilities LIKE '%AC%'
ORDER BY room_number DESC;
```
{% endcode %}
{% endstep %}
{% endstepper %}
