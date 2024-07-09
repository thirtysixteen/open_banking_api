# OpenBanking::ObbDateRangeAndAmount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Float** | Metric value for the given period | [optional] |
| **period** | **String** | Period represented by this metric |  |
| **period_begin_date** | **String** | Begin date of the period being reported |  |
| **period_end_date** | **String** | End date of the period being reported |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbDateRangeAndAmount.new(
  amount: 890.99,
  period: last30to1,
  period_begin_date: 2022-03-01,
  period_end_date: 2022-03-30
)
```

