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

## Lab 3: Login Bypass

Login as administrator via SQL injection

Difficulty: Beginner

### Objective

Perform a SQL injection attack that logs in as the `administrator` user.

Important: The username must be "administrator" — this is the account we're targeting.

### Theory

#### Lab Overview

This lab contains a SQL injection vulnerability in the login functionality. Your goal is to log in as the `administrator` user without knowing the password.

#### Understanding the Vulnerability

(Section left intentionally for hands-on exploration and testing of the login form to discover how inputs are used in SQL queries.)

#### Testing for SQLi

(Use typical SQLi probes against the login form to observe behavior and error messages, then craft payloads to bypass authentication.)

#### The Exploit

(Exploit involves manipulating the username/password inputs to alter the SQL logic so that the application authenticates as the administrator.)

#### Prevention

(Defensive guidance: use prepared statements/parameterized queries, input validation, least privilege for DB accounts, and proper error handling.)

***

shop\_login.php

Username

Password

Login

Enter credentials and click Login to see results

<details>

<summary>Need a hint?</summary>

Try testing how the login form behaves with SQL special characters and boolean-changing payloads. The target account is exactly "administrator".

</details>

<details>

<summary>query_output</summary>

The application will display results after you submit credentials. Use that feedback to refine injections.

</details>
