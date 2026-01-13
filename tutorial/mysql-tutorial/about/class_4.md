# class\_4

### List databases

{% code title="show_databases.sql" %}
```sql
show databases;
```
{% endcode %}

### Switch to information\_schema

{% code title="use_information_schema.sql" %}
```sql
use information_schema;
```
{% endcode %}

### Show tables

{% code title="show_tables.sql" %}
```sql
show tables;
```
{% endcode %}

### Query routines (filter by name = 'format\_bytes')

{% code title="routines_by_name.sql" %}
```sql
select * from routines
where routine_name='format_bytes';
```
{% endcode %}

### Query routines (filter by character\_maximum\_length = 64)

{% code title="routines_length_eq_64.sql" %}
```sql
select * from routines
where character_maximum_length=64;
```
{% endcode %}

### Query routines (filter by character\_maximum\_length > 64)

{% code title="routines_length_gt_64.sql" %}
```sql
select * from routines
where character_maximum_length>64;
```
{% endcode %}

### Query routines (order by specific\_name)

{% code title="routines_order_by_specific_name.sql" %}
```sql
select * from routines
order by specific_name;
```
{% endcode %}

### Query routines (order by character\_maximum\_length ascending)

{% code title="routines_order_by_length_asc.sql" %}
```sql
select * from routines
order by character_maximum_length asc;
```
{% endcode %}

### Query routines (order by character\_maximum\_length descending)

{% code title="routines_order_by_length_desc.sql" %}
```sql
select * from routines
order by character_maximum_length desc;
```
{% endcode %}

### Query routines (name = 'format\_bytes' and character\_maximum\_length > 64)

{% code title="routines_name_and_length_filter.sql" %}
```sql
select * from routines
where routine_name='format_bytes' and character_maximum_length>64;
```
{% endcode %}
