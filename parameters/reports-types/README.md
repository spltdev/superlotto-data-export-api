---
icon: list
---

# Report Types

The Data Export API supports 8 different report types, each providing different data views and available formats.

{% hint style="warning" %}
If a format is not listed for a report type, an error code `107` (incorrect_format) will be returned if it is requested.
{% endhint %}

## Available Report Types

| Report Type | Formats | Description |
|-------------|---------|-------------|
| `1` | JSON, XML | Sales report, grouped by partner |
| `2` | JSON, XML | Sales report, grouped by game |
| `3` | JSON, XML | TV lotteries draw results |
| `4` | CSV | List of tickets |
| `5` | CSV | List of pay in and pay out transactions |
| `6` | JSON | List of tickets with the tax amount |
| `7` | JSON | List of player transactions |
| `8` | JSON | List of transactions with the clientplatform values |

## Format Availability

* **JSON**: Available for report types 1, 2, 3, 6, 7, 8
* **XML**: Available for report types 1, 2, 3
* **CSV**: Available for report types 4, 5

## Examples

For detailed examples of each report type and format, see the individual example files:

* [Report Type 1 - XML Format](example-by-report-type-1-and-xml-format.md)
* [Report Type 2 - JSON Format](example-by-report-type-2-and-json-format.md)
* [Report Type 3 - XML Format](example-by-report-type-3-and-xml-format.md)
* [Report Type 4 - CSV Format](example-by-report-type-4-and-csv-format.md)
* [Report Type 5 - CSV Format](example-by-report-type-5-and-csv-format.md)
* [Report Type 6 - JSON Format](example-of-report-type-6-and-json-format.md)
* [Report Type 7 - JSON Format](example-of-report-type-7-and-json-format.md)
* [Report Type 8 - JSON Format](example-of-report-type-8-and-json-format.md)

