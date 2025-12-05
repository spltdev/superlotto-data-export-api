# Additional report parameters

Addition report parameters can be passed as URL parameters.

{% tabs %}
{% tab title="Example:" %}
{% code overflow="wrap" %}
```markup
https://back.staging.splt.eu/partners_reports/15/C6D5D546FD15EAE4FCC24DA4B37B45F7?from=2018081001&to=2018081223&utc=3
```
{% endcode %}
{% endtab %}
{% endtabs %}

<table><thead><tr><th width="183">Parameter name</th><th width="120" align="center">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>from</code></strong></td><td align="center">integer</td><td>Yesterday’s first hour</td><td>Format is <code>YYYYMMDDHH</code>. <br>Parameter <code>from</code> cannot be greater than <code>to</code></td></tr><tr><td><strong><code>to</code></strong></td><td align="center">integer</td><td>Last hour of day from parameter „from“</td><td>Format is <code>YYYYMMDDHH</code>. Maximum <code>from</code> and <code>to</code> range is 31 days.</td></tr><tr><td><strong><code>utc</code></strong></td><td align="center">integer</td><td>0</td><td>Timezone offset (-1, 0, 2, 3...)</td></tr><tr><td><strong><code>report_type</code></strong></td><td align="center">integer</td><td>1</td><td><p>Number of report template.</p><p>Allowed values: 1, 2, 3, 4, 5 (See chapter „Reports types“)</p></td></tr><tr><td><strong><code>report_format</code></strong></td><td align="center">string</td><td>xml</td><td><p>Format of the report. Available formats depend on report type that is chosen.</p><p>All possible values: <code>xml</code>, <code>json</code>, <code>csv</code></p></td></tr></tbody></table>
