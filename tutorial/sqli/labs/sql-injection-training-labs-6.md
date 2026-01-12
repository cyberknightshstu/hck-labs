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

Site: https://www.hstucyberknights.top/

***

## Lab 1: Authentication Bypass

Exploit a vulnerable login form

Difficulty: Beginner

Objective

* Bypass authentication and login as `admin` without knowing the password.

### Theory

#### What is SQL Injection?

SQL injection is a vulnerability where an attacker interferes with SQL queries by injecting malicious SQL code through user inputs.

Example — normal query:

```sql
SELECT * FROM users WHERE username = 'admin' AND password = 'secret'
```

With injection (e.g., `admin'--`):

```sql
SELECT * FROM users WHERE username = 'admin'--' AND password = 'x'
```

The `--` comments out the password check, allowing bypass.

### How Authentication Bypass Works

Authentication bypass abuses input that is inserted into SQL queries without proper sanitization or parameterization. By crafting an input that changes the logic of the WHERE clause (for example making it always true or truncating the rest of the query via comment syntax), an attacker can bypass credentials checks.

Common techniques include:

* Injecting tautologies (e.g., `' OR '1'='1`)
* Injecting comment sequences to ignore the remainder of the query (e.g., `--`)
* Exploiting numeric comparisons where quotes are not used (e.g., `OR 1=1`)

### Practice (vulnerable\_login.php)

Use the vulnerable login form to test payloads against the application.

Fields:

* Username
* Password

Actions:

* Execute — submit the login attempt and observe results
* query\_output — view query result/feedback (if provided by the lab)



### Quick Payloads

Try these payloads in the username field (or where applicable) to bypass authentication:

```
admin'--
```

Comment out the rest of the query to skip password check.

```
' OR '1'='1
```

Tautology that evaluates to true.

```
' OR 1=1--
```

Numeric tautology with comment to ignore remainder.

```
{% endstep %}
{% endstepper %}

Need to track progress or login: https://sqli.lab.hstucyberknights.top/auth

<details>
<summary>Need a hint?</summary>

If the application builds a SQL query by concatenating your input directly into the WHERE clause, try modifying your input so the WHERE clause always evaluates to true (e.g., inject a tautology) or so the remainder of the query is commented out.

Examples to test in the username field:
- `admin'--`  (if you want to attempt directly logging in as admin)
- `' OR '1'='1` (generic bypass)
- `' OR 1=1--` (numeric variant with comment)
</details>
```
