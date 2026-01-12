# SQL Injection Training Labs

## HSTU CyberKnights — SQLi Training Labs

Dashboard: https://sqli.lab.hstucyberknights.top/

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

* Final Exam — Complete all labs
* Certificate — Pass the exam

Website: https://www.hstucyberknights.top/

***

## Lab 12: Blind SQLi — Conditional Responses

Extract data using page content differences

Difficulty: Advanced

### Objective

Exploit blind SQLi in the tracking cookie to extract the administrator password (20 chars).

### Extracted Password:

0/20 characters

### Theory

#### What is Blind SQL Injection?

Blind SQL injection occurs when an application is vulnerable but doesn't return query results or error messages directly.

Instead, you detect differences in:

* Page content (conditional responses)
* Response time (time-based)
* Error states

#### Conditional Responses

(Use differences in returned page content to infer boolean conditions about the database.)

#### Character Enumeration

(Iteratively test characters of the target string by constructing boolean conditions and observing content differences.)

#### Password Length Detection

(Determine the length of the target string first by testing equality/greater-than conditions.)

shop.example.com — Welcome back!

TrackingId Cookie:

Send

Test True Test False Check Users

### Need a hint?

<details>

<summary>Show hint</summary>

Try crafting payloads that cause the page to display different content when a condition about the administrator's password is true vs false. For example, use boolean expressions in the TrackingId cookie to check characters at specific positions and observe which requests return the "true" content.

</details>
