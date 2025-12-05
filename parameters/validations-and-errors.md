---
icon: circle-exclamation
---

# Validations and Errors

The API validates request parameters (types and logic) and signature. For incorrect requests, dedicated error codes are returned.

## Success Response

{% hint style="success" %}
If the response is **successful**, the code is **`100`**.
{% endhint %}

## Error Codes

| Code | Name | Reason | Solution |
|------|------|--------|----------|
| `101` | `invalid_params` | Parameter does not exist or incorrect parameter type is used | Check if correct types and parameter names are used |
| `102` | `no_permission` | Partner does not have permission to get reports or wrong partner ID is used | Check if correct partner ID is used, otherwise contact Superlotto.tv |
| `103` | `invalid_signature` | Wrong signature | Review [signature formatting](signature-formatting.md) and ensure the signature is generated correctly |
| `104` | `limit_exceeded` | Exceeded requests limit per minute (5 requests/minute) | Try again after a minute; reduce the amount of calls in your application |
| `105` | `incorrect_range` | Wrong `from` and `to` date range | Check date range rules: `from` cannot be greater than `to`, and maximum range is 31 days |
| `106` | `general_error` | Other unnamed error | Contact Superlotto.tv for assistance |
| `107` | `incorrect_format` | Not allowed format for the selected report type | Check which formats are allowed for individual [report types](reports-types/README.md) |

## Example Error Response

```xml
<report>
    <status>
        <success>0</success>
        <info>invalid_signature</info>
        <code>103</code>
    </status>
</report>
```
