---
icon: qrcode
---

# Signature Formatting

The request signature is generated using an **MD5 hash** of all passed parameters (names and values), secret key, and today's date (YYYYMMDD in UTC+0).

## Concatenation Order

The signature is created by concatenating the following components in this specific order:

1. **Partner ID** (integer)
2. **Parameters** (only if present) - parameter names and values in the order they appear in the URL
3. **Secret key** (provided by Superlotto.tv)
4. **Date** (YYYYMMDD format in UTC+0 timezone)

After concatenation, generate an MD5 hash of the resulting string.

{% hint style="warning" %}
The MD5 signature must be passed in **lowercase** in the URL.
{% endhint %}

{% hint style="info" %}
Always use **UTC+0 timezone** for the date, regardless of your local timezone.
{% endhint %}

## Step-by-Step Process

1. Get today's date in `YYYYMMDD` format using UTC+0 timezone (e.g., `20180813`)
2. Get your partner ID (integer, e.g., `15`)
3. Get your secret key (provided by Superlotto.tv, e.g., `4598-8596`)
4. If parameters are present, get parameter names and values in the order they appear in the URL
5. Concatenate all values in order: `partner_id + parameters + secret_key + date`
6. Generate MD5 hash of the concatenated string (must be lowercase)

## Examples

{% tabs %}
{% tab title="Example 1: No Parameters" %}
**Base URL**: `https://back.staging.splt.eu/partners_reports`

**Parameters**:
- Partner ID: `15`
- Secret key: `4598-8596`
- Date (UTC+0): `20180813` (August 13, 2018)
- No additional parameters (using defaults)

**Step 1: Concatenate values**
```
15 + 4598-8596 + 20180813 = 154598-859620180813
```

**Step 2: Generate MD5 hash**
```
f8de1b09af1dafccd072a81899516c69
```

**Final URL**:
```
https://back.staging.splt.eu/partners_reports/15/f8de1b09af1dafccd072a81899516c69
```
{% endtab %}

{% tab title="Example 2: With Date Parameters" %}
**Base URL**: `https://back.staging.splt.eu/partners_reports`

**Parameters**:
- Partner ID: `15`
- Secret key: `4598-8596`
- Date (UTC+0): `20180813`
- `from`: `2018081000` (August 10, 2018 00:00)
- `to`: `2018081223` (August 12, 2018 23:00)
- `utc`: `3` (UTC+3)

**Step 1: Concatenate values (parameter names and values in order)**
```
15 + from + 2018081000 + to + 2018081223 + utc + 3 + 4598-8596 + 20180813
= 15from2018081000to2018081223utc34598-859620180813
```

**Step 2: Generate MD5 hash**
```
7c971bc319c93dda4b9bb37f461e67aa
```

**Final URL**:
```
https://back.staging.splt.eu/partners_reports/15/7c971bc319c93dda4b9bb37f461e67aa?from=2018081000&to=2018081223&utc=3
```
{% endtab %}

{% tab title="Example 3: With All Parameters" %}
**Base URL**: `https://back.staging.splt.eu/partners_reports`

**Parameters**:
- Partner ID: `15`
- Secret key: `4598-8596`
- Date (UTC+0): `20180813`
- `report_type`: `7`
- `from`: `2018081000`
- `to`: `2018081223`
- `report_format`: `json`
- `utc`: `3`

**Step 1: Concatenate values (parameter names and values in order)**
```
15 + report_type + 7 + from + 2018081000 + to + 2018081223 + report_format + json + utc + 3 + 4598-8596 + 20180813
= 15report_type7from2018081000to2018081223report_formatjsonutc34598-859620180813
```

**Step 2: Generate MD5 hash**
```
1f8c219292581eeaea83adcb8a0bdfb1
```

**Final URL**:
```
https://back.staging.splt.eu/partners_reports/15/1f8c219292581eeaea83adcb8a0bdfb1?report_type=7&from=2018081000&to=2018081223&report_format=json&utc=3
```
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Important**: Parameter names and values must be concatenated in the exact order they appear in the URL query string. The order matters for signature generation.
{% endhint %}





