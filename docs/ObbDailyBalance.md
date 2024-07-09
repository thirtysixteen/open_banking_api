# OpenBanking::ObbDailyBalance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** | Date of balance information |  |
| **day_of_week** | **String** | Day of the week for which balance information available |  |
| **ending_balance** | **Float** | End of day balance |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbDailyBalance.new(
  date: 2021-10-11,
  day_of_week: Monday,
  ending_balance: 21527.3
)
```

