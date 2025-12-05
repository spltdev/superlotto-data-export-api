---
icon: code
---

# Report Type 4 - CSV Format

List of tickets.

## Request

**Endpoint**: `GET {base_url}/{partner_id}/{signature}?report_type=4&report_format=csv&from={from}&to={to}&utc={utc}`

**Example Request**:
```
https://back.staging.splt.eu/partners_reports/15/{signature}?report_type=4&report_format=csv&from=201904100000&to=201904102359&utc=0
```

{% hint style="info" %}
Replace `{signature}` with the MD5 hash generated from your parameters. See [Signature Formatting](../signature-formatting.md) for details.
{% endhint %}

## Response

```csv
id;datetime_payin;status;amount;code
3541753;2019-04-10 17:28:51;payed_out;0.10;eur
3541756;2019-04-10 17:29:07;payed_out;0.10;eur
3541757;2019-04-10 17:29:07;payed_out;0.10;eur
3542217;2019-04-10 17:49:49;payed_out;0.10;eur
3542218;2019-04-10 17:49:49;payed_out;0.10;eur
3542243;2019-04-10 17:52:16;payed_out;0.10;eur
3542244;2019-04-10 17:52:16;payed_out;0.10;eur
```
