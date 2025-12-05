# Example of report type 1 and XML format

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
