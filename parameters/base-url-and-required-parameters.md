# Base URL and required parameters

Default URL format is:

```
{base_url}/{partner_id}/{signature}?{parameter_name}={value}
```

{% hint style="info" %}
Endpoint accepts **GET** method requests only
{% endhint %}

{% hint style="info" %}
&#x20;Endpoint has a limit of **5 requests** per minute
{% endhint %}

<table><thead><tr><th width="185">Parameter</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>base_url</code></strong></td><td>URL, given by Superlotto.tv</td></tr><tr><td><strong><code>partner_id</code></strong></td><td>partner ID in Superlotto.tv system</td></tr><tr><td><strong><code>signature</code></strong></td><td>md5 checksum from sent parameters names, values, secret-key (given by Superlotto.tv) and today’s date (YYYYMMDD by UTC0)</td></tr></tbody></table>

