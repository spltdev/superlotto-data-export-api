---
icon: play
---

# Getting Started

The **Data Export API** allows partners to retrieve sales and draw reports in various formats (XML, JSON, CSV). The API supports multiple report types, each providing different data views and available formats.

## Endpoint

**Method**: `GET`  
**Format**: Responses are formatted in XML, JSON, or CSV depending on the `report_format` parameter.

### Base URL Format

```
{base_url}/{partner_id}/{signature}?{parameter_name}={value}
```

### Environments

* **Staging**: `https://back.staging.splt.eu/partners_reports`
* **Production**: Provided by Superlotto.tv (unique for each partner)

### Example Request

```
https://back.staging.splt.eu/partners_reports/15/f8de1b09af1dafccd072a81899516c69?from=2018081000&to=2018081223&report_type=1&report_format=xml&utc=3
```

## Authentication

The API uses signature-based authentication. Each request requires an MD5 signature generated from:
- Partner ID
- Request parameters (if present)
- Secret key (provided by Superlotto.tv)
- Today's date (YYYYMMDD in UTC+0)

See the [Signature Formatting](parameters/signature-formatting.md) section for detailed instructions.

## Rate Limits

The API has a limit of **5 requests per minute**. If the limit is exceeded, error code `104` will be returned.

## Report Types

The API supports 8 different report types, each with specific available formats:

| Report Type | Formats | Description |
|------------|---------|-------------|
| `1` | JSON, XML | Sales report, grouped by partner |
| `2` | JSON, XML | Sales report, grouped by game |
| `3` | JSON, XML | TV lotteries draw results |
| `4` | CSV | List of tickets |
| `5` | CSV | List of pay in and pay out transactions |
| `6` | JSON | List of tickets with the tax amount |
| `7` | JSON | List of player transactions |
| `8` | JSON | List of transactions with the clientplatform values |

For detailed examples of each report type, see the [Reports Types](parameters/reports-types/README.md) section.

{% hint style="warning" %}
If a format is not listed for a report type, an error will be returned if it is requested.
{% endhint %}
