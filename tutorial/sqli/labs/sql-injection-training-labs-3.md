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

## Lab 19: Visible Error-Based SQLi

Extract data from verbose error messages

Difficulty: Advanced

Objective

Leak the administrator password through verbose database error messages.

### Theory

#### Visible Error-Based SQLi

Some applications display verbose database errors that can leak sensitive information directly in the error message.

Error message reveals:

`invalid input syntax for type integer: "secret_password"`

#### CAST Function Trick

(Section present in original content.)

#### Attack Methodology

(Section present in original content.)

#### Handling Truncation

(Section present in original content.)

analytics.vulnerable-app.com

Request processed successfully

TrackingId Cookie:

Send

Test ErrorLeak UsernameLeak Password

{% hint style="info" %}
Need a hint?
{% endhint %}
