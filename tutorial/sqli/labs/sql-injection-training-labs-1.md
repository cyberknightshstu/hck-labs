# SQL Injection Training Labs

## HSTU CyberKnights

SQLi Training Labs

* [Dashboard](https://sqli.lab.hstucyberknights.top/)

Labs

* [Lab 1: Auth BypassBeginner](sql-injection-training-labs-6.md)
* [Lab 2: Hidden DataBeginner](../sql-injection-training-labs-6.md)
* [Lab 3: Login BypassBeginner](../sql-injection-training-labs-9.md)
* [Lab 4: UNION ColumnsBeginner](sql-injection-training-labs-4.md)
* [Lab 5: Text ColumnBeginner](sql-injection-training-labs-7.md)
* [Lab 6: Data RetrievalIntermediate](sql-injection-training-labs-1.md)
* [Lab 7: Multi ValuesIntermediate](../sql-injection-training-labs-5.md)
* [Lab 8: Oracle VersionIntermediate](sql-injection-training-labs-5.md)
* [Lab 9: MySQL VersionIntermediate](sql-injection-training-labs.md)
* [Lab 10: DB ContentsAdvanced](../sql-injection-training-labs-3.md)
* [Lab 11: Oracle ContentsAdvanced](../sql-injection-training-labs-11.md)
* [Lab 12: Blind ResponsesAdvanced](../sql-injection-training-labs-8.md)
* [Lab 13: Blind ErrorsAdvanced](../sql-injection-training-labs-7.md)
* [Lab 14: Time DelaysAdvanced](../sql-injection-training-labs-2.md)
* [Lab 15: Time RetrievalAdvanced](../sql-injection-training-labs-4.md)
* [Lab 16: Out-of-BandExpert](sql-injection-training-labs-8.md)
* [Lab 17: OOB ExfilExpert](../sql-injection-training-labs-10.md)
* [Lab 18: XML BypassExpert](sql-injection-training-labs-2.md)
* [Lab 19: Error BasedAdvanced](sql-injection-training-labs-3.md)

Certification

* Final Exam Complete all labs
* Certificate Pass the exam

[hstucyberknights.top](https://www.hstucyberknights.top/)

***

## Lab 6: UNION Attack - Data Retrieval

Extract usernames and passwords from other tables

Difficulty: Intermediate

Objective

{% hint style="info" %}
The database has a `users` table with columns `username` and `password`. Extract the credentials and login as administrator.
{% endhint %}

### Theory

#### Retrieving Data from Other Tables

Once you've confirmed a UNION injection works, you can use it to extract data from other tables in the database. The key is knowing:

* The table name (e.g., `users`)
* The column names (e.g., `username`, `password`)
* The number of columns must match the original query

#### The Attack Technique

Use a successful UNION injection to return rows from another table by matching column count and compatible column types, then selecting the desired columns (for example, `username` and `password`).

### Attack Strategy

{% stepper %}
{% step %}
### Confirm there are 2 columns

Determine the number of columns the original query returns (in this lab, confirm 2).
{% endstep %}

{% step %}
### Use UNION SELECT with users table

Craft a UNION SELECT that retrieves `username` and `password` from the `users` table, ensuring the column count and types align with the original query.
{% endstep %}

{% step %}
### Extract username and password

Run the UNION payload to return rows containing usernames and passwords from the `users` table.
{% endstep %}

{% step %}
### Login as administrator

Use the extracted administrator credentials to authenticate as the administrator.
{% endstep %}
{% endstepper %}

Need more help?

<details>

<summary>Additional assistance</summary>

If you need more hints or walkthroughs, refer to the lab UI or other training materials provided by the platform.

</details>

#### Query Log

<details>

<summary>Executed queries</summary>

No queries executed yet...

</details>

#### Admin Login

Login

***

#### 🛒 ShopZone - Product Catalog

Filter

GET /products?category=Gifts
