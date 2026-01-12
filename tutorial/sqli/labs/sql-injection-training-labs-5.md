# SQL Injection Training Labs

## HSTU CyberKnights

SQLi Training Labs

* Dashboard: https://sqli.lab.hstucyberknights.top/

Labs

* Lab 1: Auth Bypass — Beginner\
  https://sqli.lab.hstucyberknights.top/labs/basic-auth-bypass
* Lab 2: Hidden Data — Beginner\
  https://sqli.lab.hstucyberknights.top/labs/hidden-data-retrieval
* Lab 3: Login Bypass — Beginner\
  https://sqli.lab.hstucyberknights.top/labs/login-bypass
* Lab 4: UNION Columns — Beginner\
  https://sqli.lab.hstucyberknights.top/labs/union-column-count
* Lab 5: Text Column — Beginner\
  https://sqli.lab.hstucyberknights.top/labs/union-text-column
* Lab 6: Data Retrieval — Intermediate\
  https://sqli.lab.hstucyberknights.top/labs/union-data-retrieval
* Lab 7: Multi Values — Intermediate\
  https://sqli.lab.hstucyberknights.top/labs/union-multiple-values
* Lab 8: Oracle Version — Intermediate\
  https://sqli.lab.hstucyberknights.top/labs/oracle-db-version
* Lab 9: MySQL Version — Intermediate\
  https://sqli.lab.hstucyberknights.top/labs/mysql-db-version
* Lab 10: DB Contents — Advanced\
  https://sqli.lab.hstucyberknights.top/labs/database-contents
* Lab 11: Oracle Contents — Advanced\
  https://sqli.lab.hstucyberknights.top/labs/oracle-db-contents
* Lab 12: Blind Responses — Advanced\
  https://sqli.lab.hstucyberknights.top/labs/blind-conditional-responses
* Lab 13: Blind Errors — Advanced\
  https://sqli.lab.hstucyberknights.top/labs/blind-conditional-errors
* Lab 14: Time Delays — Advanced\
  https://sqli.lab.hstucyberknights.top/labs/blind-time-delays
* Lab 15: Time Retrieval — Advanced\
  https://sqli.lab.hstucyberknights.top/labs/blind-time-retrieval
* Lab 16: Out-of-Band — Expert\
  https://sqli.lab.hstucyberknights.top/labs/blind-out-of-band
* Lab 17: OOB Exfil — Expert\
  https://sqli.lab.hstucyberknights.top/labs/blind-out-of-band-exfil
* Lab 18: XML Bypass — Expert\
  https://sqli.lab.hstucyberknights.top/labs/xml-encoding-bypass
* Lab 19: Error Based — Advanced\
  https://sqli.lab.hstucyberknights.top/labs/visible-error-based

Certification

* Final Exam: Complete all labs
* Certificate: Pass the exam

https://www.hstucyberknights.top/

### Theory

#### Oracle Database Specifics

#### Why DUAL Table?

#### Extracting Database Version

#### Attack Strategy

**Query Log**

<details>

<summary>Query Log (expand)</summary>

No queries executed yet...

</details>

## Lab 8: Oracle DB Version

Query database type and version on Oracle

Difficulty: Intermediate

Target: CyberShop - Oracle Edition

Database: Oracle DB

Filter by Category:

Filter

URL: /products?category=...

{% hint style="info" %}
Hints

* Oracle requires a FROM clause in every SELECT.
* Use the DUAL table for UNION attacks on Oracle.
* The v$version view contains version information.
* The banner column contains the version string.
{% endhint %}
