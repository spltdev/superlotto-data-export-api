---
icon: code
---

# Base URL and Required Parameters

## Endpoint

**Method**: `GET`  
**URL Format**: `{base_url}/{partner_id}/{signature}?{parameter_name}={value}`

### Environments

* **Staging**: `https://back.staging.splt.eu/partners_reports`
* **Production**: Provided by Superlotto.tv (unique for each partner)

{% hint style="info" %}
The endpoint accepts **GET** method requests only.
{% endhint %}

{% hint style="warning" %}
The endpoint has a limit of **5 requests per minute**. If exceeded, error code `104` will be returned.
{% endhint %}

## Required URL Components

| Component | Type | Description |
|-----------|------|-------------|
| `base_url` | string | Base URL provided by Superlotto.tv. Use staging URL for testing or production URL for live environment. |
| `partner_id` | integer | Your partner ID in the Superlotto.tv system, provided by Superlotto.tv. |
| `signature` | string | MD5 checksum generated from sent parameters (names and values), secret key, and today's date (YYYYMMDD in UTC+0). Must be in **lowercase**. See [Signature Formatting](signature-formatting.md) for details. |

## Example Request

```
https://back.staging.splt.eu/partners_reports/15/f8de1b09af1dafccd072a81899516c69
```

In this example:
- `base_url`: `https://back.staging.splt.eu/partners_reports`
- `partner_id`: `15`
- `signature`: `f8de1b09af1dafccd072a81899516c69`

