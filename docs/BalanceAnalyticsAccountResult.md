# OpenBanking::BalanceAnalyticsAccountResult

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_details** | [**ObbAccountDetails**](ObbAccountDetails.md) |  |  |
| **account_id** | **Integer** | An account ID represented as a number |  |
| **balance_analytics_metrics** | [**BalanceAnalyticsMetrics**](BalanceAnalyticsMetrics.md) |  | [optional] |
| **current_report_request** | [**ObbCurrentReportRequestDetails**](ObbCurrentReportRequestDetails.md) |  |  |
| **historic_data_availability** | [**ObbDataAvailability**](ObbDataAvailability.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::BalanceAnalyticsAccountResult.new(
  account_details: null,
  account_id: 5011648377,
  balance_analytics_metrics: null,
  current_report_request: null,
  historic_data_availability: null
)
```

