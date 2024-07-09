# OpenBanking::StatePeriod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **beginning_value** | **Float** | Value on the first date in the period |  |
| **count** | **Integer** | Count of data points during the period |  |
| **end_date** | **Date** | End date for the period being reported |  |
| **ending_value** | **Float** | Value on the last date in the period |  |
| **max** | **Float** | Maximum amount during the period | [optional] |
| **mean** | **Float** | Mean of amounts during the period | [optional] |
| **median** | **Float** | Median of amounts during the period | [optional] |
| **min** | **Float** | Minimum amount during the period | [optional] |
| **standard_deviation** | **Float** | Standard deviation of amounts during the period | [optional] |
| **start_date** | **Date** | Start date for the period being reported |  |
| **sum** | **Float** | Sum of amounts during the period | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::StatePeriod.new(
  beginning_value: 60.21,
  count: 2,
  end_date: Sat Dec 31 18:00:00 CST 2022,
  ending_value: 60.21,
  max: 60.21,
  mean: 42.22,
  median: 42.22,
  min: 30.22,
  standard_deviation: 14.995,
  start_date: Wed Nov 30 18:00:00 CST 2022,
  sum: 90.43
)
```

