# Signature formatting

Request signature concluded from **MD5** of all passed parameters (names and values), secret-key and today’s date (YYYYMMDD by UTC0).

Order of concatenation is as follows:

1. Partner ID
2. Parameters (only if present)
3. Secret key
4. Date

{% hint style="warning" %}
MD5 signature must be passed in **lowercase**
{% endhint %}

{% tabs %}
{% tab title="Example with no parameters" %}
Base **`URL`** that we are using: **`https://back.staging.splt.eu/partners_reports`**

Partner ID is **`15`** and for others parameters we using default values

Provided secret key is **`4598-8596`**

#### All piece are concatenated into a single string

```
15 + 4598-8596 + 20180813 = 154598-859620180813
```

#### MD5 sum is calculated, that results in

```
f8de1b09af1dafccd072a81899516c69
```

#### Hashed string is then added to the URL

{% code overflow="wrap" %}
```
https://back.staging.splt.eu/partners_reports/15/f8de1b09af1dafccd072a81899516c69
```
{% endcode %}
{% endtab %}

{% tab title="Example with params #1" %}
Base **`URL`** that we are using: **`https://back.staging.splt.eu/partners_reports`**

Partner ID is **`15`**

Provided secret key is **`4598-8596`**

#### Additional parameters

**`from`** – 2018081000 (equates to 2018-08-10 00h).

**`to`** – 2018081223 (equates to 2018-08-12 23h).

**`utc`** – 3 (equates to UTC+3)

#### All piece are concatenated into a single string

```
15 + from + 2018081000 + to + 2018081223 + utc + 3 + 4598-8596 + 20180813 = 15from2018081000to2018081223utc34598-859620180813
```

#### MD5 sum is calculated, that results in

```
7c971bc319c93dda4b9bb37f461e67aa
```

#### Hashed string is then added to the URL

```
https://back.staging.splt.eu/partners_reports/15/7c971bc319c93dda4b9bb37f461e67aa?from=2018081000&to=2018081223&utc=3
```
{% endtab %}

{% tab title="Example with params #2" %}
Base **`URL`** that we are using: **`https://back.staging.splt.eu/partners_reports`**

Partner ID is **`15`**

Provided secret key is **`4598-8596`**

#### Additional parameters

**`from`** – 2018081000 (equates to 2018-08-10 00h).

**`to`** – 2018081223 (equates to 2018-08-12 23h).

**`utc`** – 3 (equates to UTC+3)

**`report_type`** - from 1 to 7

**`report_format`** - JSON, CSV or XML

#### All piece are concatenated into a single string

```
15 + report_type + 7+ from + 2018081000 + to + 2018081223 + report_format + json+ utc + 3 + 4598-8596 + 20180813 = 15report_type7from2018081000to2018081223report_formatjsonutc34598-859620180813
```

#### MD5 sum is calculated, that results in

```
1f8c219292581eeaea83adcb8a0bdfb1
```

#### Hashed string is then added to the URL

```
https://back.staging.splt.eu/partners_reports/15/1f8c219292581eeaea83adcb8a0bdfb1?report_type=7&from=2018081000&to=2018081223&report_format=json&utc=3
```
{% endtab %}
{% endtabs %}





