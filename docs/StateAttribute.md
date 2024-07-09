# OpenBanking::StateAttribute

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attribute_name** | **String** | Name of Attribute as mentioned in Data Dictionary |  |
| **reported_by_time_periods** | [**Array&lt;StateTimeInterval&gt;**](StateTimeInterval.md) | List of state values grouped by specified Time Interval |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::StateAttribute.new(
  attribute_name: NET_CASH_FLOW,
  reported_by_time_periods: null
)
```

