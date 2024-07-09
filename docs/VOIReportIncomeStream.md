# OpenBanking::VOIReportIncomeStream

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Income stream ID |  |
| **name** | **String** | A human-readable name based on the &#x60;normalizedPayee&#x60; name of the transactions for this income stream |  |
| **status** | **String** | Possible values: \&quot;ACTIVE\&quot;, \&quot;INACTIVE\&quot; |  |
| **estimate_inclusion** | **String** | Possible values: \&quot;HIGH\&quot;, \&quot;MODERATE\&quot;, \&quot;LOW\&quot;, \&quot;NO\&quot; |  |
| **confidence** | **Integer** | Level of confidence that the deposit stream represents income (example: 85%) |  |
| **cadence** | [**CadenceDetails**](CadenceDetails.md) |  |  |
| **net_monthly** | [**Array&lt;NetMonthly&gt;**](NetMonthly.md) | A list of net monthly records. One instance for each complete calendar month in the report. | [optional] |
| **net_annual** | **Float** | Sum of all values in &#x60;netMonthlyIncome&#x60; over the previous 12 months | [optional] |
| **projected_net_annual** | **Float** | Projected net income over the next 12 months, across all income streams, based on &#x60;netAnnualIncome&#x60; | [optional] |
| **estimated_gross_annual** | **Float** | Before-tax gross annual income (estimated from &#x60;netAnnual&#x60;) across all income stream in the past 12 months | [optional] |
| **projected_gross_annual** | **Float** | Projected gross income over the next 12 months, across all active income streams, based on &#x60;projectedNetAnnual&#x60; | [optional] |
| **average_monthly_income_net** | **Float** | Monthly average amount over the previous 24 months | [optional] |
| **income_stream_months** | **Integer** | The number of months the income transactions are observed | [optional] |
| **transactions** | [**Array&lt;ReportTransaction&gt;**](ReportTransaction.md) | A list of transaction records |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::VOIReportIncomeStream.new(
  id: dens28i3vsch-voi1,
  name: none,
  status: ACTIVE,
  estimate_inclusion: HIGH,
  confidence: 70,
  cadence: null,
  net_monthly: null,
  net_annual: 110475.7,
  projected_net_annual: 0,
  estimated_gross_annual: 12321.1,
  projected_gross_annual: 151609,
  average_monthly_income_net: 9206.31,
  income_stream_months: 18,
  transactions: null
)
```

