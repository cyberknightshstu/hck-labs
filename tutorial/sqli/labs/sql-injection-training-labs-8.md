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

## Lab 16: Out-of-Band Interaction

Trigger DNS lookup to external server

Level: Expert

### Objective

Trigger a DNS lookup to Burp Collaborator using out-of-band SQL injection.

Burp Collaborator Domain:

```
abcd1234.burpcollaborator.net
```

### Theory

#### Out-of-Band SQL Injection

When the query is executed asynchronously and has no visible effect, you can trigger out-of-band interactions with external systems.

Key requirement:

* Need an external server to receive the DNS/HTTP request

#### Burp Collaborator

#### Oracle OOB Techniques

#### Other Database Techniques

### Burp Collaborator Client

DNS Interactions:

No interactions recorded yet...

vulnerable-app.oracle.local

TrackingId Cookie:

Send

Oracle XXEOracle UTL\_INADDR

{% hint style="info" %}
Need a hint?
{% endhint %}
