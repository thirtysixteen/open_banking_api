# OpenBanking::ReportIncomeEstimate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **net_annual** | **Float** | Sum of all values in &#x60;netMonthlyIncome&#x60; over the previous 12 months |  |
| **projected_net_annual** | **Float** | Projected net income over the next 12 months, across all income streams, based on &#x60;netAnnualIncome&#x60; |  |
| **estimated_gross_annual** | **Float** | Before-tax gross annual income (estimated from &#x60;netAnnual&#x60;) across all income stream in the past 12 months |  |
| **projected_gross_annual** | **Float** | Projected gross income over the next 12 months, across all active income streams, based on &#x60;projectedNetAnnual&#x60; |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ReportIncomeEstimate.new(
  net_annual: 1000.12,
  projected_net_annual: 1500.23,
  estimated_gross_annual: 2000.12,
  projected_gross_annual: 2500.23
)
```

