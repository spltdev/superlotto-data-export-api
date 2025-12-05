---
icon: code
---

# Report Type 6 - JSON Format

List of tickets with the tax amount.

{% hint style="info" %}
`tax_amount` represents only the tax and `amount_payout` includes both tax amount and the actual payed out winning.
{% endhint %}

## Request

**Endpoint**: `GET {base_url}/{partner_id}/{signature}?report_type=6&report_format=json&from={from}&to={to}&utc={utc}`

**Example Request**:
```
https://back.staging.splt.eu/partners_reports/15/{signature}?report_type=6&report_format=json&from=20240115000000&to=20240115235959&utc=0
```

{% hint style="info" %}
Replace `{signature}` with the MD5 hash generated from your parameters. See [Signature Formatting](../signature-formatting.md) for details.
{% endhint %}

## Response

```json
{
  "status": {
    "success": true,
    "code": 100,
    "info": "ok"
  },
  "entries": [
    {
      "id": 900000001,
      "series": "2402",
      "number": "1000000001-100-01",
      "datetime_payout": "2024-01-15 06:06:06",
      "datetime_payin": "2024-01-15 06:04:03",
      "amount": "98.00",
      "amount_payout": "54.00",
      "tax_amount": "10"
    },
    {
      "id": 900000003,
      "series": "2402",
      "number": "1000000003-100-01",
      "datetime_payout": "2024-01-15 06:09:26",
      "datetime_payin": "2024-01-15 06:04:03",
      "amount": "98.00",
      "amount_payout": "66.00",
      "tax_amount": "5"
    }
  ],
  "parameters": {
    "partner_id": 3,
    "utc": 0,
    "type": "6",
    "from": "20240115000000",
    "to": "20240115235959"
  }
}
```
