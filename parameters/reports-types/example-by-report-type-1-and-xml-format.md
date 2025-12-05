---
icon: code
---

# Report Type 1 - XML Format

Sales report grouped by partner.

## Request

**Endpoint**: `GET {base_url}/{partner_id}/{signature}?report_type=1&report_format=xml&from={from}&to={to}&utc={utc}`

**Example Request**:
```
https://back.staging.splt.eu/partners_reports/15/{signature}?report_type=1&report_format=xml&from=201808130000&to=20180813235959&utc=0
```

{% hint style="info" %}
Replace `{signature}` with the MD5 hash generated from your parameters. See [Signature Formatting](../signature-formatting.md) for details.
{% endhint %}

## Response

{% code lineNumbers="true" %}
```xml
<report>
    <status>
        <success>1</success>
        <info>ok</info>
        <code>100</code>
    </status>
    <parameters>
        <partner>3</partner>
        <from>201808130000</from>
        <to>20180813235959</to>
        <type>1</type>
        <utc>0</utc>
    </parameters>
    <entries>
        <entry>
            <currency>eur</currency>
            <completed>0</completed>
            <sums>
                <turnover>120710.00</turnover>
                <payouts>142990.74</payouts>
                <returns>6424.00</returns>
                <payouts-large>0.00</payouts-large>
            </sums>
            <counts>
                <turnover>60357</turnover>
                <payouts>1388</payouts>
                <returns>3212</returns>
                <payouts-large>0</payouts-large>
            </counts>
        </entry>
    </entries>
</report>
```
{% endcode %}
