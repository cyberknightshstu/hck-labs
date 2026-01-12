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

## Lab 14: Blind SQLi - Time Delays

Cause a 10-second time delay

Advanced

Objective

Cause a 10-second delay in the database response using time-based SQL injection.

### Theory

#### Time-Based Blind SQLi

When neither content nor errors differ, you can use time delays to infer information from the database.

The key insight:

If the query takes longer, the injection worked!

#### Database-Specific Syntax

{% tabs %}
{% tab title="PostgreSQL Sleep" %}
PostgreSQL Sleep
{% endtab %}

{% tab title="MySQL Sleep" %}
MySQL Sleep
{% endtab %}

{% tab title="SQL Server" %}
SQL Server
{% endtab %}
{% endtabs %}

#### Payload Construction

#### Detecting the Database

analytics.example.com

Response Time:

***

TrackingId Cookie:

Send

<details>

<summary>Need a hint?</summary>



</details>
