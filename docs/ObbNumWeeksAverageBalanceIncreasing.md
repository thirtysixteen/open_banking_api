# OpenBanking::ObbNumWeeksAverageBalanceIncreasing

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **historic_average_weekly_balances** | [**Array&lt;ObbAverageWeeklyBalance&gt;**](ObbAverageWeeklyBalance.md) | Average weekly balances over the known history |  |
| **historic_number_of_weeks_average_balance_increasing** | **Integer** | Number of weeks during the known history where the average balance of the account increased week over week |  |
| **historic_number_of_weeks_with_data_available** | **Integer** | Number of weeks during the history in which data was available |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbNumWeeksAverageBalanceIncreasing.new(
  historic_average_weekly_balances: null,
  historic_number_of_weeks_average_balance_increasing: 3,
  historic_number_of_weeks_with_data_available: 4
)
```

