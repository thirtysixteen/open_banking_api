# OpenBanking::CashFlowNumWeeksZeros

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **historic_number_of_weeks_with_data_available** | **Integer** | Number of weeks during known history of account in which data was available |  |
| **historic_number_of_weeks_zero_transactions** | **Integer** | Number of weeks during known history of account where zero transactions were posted |  |
| **historic_weeks_with_zero_transactions** | [**Array&lt;ObbWeekOfYear&gt;**](ObbWeekOfYear.md) | List of weeks with zero reported transactions |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowNumWeeksZeros.new(
  historic_number_of_weeks_with_data_available: 10,
  historic_number_of_weeks_zero_transactions: 5,
  historic_weeks_with_zero_transactions: null
)
```

