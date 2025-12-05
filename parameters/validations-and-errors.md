# Validations and errors

Service validates request parameters types, logic, signature.

For **incorrect requests** there are dedicated error codes:

<table><thead><tr><th width="103">Code</th><th width="163">Name</th><th>Reason</th><th>Solution</th></tr></thead><tbody><tr><td><strong><code>101</code></strong></td><td>invalid_params</td><td>Parameter does not exist or incorrect parameter type is used</td><td>Check if correct types / parameter names are used</td></tr><tr><td><strong><code>102</code></strong></td><td>no_permission</td><td>Partner does not have permission to get reports or wrong partner ID is used</td><td>Check if correct partner ID is used otherwise contact Superlotto.tv</td></tr><tr><td><strong><code>103</code></strong></td><td>invalid_signature</td><td>Wrong signature</td><td>Review <a href="signature-formatting.md">signature formatting</a></td></tr><tr><td><strong><code>104</code></strong></td><td>limit_exceeded</td><td>Exceeded requests limit per minute</td><td>Try again after a minute; reduce amount of calls in your application</td></tr><tr><td><strong><code>105</code></strong></td><td>incorrect_range</td><td>Wrong <strong><code>from</code></strong> and <strong><code>to</code></strong> range</td><td>Check date range rules</td></tr><tr><td><strong><code>106</code></strong></td><td>general_error</td><td>Other unnamed error</td><td>contact Superlotto.tv</td></tr><tr><td><strong><code>107</code></strong></td><td>incorrect_format</td><td>Not allowed format of report type</td><td>Check which formats are allowed for individual <a href="reports-types/">report types</a></td></tr></tbody></table>

{% hint style="success" %}
If the response is **successful**, code – **`100`**
{% endhint %}
