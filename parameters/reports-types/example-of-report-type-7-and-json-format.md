---
icon: code
---

# Report Type 7 - JSON Format

List of player transactions.

## Request

**Endpoint**: `GET {base_url}/{partner_id}/{signature}?report_type=7&report_format=json&from={from}&to={to}&utc={utc}`

**Example Request**:
```
https://back.staging.splt.eu/partners_reports/15/{signature}?report_type=7&report_format=json&from=20220720000000&to=20220720235959&utc=0
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
            "id": 1,
            "datetime_payout": "2022-07-20 11:23:18",
            "datetime_payin": "2022-07-20 11:23:12",
            "amount": "1.00",
            "amount_payout": "7.50",
            "player": "local",
            "game": "Aquarium"
        },
        {
            "id": 2,
            "datetime_payout": "2022-07-20 11:23:26",
            "datetime_payin": "2022-07-20 11:23:20",
            "amount": "1.00",
            "amount_payout": "5.00",
            "player": "local",
            "game": "Aquarium"
        },
        {
            "id": 3,
            "datetime_payout": "2022-07-20 11:23:33",
            "datetime_payin": "2022-07-20 11:23:27",
            "amount": "1.00",
            "amount_payout": "1.50",
            "player": "local",
            "game": "Aquarium"
        }
    ],
    "parameters": {
        "partner_id": 3,
        "utc": 0,
        "type": 7,
        "from": "20220720000000",
        "to": "20220720235959"
    }
}
```
