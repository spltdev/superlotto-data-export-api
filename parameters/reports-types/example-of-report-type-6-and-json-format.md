# Example of report type 6 and JSON format

`tax_amount` represents only the tax and `amount_payout` includes both tax amount and the actual payed out winning.

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
