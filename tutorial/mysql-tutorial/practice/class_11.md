# class\_11

## LIKE examples — wildcards and patterns

* % matches any sequence of zero or more characters
* \_ matches a single character
* \[chars] matches any single character in the listed set or range
* NOT IN / IN / subqueries examples are shown below

{% code title="Match single characters with _ (underscore)" %}
```
```
{% endcode %}

{% code title="Match any city containing " %}
```
```
{% endcode %}

{% code title="Match CustomerName starting with " %}
```
```
{% endcode %}

{% code title="Match CustomerName starting with " %}
```
```
{% endcode %}

{% code title="Match CustomerName ending with " %}
```
```
{% endcode %}

{% code title="Match CustomerName starting with " %}
```
```
{% endcode %}

{% code title="Match CustomerName containing " %}
```
```
{% endcode %}

{% code title="Match CustomerName starting with " %}
```
```
{% endcode %}

{% code title="Match CustomerName with second letter " %}
```
```
{% endcode %}

{% code title="Match Country exactly equal to " %}
```
```
{% endcode %}

## LIKE examples — character lists and ranges

{% code title="Character list: match names starting with b, s or p" %}
```
```
{% endcode %}

{% code title="Character range: match names starting with letters a to f" %}
```
```
{% endcode %}

## IN / NOT IN and subqueries

{% code title="Exclude specific countries" %}
```
```
{% endcode %}

{% code title="Customers that have orders (using IN with subquery)" %}
```
```
{% endcode %}

{% code title="Customers that do not have orders (using NOT IN with subquery)" %}
```
```
{% endcode %}
