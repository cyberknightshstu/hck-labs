# SQL Injection Training Labs

## HSTU CyberKnights

SQLi Training Labs

* Dashboard: https://sqli.lab.hstucyberknights.top/

Labs

* Lab 1: Auth BypassBeginner — https://sqli.lab.hstucyberknights.top/labs/basic-auth-bypass
* Lab 2: Hidden DataBeginner — https://sqli.lab.hstucyberknights.top/labs/hidden-data-retrieval
* Lab 3: Login BypassBeginner — https://sqli.lab.hstucyberknights.top/labs/login-bypass
* Lab 4: UNION ColumnsBeginner — https://sqli.lab.hstucyberknights.top/labs/union-column-count
* Lab 5: Text ColumnBeginner — https://sqli.lab.hstucyberknights.top/labs/union-text-column
* Lab 6: Data RetrievalIntermediate — https://sqli.lab.hstucyberknights.top/labs/union-data-retrieval
* Lab 7: Multi ValuesIntermediate — https://sqli.lab.hstucyberknights.top/labs/union-multiple-values
* Lab 8: Oracle VersionIntermediate — https://sqli.lab.hstucyberknights.top/labs/oracle-db-version
* Lab 9: MySQL VersionIntermediate — https://sqli.lab.hstucyberknights.top/labs/mysql-db-version
* Lab 10: DB ContentsAdvanced — https://sqli.lab.hstucyberknights.top/labs/database-contents
* Lab 11: Oracle ContentsAdvanced — https://sqli.lab.hstucyberknights.top/labs/oracle-db-contents
* Lab 12: Blind ResponsesAdvanced — https://sqli.lab.hstucyberknights.top/labs/blind-conditional-responses
* Lab 13: Blind ErrorsAdvanced — https://sqli.lab.hstucyberknights.top/labs/blind-conditional-errors
* Lab 14: Time DelaysAdvanced — https://sqli.lab.hstucyberknights.top/labs/blind-time-delays
* Lab 15: Time RetrievalAdvanced — https://sqli.lab.hstucyberknights.top/labs/blind-time-retrieval
* Lab 16: Out-of-BandExpert — https://sqli.lab.hstucyberknights.top/labs/blind-out-of-band
* Lab 17: OOB ExfilExpert — https://sqli.lab.hstucyberknights.top/labs/blind-out-of-band-exfil
* Lab 18: XML BypassExpert — https://sqli.lab.hstucyberknights.top/labs/xml-encoding-bypass
* Lab 19: Error BasedAdvanced — https://sqli.lab.hstucyberknights.top/labs/visible-error-based

Certification

* Final Exam: Complete all labs
* Certificate: Pass the exam

Website: https://www.hstucyberknights.top/

***

## Lab 18: XML Encoding WAF Bypass

Bypass WAF using XML hex entities

Difficulty: Expert

Objective

Bypass the WAF and extract admin credentials using XML encoding.

### Theory

#### Web Application Firewall Bypass

WAFs detect SQL injection by pattern matching. Encoding can bypass these filters while the backend still processes the payload.

Blocked example:

```
1 UNION SELECT NULL
```

Bypassed example (encoded):

```
1 UNION SELECT NULL
```

#### XML Context

#### Using Hackverter

#### Single Column Extraction

Product: Premium Widget$49.99

Check Stock (XML API)

Product ID:

Store ID:

Check Stock

Quick Payloads:

* Plain UNION (blocked)
* Encoded UNION
* Extract Users

<details>

<summary>Need a hint?</summary>

Need a hint?

</details>
