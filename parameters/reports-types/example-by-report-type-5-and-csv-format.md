---
icon: code
---

# Report Type 5 - CSV Format

List of pay in and pay out transactions.

## Request

**Endpoint**: `GET {base_url}/{partner_id}/{signature}?report_type=5&report_format=csv&from={from}&to={to}&utc={utc}`

**Example Request**:
```
https://back.staging.splt.eu/partners_reports/15/{signature}?report_type=5&report_format=csv&from=201904100000&to=201904102359&utc=0
```

{% hint style="info" %}
Replace `{signature}` with the MD5 hash generated from your parameters. See [Signature Formatting](../signature-formatting.md) for details.
{% endhint %}

## Response

```csv
id;datetime;type;amount;currency;player_code
3541753;2019-04-10 17:28:51;payed_in;0.10;eur;5251
3541753;2019-04-10 17:31:48;payed_in;2;eur;5251
3541754;2019-04-10 17:33:21;payed_in;1;eur;5874
3541755;2019-04-10 17:34:49;payed_in;2;eur;4001
3541754;2019-04-10 17:36:21;payed_in;0;eur;5874
```
