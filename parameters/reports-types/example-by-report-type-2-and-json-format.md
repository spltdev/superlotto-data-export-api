---
icon: code
---

# Report Type 2 - JSON Format

Sales report grouped by game.

## Request

**Endpoint**: `GET {base_url}/{partner_id}/{signature}?report_type=2&report_format=json&from={from}&to={to}&utc={utc}`

**Example Request**:
```
https://back.staging.splt.eu/partners_reports/15/{signature}?report_type=2&report_format=json&from=201808130000&to=20180813235959&utc=0
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
            "turnover_count": "2",
            "payouts_count": "1",
            "returns_count": "0",
            "payouts_large_count": "0",
            "game": "5 from 36",
            "currency": "eur",
            "completed": 1,
            "turnover": "2.00",
            "payouts": "2.00",
            "returns": "0.00",
            "payouts_large": "0.00"
        },
        {
            "turnover_count": "2",
            "payouts_count": "0",
            "returns_count": "0",
            "payouts_large_count": "0",
            "game": "7 from 42",
            "currency": "eur",
            "completed": 1,
            "turnover": "2.00",
            "payouts": "0.00",
            "returns": "0.00",
            "payouts_large": "0.00"
        },
        {
            "turnover_count": "61352",
            "payouts_count": "1406",
            "returns_count": "3212",
            "payouts_large_count": "0",
            "game": "interjackpot",
            "currency": "eur",
            "completed": 0,
            "turnover": "122704.00",
            "payouts": "144389.76",
            "returns": "6424.00",
            "payouts_large": "0.00"
        }
    ],
    "parameters": {
        "partner_id": 3,
        "utc": 0,
        "type": "2",
        "from": "201808130000",
        "to": "20180813235959"
    }
}
```
