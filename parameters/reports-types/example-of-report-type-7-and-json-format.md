# Example of report type 7 and JSON format

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
