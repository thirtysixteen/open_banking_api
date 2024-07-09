# OpenBanking::BalanceAnalyticsBusinessSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **balance_analytics_metrics** | [**BalanceAnalyticsMetrics**](BalanceAnalyticsMetrics.md) |  | [optional] |
| **current_report_request** | [**ObbCurrentReportRequestDetails**](ObbCurrentReportRequestDetails.md) |  | [optional] |
| **historic_data_availability** | [**ObbDataAvailability**](ObbDataAvailability.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::BalanceAnalyticsBusinessSummary.new(
  balance_analytics_metrics: null,
  current_report_request: null,
  historic_data_availability: null
)
```

