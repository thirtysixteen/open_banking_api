# OpenBanking::CashFlowMonthlyCashFlowBalanceSummaries

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **month** | **Integer** | One instance for each complete calendar month in the report |  |
| **min_daily_balance** | **Float** | Min Daily Balance for each month for all accounts |  |
| **max_daily_balance** | **Float** | Max Daily Balance for each month for all accounts |  |
| **average_daily_balance** | **Float** | Average Daily Balance for each month for all accounts |  |
| **standard_deviation_of_daily_balance** | **String** | Standard Deviation of Daily Balance for each month for all accounts | [optional] |
| **number_of_days_negative_balance** | **String** | Number of Days Negative Balance for each month for all accounts |  |
| **number_of_days_positive_balance** | **String** | Number of Days Positive Balance for each month for all accounts |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowMonthlyCashFlowBalanceSummaries.new(
  month: 1512111600,
  min_daily_balance: 3479.39,
  max_daily_balance: 3479.39,
  average_daily_balance: 3479.39,
  standard_deviation_of_daily_balance: 20.45454545,
  number_of_days_negative_balance: 6,
  number_of_days_positive_balance: 0
)
```

