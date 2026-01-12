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

## Lab 5: UNION Attack - Text Column

Find which column accepts text data

Difficulty: Beginner

### Objective

The query returns 3 columns. Find which column accepts text and make this string appear:

`h4Ck3rM4n`

### Theory

#### Why Data Types Matter

After determining the number of columns in a query, the next step is to find which columns can hold **string/text data**. This is crucial because when extracting data like usernames or passwords, you need to output them in columns that accept text.

The UNION operator requires compatible data types between queries:

* An INTEGER column cannot display a STRING value
* A STRING column can display text data you want to extract
* If data types don't match, the database returns an error

#### The Probing Technique

To identify which columns accept text, inject payloads using UNION with string values placed into each column position. Columns that accept string values will not produce a type-mismatch error and will display the injected text.

### Step-by-Step Process

#### Attack Strategy

{% stepper %}
{% step %}
### Confirm there are 3 columns

Determine the number of columns returned by the original query (already known here: 3).
{% endstep %}

{% step %}
### Test string in each column

Inject test strings into each column position (one at a time or in combinations) using UNION to see which column(s) accept string data.
{% endstep %}

{% step %}
### Identify which column doesn't error

Observe responses/errors. The column that displays the injected string (or doesn't error) is a string-capable column.
{% endstep %}

{% step %}
### Inject the target string

Once identified, inject the target string into that column so it appears in the query output:

`h4Ck3rM4n`
{% endstep %}
{% endstepper %}

### Need more help?

<details>

<summary>Click for hints</summary>

* Try payloads such as: `UNION SELECT 'a', NULL, NULL` (and variants placing the string in each position).
* Use NULL placeholders to preserve column count while testing data types.
* If the application sanitizes quotes, try alternate encodings or concatenation techniques appropriate to the database.

</details>

### Query Log

No queries executed yet...

***

#### 🛒 ShopZone - Product Catalog

Filter

GET /products?category=Gifts

Click "Filter" to search products...
