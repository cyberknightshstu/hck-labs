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

## Lab 2: Hidden Data Retrieval

Bypass WHERE clause filter to see hidden products

Difficulty: Beginner

### Objective

Exploit the SQL injection vulnerability to display ALL products, including **unreleased/hidden** ones.

### Theory

#### The Vulnerability

This lab simulates a product filtering system vulnerable to SQL injection in the WHERE clause category filter.

Backend query:

{% code title="shop_filter.php" %}
```sql
SELECT * FROM products
WHERE category = '[USER INPUT]'
AND released = 1
```
{% endcode %}

The `released = 1` filter hides unreleased products. Your goal is to bypass this filter!

#### Attack Methodology

(Section placeholder — original content provided no further details.)

#### Useful Payloads

(Section placeholder — original content provided no further details.)

#### Real-World Impact

(Section placeholder — original content provided no further details.)

### Context (UI Fields / Inputs)

* shop\_filter.php
* Page displays categories: AllElectronicsSportsBooks
* Category Filter (URL parameter): ?category=
* Filter Products (UI control)
* query\_output (results area)
* Message shown: "Select a category or enter a filter to query products"

{% hint style="info" %}
Need a hint?
{% endhint %}

<details>

<summary>Additional information / UI notes</summary>

* The category value is used directly in the WHERE clause.
* The `released = 1` condition is appended server-side and is intended to hide unreleased products.
* Your task is to craft input that bypasses or neutralizes that condition so the query returns all rows.

</details>
