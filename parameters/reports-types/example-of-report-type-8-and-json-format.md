---
icon: code
---

# Report Type 8 - JSON Format

List of transactions with the clientplatform values.

## Request

**Endpoint**: `GET {base_url}/{partner_id}/{signature}?report_type=8&report_format=json&from={from}&to={to}&utc={utc}`

**Example Request**:
```
https://back.staging.splt.eu/partners_reports/15/{signature}?report_type=8&report_format=json&from=20230607000000&to=20230607235959&utc=0
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
            "id": 961375143,
            "series": "3079",
            "number": "112845573",
            "datetime_payout": "2023-06-07 11:34:01",
            "datetime_payin": "2023-06-07 11:28:45",
            "amount": "50.00",
            "amount_payout": "100.00",
            "player": "test102",
            "game": "Arabeska",
            "clientplatform": "web"
        },
        {
            "id": 961375144,
            "series": "3079",
            "number": "113959417",
            "datetime_payout": "2023-06-07 11:40:05",
            "datetime_payin": "2023-06-07 11:39:59",
            "amount": "50.00",
            "amount_payout": "50.00",
            "player": "test102",
            "game": "Arabeska",
            "clientplatform": "web"
        },
        {
            "id": 961375145,
            "series": "3079",
            "number": "114135575",
            "datetime_payout": "2023-06-07 11:41:41",
            "datetime_payin": "2023-06-07 11:41:35",
            "amount": "20.00",
            "amount_payout": "20.00",
            "player": "test102",
            "game": "Spaceships",
            "clientplatform": "mobile"
        },
        {
            "id": 961375146,
            "series": "3079",
            "number": "114143898",
            "datetime_payout": "2023-06-07 11:41:49",
            "datetime_payin": "2023-06-07 11:41:43",
            "amount": "20.00",
            "amount_payout": "0.00",
            "player": "test102",
            "game": "Spaceships",
            "clientplatform": "mobile"
        },
        {
            "id": 961375147,
            "series": "3079",
            "number": "114242392",
            "datetime_payout": "2023-06-07 11:42:46",
            "datetime_payin": "2023-06-07 11:42:42",
            "amount": "100.00",
            "amount_payout": "0.00",
            "player": "test102",
            "game": "Winter_night",
            "clientplatform": "mobile"
        },
        {
            "id": 961375148,
            "series": "3079",
            "number": "114248430",
            "datetime_payout": "2023-06-07 11:42:51",
            "datetime_payin": "2023-06-07 11:42:48",
            "amount": "100.00",
            "amount_payout": "0.00",
            "player": "test102",
            "game": "Winter_night",
            "clientplatform": "mobile"
        },
        {
            "id": 961375149,
            "series": "3079",
            "number": "114254710",
            "datetime_payout": "2023-06-07 11:48:00",
            "datetime_payin": "2023-06-07 11:42:54",
            "amount": "100.00",
            "amount_payout": "100.00",
            "player": "test102",
            "game": "Winter_night",
            "clientplatform": "mobile"
        },
        {
            "id": 961375150,
            "series": "3079",
            "number": "122013843",
            "datetime_payout": "2023-06-07 12:20:17",
            "datetime_payin": "2023-06-07 12:20:13",
            "amount": "50.00",
            "amount_payout": "0.00",
            "player": "test102",
            "game": "5x",
            "clientplatform": "mobile"
        }
    ],
    "parameters": {
        "partner_id": 169,
        "utc": 0,
        "type": 8,
        "from": "20230607000000",
        "to": "20230607235959"
    }
}
```
