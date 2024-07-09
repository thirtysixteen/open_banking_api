# OpenBanking::CashFlowCashFlowBalance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monthly_cash_flow_balances** | [**Array&lt;CashFlowMonthlyCashFlowBalances&gt;**](CashFlowMonthlyCashFlowBalances.md) | List of attributes for each month |  |
| **min_daily_balance** | **Float** | Min daily balance across entire transaction history |  |
| **max_daily_balance** | **Float** | Max Daily Balance across entire transaction history |  |
| **twelve_month_average_daily_balance** | **Float** | Average Daily Balance across twelve months for the account |  |
| **six_month_average_daily_balance** | **Float** | Average Daily Balance across six months for the account |  |
| **two_month_average_daily_balance** | **Float** | Average Daily Balance across two months for the account |  |
| **twelve_month_standard_deviation_of_daily_balance** | **String** | Standard Deviation of Daily Balance across twelve months for the account |  |
| **six_month_standard_deviation_of_daily_balance** | **String** | Standard Deviation of Daily Balance across six months for the account | [optional] |
| **two_month_standard_deviation_of_daily_balance** | **String** | Standard Deviation of Daily Balance across two months for the account |  |
| **number_days_negative_balance** | **String** | Number of Days Negative Balance over entire transaction history | [optional] |
| **number_of_days_positive_balance** | **String** | Number of Days positive balance over entire transaction history |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowCashFlowBalance.new(
  monthly_cash_flow_balances: null,
  min_daily_balance: 3479.39,
  max_daily_balance: 3479.39,
  twelve_month_average_daily_balance: 3479.39,
  six_month_average_daily_balance: 3479.39,
  two_month_average_daily_balance: 3479.39,
  twelve_month_standard_deviation_of_daily_balance: 20,
  six_month_standard_deviation_of_daily_balance: 20,
  two_month_standard_deviation_of_daily_balance: 20,
  number_days_negative_balance: 6,
  number_of_days_positive_balance: 0
)
```

