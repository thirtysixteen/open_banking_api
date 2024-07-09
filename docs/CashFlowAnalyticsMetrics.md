# OpenBanking::CashFlowAnalyticsMetrics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inflow** | [**CashFlowInflowAttributes**](CashFlowInflowAttributes.md) |  | [optional] |
| **negative_triggers** | [**CashFlowNegativeTriggers**](CashFlowNegativeTriggers.md) |  | [optional] |
| **outflow** | [**CashFlowOutflowAttributes**](CashFlowOutflowAttributes.md) |  | [optional] |
| **revenue_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Sum of all transactions categorized as revenue, split by months | [optional] |
| **revenue_for_the_report_time_period** | **Float** | Sum of all transactions categorized as revenue | [optional] |
| **transaction_analytics** | [**CashFlowTransactionAnalyticsAttributes**](CashFlowTransactionAnalyticsAttributes.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowAnalyticsMetrics.new(
  inflow: null,
  negative_triggers: null,
  outflow: null,
  revenue_by_month_for_the_report_time_period: null,
  revenue_for_the_report_time_period: 43893.44,
  transaction_analytics: null
)
```

