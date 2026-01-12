# SQL Injection Training Labs

## HSTU CyberKnights

SQLi Training Labs

* [Dashboard](https://sqli.lab.hstucyberknights.top/)

Labs

* [Lab 1: Auth BypassBeginner](labs/sql-injection-training-labs-6.md)
* [Lab 2: Hidden DataBeginner](sql-injection-training-labs-6.md)
* [Lab 3: Login BypassBeginner](sql-injection-training-labs-9.md)
* [Lab 4: UNION ColumnsBeginner](labs/sql-injection-training-labs-4.md)
* [Lab 5: Text ColumnBeginner](labs/sql-injection-training-labs-7.md)
* [Lab 6: Data RetrievalIntermediate](labs/sql-injection-training-labs-1.md)
* [Lab 7: Multi ValuesIntermediate](sql-injection-training-labs-5.md)
* [Lab 8: Oracle VersionIntermediate](labs/sql-injection-training-labs-5.md)
* [Lab 9: MySQL VersionIntermediate](labs/sql-injection-training-labs.md)
* [Lab 10: DB ContentsAdvanced](sql-injection-training-labs-3.md)
* [Lab 11: Oracle ContentsAdvanced](sql-injection-training-labs-11.md)
* [Lab 12: Blind ResponsesAdvanced](sql-injection-training-labs-8.md)
* [Lab 13: Blind ErrorsAdvanced](sql-injection-training-labs-7.md)
* [Lab 14: Time DelaysAdvanced](sql-injection-training-labs-2.md)
* [Lab 15: Time RetrievalAdvanced](sql-injection-training-labs-4.md)
* [Lab 16: Out-of-BandExpert](labs/sql-injection-training-labs-8.md)
* [Lab 17: OOB ExfilExpert](sql-injection-training-labs-10.md)
* [Lab 18: XML BypassExpert](labs/sql-injection-training-labs-2.md)
* [Lab 19: Error BasedAdvanced](labs/sql-injection-training-labs-3.md)

Certification

* Final Exam Complete all labs
* Certificate Pass the exam

[hstucyberknights.top](https://www.hstucyberknights.top/)

***

## Lab 11: Oracle DB Contents

List database contents on Oracle

Advanced

### Objective

Find the users table, enumerate its columns, and extract the administrator credentials.

### Progress

{% stepper %}
{% step %}
### Find tables

Locate relevant tables (for example, a users table) using Oracle metadata views.
{% endstep %}

{% step %}
### Find columns

Enumerate columns for the discovered table to identify which column contains credentials.
{% endstep %}

{% step %}
### Extract credentials

Extract the administrator credentials from the identified columns.
{% endstep %}
{% endstepper %}

### Theory

#### Oracle Metadata Tables

Oracle databases use different metadata views than other databases to enumerate tables and columns.

List all tables:

{% code title="List tables" %}
```sql
SELECT table_name FROM all_tables
```
{% endcode %}

List columns in a table:

{% code title="List columns in USERS table" %}
```sql
SELECT column_name FROM all_tab_columns WHERE table_name='USERS'
```
{% endcode %}

#### Attack Methodology

(Original content provided no further details.)

#### Oracle-Specific Syntax

(Original content provided no further details.)

#### Example Payloads

(Original content provided no specific payloads.)

shop.oracle.local/products

Filter

Wireless Headphones

Electronics

$79.99

Mechanical Keyboard

Electronics

$129.99

USB-C Hub

Electronics

$49.99

<details>

<summary>Need a hint?</summary>

No hint content was provided in the original source.

</details>
