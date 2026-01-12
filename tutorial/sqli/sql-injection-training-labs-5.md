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

## Lab 7: UNION Attack - Multiple Values

Retrieve multiple values in a single column using concatenation

Intermediate

### Objective

Only one column displays text. Use string concatenation to retrieve both username and password, then login as administrator.

### Theory

#### The Single Column Challenge

Sometimes you'll find that **only one column** in the query accepts text data. This creates a problem: how do you extract _two_ values (username AND password) when you only have one column to work with?

**Challenge:** In this lab, column 1 is INTEGER-only. Only column 2 accepts text. You need both username and password!

#### String Concatenation

#### The Attack Steps

#### Attack Strategy

{% stepper %}
{% step %}
Find column count (2 columns)
{% endstep %}

{% step %}
Find text column (column 2)
{% endstep %}

{% step %}
Use version() to detect DB
{% endstep %}

{% step %}
Concatenate username||password
{% endstep %}

{% step %}
Login as administrator
{% endstep %}
{% endstepper %}

Need more help?

<details>

<summary>Query Log</summary>

No queries executed yet...

</details>

#### Admin Login

Login

#### 🏃 SportGear - Product Catalog

Filter

GET /products?category=Sports
