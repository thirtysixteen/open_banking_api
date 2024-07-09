# OpenBanking::ObbDateRangeAndCount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **count** | **Integer** | Count of occurrences for the given period |  |
| **period** | **String** | Period represented by this metric |  |
| **period_begin_date** | **String** | Begin date of the period being reported |  |
| **period_end_date** | **String** | End date of the period being reported |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbDateRangeAndCount.new(
  count: 5,
  period: last30to1,
  period_begin_date: 2022-03-01,
  period_end_date: 2022-03-30
)
```

