# OpenBanking::CashFlowCashFlowBalanceSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monthly_cash_flow_balance_summaries** | [**Array&lt;CashFlowMonthlyCashFlowBalanceSummaries&gt;**](CashFlowMonthlyCashFlowBalanceSummaries.md) | List of attributes for each month |  |
| **min_daily_balance** | **Float** | Min Daily Balance across entire transaction history  for all accounts |  |
| **max_daily_balance** | **Float** | Max Daily Balance across entire transaction history for all accounts |  |
| **twelve_month_average_daily_balance** | **Float** | Average Daily Balance across twelve months for all accounts |  |
| **six_month_average_daily_balance** | **Float** | Average Daily Balance across six months for all accounts |  |
| **two_month_average_daily_balance** | **Float** | Average Daily Balance across two months for all accounts |  |
| **twelve_month_standard_deviation_of_daily_balance** | **String** | Standard Deviation of Daily Balance across twelve months for all accounts |  |
| **six_month_standard_deviation_of_daily_balance** | **String** | Standard Deviation of Daily Balance across six months for all accounts | [optional] |
| **two_month_standard_deviation_of_daily_balance** | **String** | Standard Deviation of Daily Balance across two months for all accounts |  |
| **number_of_days_negative_balance** | **String** | Number of Days Negative Balance over entire transaction history for all accounts |  |
| **number_of_days_positive_balance** | **String** | Number of Days Positive Balance over entire transaction history for all accounts |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowCashFlowBalanceSummary.new(
  monthly_cash_flow_balance_summaries: null,
  min_daily_balance: 3479.39,
  max_daily_balance: 3479.39,
  twelve_month_average_daily_balance: 3479.39,
  six_month_average_daily_balance: 3479.39,
  two_month_average_daily_balance: 3479.39,
  twelve_month_standard_deviation_of_daily_balance: 20,
  six_month_standard_deviation_of_daily_balance: 20,
  two_month_standard_deviation_of_daily_balance: 20,
  number_of_days_negative_balance: 6,
  number_of_days_positive_balance: 11
)
```

