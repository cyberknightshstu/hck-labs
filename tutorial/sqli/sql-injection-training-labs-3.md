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

### Theory

#### Information Schema

{% stepper %}
{% step %}
### Enumerate Tables

Use the information schema to discover tables in the database.
{% endstep %}

{% step %}
### Find Column Names

Once tables are known, enumerate columns to find relevant fields (e.g., usernames, passwords).
{% endstep %}

{% step %}
### Extract Data

After locating tables and columns, extract the desired data from the identified columns.
{% endstep %}
{% endstepper %}

#### Attack Strategy

**Query Log**

No queries executed yet...

## Lab 10: Database Contents

Listing database contents on non-Oracle

Advanced

Admin Login

Login

CyberShop - PostgreSQL

PostgreSQL

Filter by Category:

Filter

**Hints**

{% hint style="info" %}
* Use `information_schema.tables` to list tables
* Use `information_schema.columns` to list columns
* Table names may have random suffixes
* Column names may not be obvious (e.g., `username_col`, `password_col`)
* Login as administrator to complete the lab
{% endhint %}
