---
icon: code
---

# Additional Report Parameters

Additional report parameters can be passed as URL query parameters. All parameters are optional and have default values.

## Example Request

```
https://back.staging.splt.eu/partners_reports/15/C6D5D546FD15EAE4FCC24DA4B37B45F7?from=2018081001&to=2018081223&utc=3&report_type=1&report_format=xml
```

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `from` | integer | Yesterday's first hour | Start date and time in `YYYYMMDDHH` format. Parameter `from` cannot be greater than `to`. |
| `to` | integer | Last hour of day from parameter `from` | End date and time in `YYYYMMDDHH` format. Maximum `from` and `to` range is **31 days**. |
| `utc` | integer | 0 | Timezone offset in hours (e.g., -1, 0, 2, 3). |
| `report_type` | integer | 1 | Report template number. Allowed values: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. See [Reports Types](reports-types/README.md) for details. |
| `report_format` | string | xml | Format of the report. Available formats depend on the selected report type. All possible values: `xml`, `json`, `csv`. |

## Date Format

Both `from` and `to` parameters use the format `YYYYMMDDHH`:
- `YYYY` - 4-digit year
- `MM` - 2-digit month (01-12)
- `DD` - 2-digit day (01-31)
- `HH` - 2-digit hour (00-23)

**Example**: `2018081001` represents August 10, 2018 at 01:00 (1 AM).

## Date Range Rules

* The `from` parameter cannot be greater than the `to` parameter
* Maximum date range between `from` and `to` is **31 days**
* If the range exceeds 31 days, error code `105` will be returned

{% hint style="info" %}
If `from` and `to` are not specified, the API will return data for yesterday by default.
{% endhint %}
