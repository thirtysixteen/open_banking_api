# OpenBanking::ObbWeekOfYear

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **from_date** | **String** | Begin date of the week |  |
| **to_date** | **String** | End date of the week |  |
| **week** | **Integer** | Week number, where the first week of each year begins on January 1st and ends on January 7th. May be in the range [1, 53] |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbWeekOfYear.new(
  from_date: 2020-01-01,
  to_date: 2020-01-07,
  week: 1
)
```

