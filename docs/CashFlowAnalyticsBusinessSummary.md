# OpenBanking::CashFlowAnalyticsBusinessSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cashflow_analytics_metrics** | [**CashFlowAnalyticsMetrics**](CashFlowAnalyticsMetrics.md) |  | [optional] |
| **current_report_request** | [**ObbCurrentReportRequestDetails**](ObbCurrentReportRequestDetails.md) |  |  |
| **historic_data_availability** | [**ObbDataAvailability**](ObbDataAvailability.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowAnalyticsBusinessSummary.new(
  cashflow_analytics_metrics: null,
  current_report_request: null,
  historic_data_availability: null
)
```

