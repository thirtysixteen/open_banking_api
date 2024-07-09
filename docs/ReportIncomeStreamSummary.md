# OpenBanking::ReportIncomeStreamSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **confidence_type** | **String** | Possible values: \&quot;HIGH\&quot;, \&quot;MODERATE\&quot;, \&quot;LOW\&quot;, \&quot;NO\&quot; |  |
| **net_monthly** | [**Array&lt;NetMonthly&gt;**](NetMonthly.md) | A list of net monthly records. One instance for each complete calendar month in the report. |  |
| **income_estimate** | [**ReportIncomeEstimate**](ReportIncomeEstimate.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ReportIncomeStreamSummary.new(
  confidence_type: HIGH,
  net_monthly: null,
  income_estimate: null
)
```

